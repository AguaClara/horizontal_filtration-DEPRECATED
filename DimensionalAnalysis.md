```python
from aide_design.play import*
```
#Preliminary Calculations

##Flow Area
The team must first calculate the dimensions of the tank which will make up the size of the overall apparatus. To do this, HorFi takes into account the velocity at which water moves through a sand filter and the desired flow rate of the system (1 L/s).

```python
V_filter = 1.8*(u.mm/u.s)
Q_plant = 1*u.L/u.s
area_flow = Q_plant/V_filter
print(area_flow.to(u.m**2))
side_length = area_flow**(1/2)
print(side_length.to(u.m))
```
