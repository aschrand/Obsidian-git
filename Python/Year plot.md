---
author: André Schrander
Type: example
tags: [Python, Programming]
---

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import calendar
import datetime as dt
 
#pd.set_option('display.mpl_style', 'default') # Make the graphs a bit prettier
plt.rcParams['figure.figsize'] = (15,9)
plt.rcParams['font.family'] = 'sans-serif'
#plt.close('all')
 
Excelfile = 'd:\\Gebruikers\\schra\\Python projects\\databestanden\\Maand mei2020.csv'
 
df = pd.read_csv(Excelfile, sep=';',decimal=",", encoding='latin1', parse_dates=True, index_col='Datum')
 
watts = df.loc[df['Type'] == 'electricity_produced']
 
pv = pd.pivot_table(watts, index=watts.index.month, columns=watts.index.year, values='Waarde(kWh)', fill_value=0, aggfunc='sum')
pv = pv.cumsum()
pv.plot()
plt.show()
print(pv)
```

[[Show-all-wifi-passwords]]

![[Maand mei2020.csv]]