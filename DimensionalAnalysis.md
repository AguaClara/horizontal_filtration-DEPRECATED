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

The next challenge for the team is determining the bottom geometry of the filtration box. The geometry is essential for proper backwash of the filter. With an angled bottom, all the sand within the filter should be backwashed, whereas with a flat bottom there could be dead zones of sand on the lower downstream side of the filter.

```python
angle_repose_min = 15*u.degree
angle_repose_max = 30*u.degree
#starting with the shallowest angle should work? We can also check with our sand
```

Another aspect of design that the team will need to  determine is the dimensions of the filter shelves that will prevent sand from leaving the filter. Determining these dimensions involves the settling velocity of sand as well as the forces that will be acting on the shelves during normal operation and during backwash. A safety factor of 2 will be used for the capture velocity of the sand to further ensure sand will not escape.

[sand source](http://www3.kau.se/kurstorg/files/t/82F314521618f25B28NvM1BAA55E/TutorialFallingSandgrain.pdf_)
The capture velocity of the shelves (V<sub>capture</sub>) must be less than or equal to the terminal settling velocity of the average sand particle. According to the source above, this value is .291 m/s.

$$ Vt = \sqrt{\frac{4gd(\rho_{particle}-\rho_{H2O})}{3C_{D}\rho_{H2O}}} $$

```python
diam_avg =
V_capture =
angle_settling = 60*u.degrees


```
