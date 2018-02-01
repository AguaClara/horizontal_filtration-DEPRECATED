```python
from aide_design.play import*
```

### Timeline Spring  2018
1.  Sloped Bottom
  - What bottom geometry will be necessary to make sure all the sand fluidize during backwash?
  - What angle? Curved?
  - how will it be fabricated
    - during testing
    - for later on
2. Calculation of force on plate settlers  + construction design
  - can a simple calculation of force based on upflow and hydrostatics be determined?
    - where does the angle matter here?
3. Stoppage of sand escape during backwash    
3. Location of settlers with respect to inlet holes
  - probably just over it?
4. Size of inlet and outlet holes
  - function of flow and depth
  - bigger holes on bottom layer for backwash
  - flow characteristics and loss calculations (probably unnecessary to some extent)
5. Is it possible for water to short circuit anywhere?
  - if backwash isn't thorough (but it should be), will water zoom over the top and back in?
6. At the speeds we are at will it be apparent where the water is going?
  - DYE!

```python
V_filter = 1.8*(u.mm/u.s)
Q_plant = 1*u.L/u.s
area_flow = Q_plant/V_filter
print(area_flow.to(u.m**2))
side_length = area_flow**(1/2)
print(side_length.to(u.m))
S```
