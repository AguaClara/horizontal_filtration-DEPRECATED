```python
from aguaclara.play import*
import math
import numpy as np

import pandas as pd
from aguaclara.core.units import unit_registry as u


Area = 1.767*u.millimeter**2
Approach_velocity = 5* u.millimeter/u.second
Flow_rate = Approach_velocity*Area
print(Flow_rate)

```
