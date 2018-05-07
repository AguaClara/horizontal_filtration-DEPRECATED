### Variables
- **A note on the coordinate system**: length is used to mean parallel to flow direction, so filter length is the horizontal distance the water flows within the sand section of the filter. Width the direction perpendicular to flow direction; center plates are spaced along the width of the filter. Height is the vertical direction.

##### Calculation of Backwash and Flow Area
- $V_{filter}$=***V_filter***=Velocity of filtration
- $V_{backwash}$=***V_backwash***=Velocity of water during backwash
- $Q_{plant}$=***Q_plant***=Water flow through plant
- $A_{backwash}$=***A_backwash***=Area of backwash
- $A_{flow}$=***A_flow***=Cross sectional area of sand/area of flow

##### Calculation of Filter Box Dimensions
- $\pi_{FiBw}$=***PiFiBw***=Volume increase ratio due to sand bed fluidization
- $l_{filter}$=***filter_length***=Length of filter
- $w_{filter}$=***filter_width***=Width of filter
- $h_{filter}$=***filter_height***=Height of entire filter
- $h_{box}$=***box_height***=Height of utilized box model

##### Calculation of Necessary Filter Shelf Length
- $\nu$=Kinematic viscosity
- $\rho_{sand}$=***rho_sand***=Density of particle
- $\rho_{water}$=***rho_water***=Density of water
- $\nu_{water}$=***nu_water***=kinematic viscosity of Water
- $d_{sand}$=***d_sand***=Diameter of sand particles
- $SF$=***SF***=Safety factor
- $\theta_{settling}$=***angle_settling***= Angle of filter shelves
- $V_{setting}$=***V_settling***=Velocity until the sand settles
- $V_{capture}$=***V_capture***=Safe estimate of velocity needed to capture the sand
- $V_{\alpha}$=***V_alpha***=Filter speed
- $V_{actual}$=***V_actual***=Filter speed after filter shelf
- $\alpha$=***alpha***=angle of shelves
- $l_{shelf}$=***L***=Length of filter shelf

##### Filter Shelf Dimension and Spacing Calculations
- $d_{shelf}$=***space_shelf***=Spacing between filter shelves (top to top)
- $d_{holes}$=***diam_holes***=Diameter of the holes in walls
- $N_{holes}$=***num_holes***=Number of holes on either side
- $\pi_{orifice}$=***pi_orifice***=Shrinking coefficient of water through area
- $h_{hole}$=***headloss_hole***=Headloss through the hole
- $t_{shelf}$=***thickness_shelf***=The thickness of the shelves
- $d_{sandlift}$=***space_sandlift***=Safety factor for sand to lift
- $d_{abovehole}$=***space_above_hole***=The spacing between the hole and the bottom of the Shelf
- $l_{vert}$=***L_vert***=Spacing between shelves, top to top=***space_shelf***
- $l_{shelf}$=***L***=Length of filter shelf
- $l_{notch}$=***L_notch***=Length of the notch into the filter Shelf
- $l_{horizontal}$=***L_horizontal***=Length of horizontal component of filter shelf
- $l_{insert}$=***insert_length***=Length of the filter insert to which the filter shelves are connected


Below is the equation for terminal settling velocity where d is diameter, $\nu$ is kinematic viscosity. This is used for laminar flow.

$$ Vt = \frac{d^2g}{18\nu}(\frac{\rho_{particle}-\rho_{H2O}}{\rho_{H2O}}) $$

After consultation with Professor Monroe Weber Shirk, it is necessary to also make calculations with turbulence in mind since sand settles rather quickly and experiences drag.

$$ Vt = \sqrt\frac{4g}{3Cd}\frac{\rho_{sand}-\rho_{H2O}}{\rho_{H2O}}    $$


```python
from aide_design.play import*
V_filter = 1.8*(u.mm/u.s)
V_backwash = 9*(u.mm/u.s)  #the constraining velocity
Q_plant = .37*(u.L/u.s)  #the scale we are working with for our first
#iteration of the filter, manipulated to achieve desired width
A_backwash = Q_plant/V_backwash #plan view area of sand (x,y axis)
A_flow = Q_plant/V_filter  #cross sectional area of sand (x,z axis)
```
From here, the team incorporated some knowledge on the depth in which water travels through a traditional AguaClara  Open Stacked Rapid Sand (OStaRS) filter. The filter backwash ratio is the ratio between settled sand height during filtration and expanded sand height during backwash. Because the filter backwash ratio is 1.3 (PiFiBw), which has been empirically determined, the team determined a settled sand height first.



The team decided that with the scale model in mind, 3.65 inches of sand in the flow direction (filter_length) is a fair parameter to start with. With this one measurement, and the ratio between filter velocity and backwash velocity, all other parameters fall into place.


```python
PiFiBw = 1.3
filter_length = 3.65*u.inch  #manipulated to achieve desired height
filter_width = A_backwash/filter_length #the filter
#width is the width for BOTH areas
filter_height = A_flow/filter_width
filter_height #height of sand
box_height = filter_height*PiFiBw #the height the expanded sand bed
box_height
#the box we ordered is 18 inch by 18 inch by 24 inch
#with wall thickness of 0.25 inches
print(box_height.to(u.inch)) #must be 0.25 less than actual because of thickness
#of the box floor ordered
print(filter_width.to(u.inch)) #must be 0.25*2 less than actual because of
#thickness of walls on either side
print('The height of the tank should be at least',box_height.to(u.inch),
'with a cross-sectional width of',filter_width.to(u.inch),'(thicknesses omitted).')
>>> height is 23.72 inches, cross sectional width of 17.46 inches
```

