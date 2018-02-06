```python
from aide_design.play import*
```
#Preliminary Calculations

##Filter Dimensions
The team must first calculate the dimensions of the sand filter space which will make up a section of the overall apparatus. To do this, HorFi takes into account the velocity at which water moves through a sand filter and the desired flow rate of the system. Since creating a 1 L/s apparatus would take all semester, the team begins with a scale model at 0.1 L/s.

Since the backwash velocity (V_backwash) is greater than the filter velocity (V_filter), it is the design constraint. With some math, the area of backwash (A_backwash) may be calculated.

```python
V_filter = 1.8*(u.mm/u.s)
V_backwash = 9*(u.mm/u.s)  #the constraining velocity
Q_plant = .1*(u.L/u.s)
A_backwash = Q_plant/V_backwash
```
From here, the team must incorporate some knowledge on the depth in which water travels through a traditional AguaClara OStaRS filter. The filter backwash ratio is the ratio between settled sand height during filtration and expanded sand height during backwash. The headloss of the system will act as the constraining depth for filter height. Because the filter backwash ratio is 1.3 (PiFiBw), which has been empirically determined, the team must determine the headloss they are working with first and divide by this ratio to get the desired depth of sand. **NOTE: We believe the headloss is the total height of the tank. Is this correct?**

The team decides that with the scale model in mind, 6 inches of headloss is a fair parameter. This was determined by manipulating the head value in the calculations below to get realistic dimensions for a fish tank.


```python
headloss = 6*(u.inch) #height of fish tank
PiFiBw = 1.3
V_ratio = V_backwash/V_filter #ratio is 5 to 1
filter_height = headloss/PiFiBw #height of sand
A_flow = Q_plant/V_filter #cross sectional area of sand
filter_width = A_flow/filter_height #width of sand
filter_length = filter_height*V_ratio #length of sand
V_filterbox = headloss*filter_length*filter_width
print(filter_height.to(u.inch))
print(filter_width.to(u.inch))
print(filter_length.to(u.inch))
print(V_filterbox.to(u.gallon))
```

Based on these calculations, the team needs to order a fish tank that is at least 6 inches tall and can hold about 11 gallons of volume in addition to the volume necessary for inlet and outlet water for pre and post treatment.
