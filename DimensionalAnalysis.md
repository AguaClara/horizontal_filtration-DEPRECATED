```python
from aide_design.play import*
```
#Preliminary Calculations

##Filter Dimensions
The team must first calculate the dimensions of the sand filter space which will make up a section of the overall apparatus. To do this, HorFi takes into account the velocity at which water moves through a sand filter and the desired flow rate of the system. Since creating a 1 L/s apparatus would take all semester, the team begins with a scale model at 0.1 L/s.

Since the backwash velocity (V_backwash) is greater than the filter velocity (V_filter), it is the design constraint. With some math, the area of backwash (A_backwash) and area of flow (A_flow) may be calculated.


```python
V_filter = 1.8*(u.mm/u.s)
V_backwash = 9*(u.mm/u.s)  #the constraining velocity
Q_plant = .1*(u.L/u.s)  #the scale we are working with for our first iteration of the filter
A_backwash = Q_plant/V_backwash #plan view area of sand (x,y axis)
A_flow = Q_plant/V_filter  #cross sectional area of sand (x,z axis)
```
From here, the team must incorporate some knowledge on the depth in which water travels through a traditional AguaClara OStaRS filter. The filter backwash ratio is the ratio between settled sand height during filtration and expanded sand height during backwash. Because the filter backwash ratio is 1.3 (PiFiBw), which has been empirically determined, the team must determine a settled sand height first.

The team decides that with the scale model in mind, 4 cm of sand in the flow direction (filter_length) is a fair parameter to start with. With this one measurement, and the ratio between filter velocity and backwash velocity, all other parameters fall into place.

```python
PiFiBw = 1.3
filter_length = 4*u.cm  #pre-determined
filter_width = A_backwash/filter_length #the filter width is the width for BOTH areas
filter_height = A_flow/filter_width #height of sand
box_height = filter_height*PiFiBw #the height the expanded sand bed
V_filterbox = filter_width*filter_length*box_height
print('The height of the tank should be at least',box_height,'with a cross-sectional width of',filter_width.to(u.cm),'.')
print(V_filterbox.to(u.gallon))
```

Based on these calculations, the team needs to order a fish tank that is at least 26 cm tall and can hold a little over 3/4 gallon of volume in addition to the volume necessary for inlet and outlet water for pre and post treatment.

Another aspect of design that the team will need to  determine is the dimensions of the filter shelves that will prevent sand from leaving the filter. Determining these dimensions involves the settling velocity of sand, distance between shelves (S), number of holes, and the forces that will be acting on the shelves during normal operation and during backwash.

A safety factor of 2 will be used for the capture velocity of the sand to further ensure sand will not escape.

Below is the equation for terminal settling velocity where d is diameter, $\nu$ is kinematic viscocity
$$ Vt = \frac{d^2g}{18\nu}(\frac{\rho_{particle}-\rho_{H2O}}{\rho_{H2O}}) $$

```python
rho_sand = 1602*u.kg/u.m**3
rho_water = 1000*u.kg/u.m**3
nu_water = 1*10**-6 *u.m**2/u.s
d_sand = .5*u.mm
SF = 2 #safety factor

V_settling=(d_sand**2)*pc.gravity/(18*nu_water)*((rho_sand-rho_water)/rho_water)
V_settling.to(u.mm/u.s)
V_capture = V_settling/SF
angle_settling = 60*u.degrees
V_capture.to(u.mm/u.s)


diam_hole = 1*u.inch
num_holes = 1

flow_max_tank = (V_filter * 18*u.inch *(24/PiFiBw)*u.inch).to(u.l/u.s)
flow_max_tank
l_max = flow_max_tank/(V_backwash*18*u.inch)

l_max.to(u.inch)
###number of holes in the wall!
#while num_holes < 100:

  #diam_hole = diam_hole- .01*u.inch
  #area_hole = pc.area_circle(diam_hole)
  #num_holes = (flow_max_tank/(V_filter*area_hole)).magnitude

#print(diam_hole)
a_holes = 3166*u.mm**2
V_max_holes = (flow_max_tank/a_holes).to(u.mm/u.s)

n_holes = 100

#prelim calc for filter length with full box

V_alpha=1.8*u.mm/u.second #upflow filter speed!
S=(1.8*u.inch).to(u.mm) #distance between shelves
alpha=np.pi/3 #angle of shelves

L=(((V_max_holes*S/V_capture)-S)/(np.cos(alpha)*np.sin(alpha)))
L.to(u.inch)
```




The next challenge for the team is determining the bottom geometry of the filtration box. The geometry is essential for proper backwash of the filter. With an angled bottom, all the sand within the filter should be backwashed, whereas with a flat bottom there could be dead zones of sand on the lower downstream side of the filter.

```python
angle_repose_min = 15*u.degree
angle_repose_max = 30*u.degree
#starting with the shallowest angle should work? We can also check with our sand


```