```python
SF =2 #safety factor suggested by AguaClara Engineer Ethan Keller

rho_sand = 1602*u.kg/u.m**3 #density of sand
rho_water = 1000*u.kg/u.m**3 #density of water at 20 C
nu_water = (pc.viscosity_kinematic(293*u.K)) #kinematic viscosity of water at 20 C
d_sand = 0.5*u.mm #diameter of sand particle
alpha = 55*u.degrees #angle of filter shelves
V_alpha=1.8*u.mm/u.second
 #filter speed!

V_actual = V_alpha/np.cos(alpha) #speed within the angled shelf
S=(1*u.inch).to(u.mm) #distance between shelves (above or below)

V_settling1=((d_sand**2)*pc.gravity/(18*nu_water))*((rho_sand-rho_water)/rho_water)
V_settling1.to(u.mm/u.s)  #settling velocity (Vt) without drag and turbulence
>>>82 mm/s
V_capture1 = V_settling1/SF #Capture velocity with safety factor incorporated
V_capture1.to(u.mm/u.s) #initial capture velocity
>>>41 mm/s

Re = (V_backwash)*(1*u.inch)/(nu_water)
Re.magnitude #Reynold's number for drag coefficient calc
Cd = 0.2 #drag coefficient corresponding with ~10^7
V_settling2 = np.sqrt(((4*pc.gravity*d_sand)/(3*Cd))*((rho_sand-rho_water)/rho_water))
V_settling2.to(u.mm/u.s)
>>> 140 mm/s #this velocity uses the drag coefficient based of the Reynolds number
V_capture2 = V_settling2/2
>>> 70 mm/s #alternative capture velocity

L1 = ((V_actual*S/V_capture1-S)/(np.cos(alpha)*np.sin(alpha)))
L2 = (S/np.cos(alpha))*((V_actual/V_capture2)-(1/np.sin(alpha)))
L1.to(u.inch)
L2.to(u.inch)
>>L1 = -1.96 inches
>>L2 = -2.05 inches
```
These lengths make the team believe that the length of the filter shelf is arbitrary due to their negative value. This seemed to correlate with the experiments as well.


From here, the team worked to calculate and parametrize the filter shelf insert. The following calculations are the steps used in calculating the filter shelf length. That is, how far into the filter they must protrude.


```python
#we decided that the diameter of a hole should be 0.25 inches and we worked from there.
space_shelf = 0.25*filter_length #this relationship was determined by Monroe as a
# reasonable measure. space_shelf is the total space between respective shelves. It is
# the same thing as L_vert.
>>space_shelf = .9125 inches (2.318 cm)

diam_holes = 0.25*u.inch
num_holes = filter_height.to(u.cm)/space_shelf.to(u.cm)
>>> num_holes = 20

# what is the headloss? (due to wall in middle of insert, 
# there will be twice as many holes)
pi_orifice = 0.62
headloss_hole= pc.head_orifice(diam_holes,pi_orifice,Q_plant/(2*num_holes))
>>>headloss_hole = 1.13 cm

thickness_shelf = 0.125*u.inch #acrylic shelf
space_sandlift = 1*u.cm  #space_sandlift was a guessed value of a safety for how
#high the sand would climb in between adjacent plate shelves
space_above_hole = space_shelf-diam_holes-thickness_shelf/np.sin(alpha)-space_sandlift
space_above_hole.to(u.cm)
>> space_above_hole = .2952 cm #space above hole
L_vert = (diam_holes+thickness_shelf/np.sin(alpha)+space_sandlift+space_above_hole)
L_vert.to(u.cm)
>>>L_vert = 2.3177 cm
L = L_vert/(np.sin(alpha))
L.to(u.cm)
>> L = 2.82945 cm #length of filter shelf
L_notch = L/4 #for support of the material
>> L_notch = .70736 cm

L_horizontal = L*np.cos(alpha)
>> L_horizontal = 1.62291 cm

insert_length = 2*L_horizontal+filter_length
>> length_insert = 12.517 cm
```
From these calculations and the given constraints, the length of the filter shelves is 2.829 cm and the length of the insert is 12.517 cm. With these values, the overall apparatus could be fabricated in Fusion.

### Fusion360

### Stress and Displacement Analysis

In order to see how plausible this design is, a stress test was performed on the acrylic box with the expected hydrostatic forces in mind.
<center>

|![stress_test](https://github.com/AguaClara/horizontal_filtration/blob/master/images/stress.PNG?raw=true)]|
|:---:|
|Figure 3: Stress calc on box|
</center>

This stress analysis could then be translated into an approximate displacement of the box itself.

<center>

|![displacement](https://github.com/AguaClara/horizontal_filtration/blob/master/images/displacement.PNG?raw=true)|
|:---:|
|Figure 4: displacement|
</center>

Since the walls would only flex a max of 2.88 mm, the design is structurally sound.
