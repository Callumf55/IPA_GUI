# IPA_GUI
Instructions and descriptions for the IPA GUI

## Databases:
One of the most powerful features of the IPA method is that it is able to integrate the knowledge gained from previous experiments in the annotation process. There are three files that are used as the IPA database:

### **1. Adducts file (required)**
<br />
The ipaPy2 library requires a file contains all the information required for the computation of the adducts. An adducts.csv file is provided with the package [here](DB/adducts.csv). The file contains the most common adducts. If any exotic adduct (or in-source fragment) needs to be considered, the user must modify the file accordingly. The format required for the adducts file is shown below. 



```python
import pandas as pd
import numpy as np
adducts = pd.read_csv('DB/adducts.csv')
adducts.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>calc</th>
      <th>Charge</th>
      <th>Mult</th>
      <th>Mass</th>
      <th>Ion_mode</th>
      <th>Formula_add</th>
      <th>Formula_ded</th>
      <th>Multi</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M+H</td>
      <td>M+1.007276</td>
      <td>1</td>
      <td>1</td>
      <td>1.007276</td>
      <td>positive</td>
      <td>H1</td>
      <td>FALSE</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M+NH4</td>
      <td>M+18.033823</td>
      <td>1</td>
      <td>1</td>
      <td>18.033823</td>
      <td>positive</td>
      <td>N1H4</td>
      <td>FALSE</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M+Na</td>
      <td>M+22.989218</td>
      <td>1</td>
      <td>1</td>
      <td>22.989218</td>
      <td>positive</td>
      <td>Na1</td>
      <td>FALSE</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M+K</td>
      <td>M+38.963158</td>
      <td>1</td>
      <td>1</td>
      <td>38.963158</td>
      <td>positive</td>
      <td>K1</td>
      <td>FALSE</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M+</td>
      <td>M-0.00054858</td>
      <td>1</td>
      <td>1</td>
      <td>-0.000549</td>
      <td>positive</td>
      <td>FALSE</td>
      <td>FALSE</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
