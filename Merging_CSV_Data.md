

```python
# Import Dependencies
import glob
import pandas as pd
import os
```


```python
# Use glob to load all CSVs for 2017
path = r"raw_data"
all_files = glob.glob(os.path.join(path, "*.csv"))
records_df = [pd.read_csv(file) for file in all_files]
# print(records_df)
```


```python
# Merge all CSVs with concatenation
citi_bikes_2017 = pd.concat(records_df, ignore_index=True)
```


```python
citi_bikes_2017
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Trip Duration</th>
      <th>Start Time</th>
      <th>Stop Time</th>
      <th>Start Station ID</th>
      <th>Start Station Name</th>
      <th>Start Station Latitude</th>
      <th>Start Station Longitude</th>
      <th>End Station ID</th>
      <th>End Station Name</th>
      <th>End Station Latitude</th>
      <th>End Station Longitude</th>
      <th>Bike ID</th>
      <th>User Type</th>
      <th>Birth Year</th>
      <th>Gender</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>680</td>
      <td>2017-01-01 00:00:21</td>
      <td>2017-01-01 00:11:41</td>
      <td>3226</td>
      <td>W 82 St &amp; Central Park West</td>
      <td>40.782750</td>
      <td>-73.971370</td>
      <td>3165</td>
      <td>Central Park West &amp; W 72 St</td>
      <td>40.775794</td>
      <td>-73.976206</td>
      <td>25542</td>
      <td>Subscriber</td>
      <td>1965.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1282</td>
      <td>2017-01-01 00:00:45</td>
      <td>2017-01-01 00:22:08</td>
      <td>3263</td>
      <td>Cooper Square &amp; E 7 St</td>
      <td>40.729236</td>
      <td>-73.990868</td>
      <td>498</td>
      <td>Broadway &amp; W 32 St</td>
      <td>40.748549</td>
      <td>-73.988084</td>
      <td>21136</td>
      <td>Subscriber</td>
      <td>1987.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>648</td>
      <td>2017-01-01 00:00:57</td>
      <td>2017-01-01 00:11:46</td>
      <td>3143</td>
      <td>5 Ave &amp; E 78 St</td>
      <td>40.776829</td>
      <td>-73.963888</td>
      <td>3152</td>
      <td>3 Ave &amp; E 71 St</td>
      <td>40.768737</td>
      <td>-73.961199</td>
      <td>18147</td>
      <td>Customer</td>
      <td>NaN</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>631</td>
      <td>2017-01-01 00:01:10</td>
      <td>2017-01-01 00:11:42</td>
      <td>3143</td>
      <td>5 Ave &amp; E 78 St</td>
      <td>40.776829</td>
      <td>-73.963888</td>
      <td>3152</td>
      <td>3 Ave &amp; E 71 St</td>
      <td>40.768737</td>
      <td>-73.961199</td>
      <td>21211</td>
      <td>Customer</td>
      <td>NaN</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>621</td>
      <td>2017-01-01 00:01:25</td>
      <td>2017-01-01 00:11:47</td>
      <td>3143</td>
      <td>5 Ave &amp; E 78 St</td>
      <td>40.776829</td>
      <td>-73.963888</td>
      <td>3152</td>
      <td>3 Ave &amp; E 71 St</td>
      <td>40.768737</td>
      <td>-73.961199</td>
      <td>26819</td>
      <td>Customer</td>
      <td>NaN</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>666</td>
      <td>2017-01-01 00:01:51</td>
      <td>2017-01-01 00:12:57</td>
      <td>3163</td>
      <td>Central Park West &amp; W 68 St</td>
      <td>40.773407</td>
      <td>-73.977825</td>
      <td>3163</td>
      <td>Central Park West &amp; W 68 St</td>
      <td>40.773407</td>
      <td>-73.977825</td>
      <td>16050</td>
      <td>Subscriber</td>
      <td>2000.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>559</td>
      <td>2017-01-01 00:05:00</td>
      <td>2017-01-01 00:14:20</td>
      <td>499</td>
      <td>Broadway &amp; W 60 St</td>
      <td>40.769155</td>
      <td>-73.981918</td>
      <td>479</td>
      <td>9 Ave &amp; W 45 St</td>
      <td>40.760193</td>
      <td>-73.991255</td>
      <td>27294</td>
      <td>Subscriber</td>
      <td>1973.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>826</td>
      <td>2017-01-01 00:05:37</td>
      <td>2017-01-01 00:19:24</td>
      <td>362</td>
      <td>Broadway &amp; W 37 St</td>
      <td>40.751726</td>
      <td>-73.987535</td>
      <td>445</td>
      <td>E 10 St &amp; Avenue A</td>
      <td>40.727408</td>
      <td>-73.981420</td>
      <td>23288</td>
      <td>Subscriber</td>
      <td>1977.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>8</th>
      <td>255</td>
      <td>2017-01-01 00:05:47</td>
      <td>2017-01-01 00:10:02</td>
      <td>430</td>
      <td>York St &amp; Jay St</td>
      <td>40.701485</td>
      <td>-73.986569</td>
      <td>242</td>
      <td>Carlton Ave &amp; Flushing Ave</td>
      <td>40.697787</td>
      <td>-73.973736</td>
      <td>25041</td>
      <td>Subscriber</td>
      <td>1989.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>634</td>
      <td>2017-01-01 00:07:34</td>
      <td>2017-01-01 00:18:08</td>
      <td>3165</td>
      <td>Central Park West &amp; W 72 St</td>
      <td>40.775794</td>
      <td>-73.976206</td>
      <td>3164</td>
      <td>Columbus Ave &amp; W 72 St</td>
      <td>40.777057</td>
      <td>-73.978985</td>
      <td>16311</td>
      <td>Subscriber</td>
      <td>1980.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1081</td>
      <td>2017-01-01 00:07:49</td>
      <td>2017-01-01 00:25:50</td>
      <td>528</td>
      <td>2 Ave &amp; E 31 St</td>
      <td>40.742909</td>
      <td>-73.977061</td>
      <td>526</td>
      <td>E 33 St &amp; 5 Ave</td>
      <td>40.747659</td>
      <td>-73.984907</td>
      <td>26138</td>
      <td>Subscriber</td>
      <td>1993.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>479</td>
      <td>2017-01-01 00:08:00</td>
      <td>2017-01-01 00:15:59</td>
      <td>474</td>
      <td>5 Ave &amp; E 29 St</td>
      <td>40.745168</td>
      <td>-73.986831</td>
      <td>3259</td>
      <td>9 Ave &amp; W 28 St</td>
      <td>40.749370</td>
      <td>-73.999234</td>
      <td>19728</td>
      <td>Subscriber</td>
      <td>1973.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2005</td>
      <td>2017-01-01 00:05:57</td>
      <td>2017-01-01 00:39:23</td>
      <td>524</td>
      <td>W 43 St &amp; 6 Ave</td>
      <td>40.755273</td>
      <td>-73.983169</td>
      <td>3325</td>
      <td>E 95 St &amp; 3 Ave</td>
      <td>40.784903</td>
      <td>-73.950503</td>
      <td>17171</td>
      <td>Subscriber</td>
      <td>1992.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>13</th>
      <td>738</td>
      <td>2017-01-01 00:08:50</td>
      <td>2017-01-01 00:21:09</td>
      <td>297</td>
      <td>E 15 St &amp; 3 Ave</td>
      <td>40.734232</td>
      <td>-73.986923</td>
      <td>355</td>
      <td>Bayard St &amp; Baxter St</td>
      <td>40.716021</td>
      <td>-73.999744</td>
      <td>23874</td>
      <td>Subscriber</td>
      <td>1996.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>901</td>
      <td>2017-01-01 00:09:18</td>
      <td>2017-01-01 00:24:20</td>
      <td>515</td>
      <td>W 43 St &amp; 10 Ave</td>
      <td>40.760094</td>
      <td>-73.994618</td>
      <td>3428</td>
      <td>8 Ave &amp; W 16 St</td>
      <td>40.740983</td>
      <td>-74.001702</td>
      <td>26501</td>
      <td>Subscriber</td>
      <td>1964.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>1246</td>
      <td>2017-01-01 00:09:19</td>
      <td>2017-01-01 00:30:06</td>
      <td>3172</td>
      <td>W 74 St &amp; Columbus Ave</td>
      <td>40.778567</td>
      <td>-73.977550</td>
      <td>3163</td>
      <td>Central Park West &amp; W 68 St</td>
      <td>40.773407</td>
      <td>-73.977825</td>
      <td>20845</td>
      <td>Subscriber</td>
      <td>1977.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>899</td>
      <td>2017-01-01 00:09:20</td>
      <td>2017-01-01 00:24:19</td>
      <td>515</td>
      <td>W 43 St &amp; 10 Ave</td>
      <td>40.760094</td>
      <td>-73.994618</td>
      <td>3428</td>
      <td>8 Ave &amp; W 16 St</td>
      <td>40.740983</td>
      <td>-74.001702</td>
      <td>15597</td>
      <td>Subscriber</td>
      <td>1970.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>17</th>
      <td>1504</td>
      <td>2017-01-01 00:09:29</td>
      <td>2017-01-01 00:34:34</td>
      <td>423</td>
      <td>W 54 St &amp; 9 Ave</td>
      <td>40.765849</td>
      <td>-73.986905</td>
      <td>3263</td>
      <td>Cooper Square &amp; E 7 St</td>
      <td>40.729236</td>
      <td>-73.990868</td>
      <td>17810</td>
      <td>Subscriber</td>
      <td>1994.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>759</td>
      <td>2017-01-01 00:09:30</td>
      <td>2017-01-01 00:22:09</td>
      <td>267</td>
      <td>Broadway &amp; W 36 St</td>
      <td>40.750977</td>
      <td>-73.987654</td>
      <td>520</td>
      <td>W 52 St &amp; 5 Ave</td>
      <td>40.759923</td>
      <td>-73.976485</td>
      <td>27279</td>
      <td>Customer</td>
      <td>NaN</td>
      <td>0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>1231</td>
      <td>2017-01-01 00:09:59</td>
      <td>2017-01-01 00:30:31</td>
      <td>369</td>
      <td>Washington Pl &amp; 6 Ave</td>
      <td>40.732241</td>
      <td>-74.000264</td>
      <td>306</td>
      <td>Cliff St &amp; Fulton St</td>
      <td>40.708235</td>
      <td>-74.005301</td>
      <td>21128</td>
      <td>Subscriber</td>
      <td>1969.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>20</th>
      <td>351</td>
      <td>2017-01-01 00:10:11</td>
      <td>2017-01-01 00:16:02</td>
      <td>3139</td>
      <td>E 72 St &amp; Park Ave</td>
      <td>40.771183</td>
      <td>-73.964094</td>
      <td>3146</td>
      <td>E 81 St &amp; 3 Ave</td>
      <td>40.775730</td>
      <td>-73.956753</td>
      <td>26491</td>
      <td>Subscriber</td>
      <td>1984.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>21</th>
      <td>229</td>
      <td>2017-01-01 00:10:50</td>
      <td>2017-01-01 00:14:40</td>
      <td>279</td>
      <td>Peck Slip &amp; Front St</td>
      <td>40.707873</td>
      <td>-74.001670</td>
      <td>308</td>
      <td>St James Pl &amp; Oliver St</td>
      <td>40.713079</td>
      <td>-73.998512</td>
      <td>18417</td>
      <td>Subscriber</td>
      <td>1974.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>22</th>
      <td>570</td>
      <td>2017-01-01 00:10:50</td>
      <td>2017-01-01 00:20:20</td>
      <td>301</td>
      <td>E 2 St &amp; Avenue B</td>
      <td>40.722174</td>
      <td>-73.983688</td>
      <td>301</td>
      <td>E 2 St &amp; Avenue B</td>
      <td>40.722174</td>
      <td>-73.983688</td>
      <td>21400</td>
      <td>Subscriber</td>
      <td>1996.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>23</th>
      <td>207</td>
      <td>2017-01-01 00:10:53</td>
      <td>2017-01-01 00:14:20</td>
      <td>128</td>
      <td>MacDougal St &amp; Prince St</td>
      <td>40.727103</td>
      <td>-74.002971</td>
      <td>229</td>
      <td>Great Jones St</td>
      <td>40.727434</td>
      <td>-73.993790</td>
      <td>26577</td>
      <td>Subscriber</td>
      <td>1991.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>24</th>
      <td>6370</td>
      <td>2017-01-01 00:11:34</td>
      <td>2017-01-01 01:57:44</td>
      <td>449</td>
      <td>W 52 St &amp; 9 Ave</td>
      <td>40.764618</td>
      <td>-73.987895</td>
      <td>524</td>
      <td>W 43 St &amp; 6 Ave</td>
      <td>40.755273</td>
      <td>-73.983169</td>
      <td>15603</td>
      <td>Customer</td>
      <td>NaN</td>
      <td>0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>6357</td>
      <td>2017-01-01 00:11:44</td>
      <td>2017-01-01 01:57:42</td>
      <td>449</td>
      <td>W 52 St &amp; 9 Ave</td>
      <td>40.764618</td>
      <td>-73.987895</td>
      <td>524</td>
      <td>W 43 St &amp; 6 Ave</td>
      <td>40.755273</td>
      <td>-73.983169</td>
      <td>16373</td>
      <td>Customer</td>
      <td>NaN</td>
      <td>0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>6330</td>
      <td>2017-01-01 00:12:13</td>
      <td>2017-01-01 01:57:43</td>
      <td>449</td>
      <td>W 52 St &amp; 9 Ave</td>
      <td>40.764618</td>
      <td>-73.987895</td>
      <td>524</td>
      <td>W 43 St &amp; 6 Ave</td>
      <td>40.755273</td>
      <td>-73.983169</td>
      <td>17438</td>
      <td>Customer</td>
      <td>NaN</td>
      <td>0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1342</td>
      <td>2017-01-01 00:12:16</td>
      <td>2017-01-01 00:34:38</td>
      <td>153</td>
      <td>E 40 St &amp; 5 Ave</td>
      <td>40.752062</td>
      <td>-73.981632</td>
      <td>428</td>
      <td>E 3 St &amp; 1 Ave</td>
      <td>40.724677</td>
      <td>-73.987834</td>
      <td>25023</td>
      <td>Subscriber</td>
      <td>1968.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1173</td>
      <td>2017-01-01 00:12:40</td>
      <td>2017-01-01 00:32:14</td>
      <td>368</td>
      <td>Carmine St &amp; 6 Ave</td>
      <td>40.730386</td>
      <td>-74.002150</td>
      <td>524</td>
      <td>W 43 St &amp; 6 Ave</td>
      <td>40.755273</td>
      <td>-73.983169</td>
      <td>26003</td>
      <td>Subscriber</td>
      <td>1991.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>29</th>
      <td>1386</td>
      <td>2017-01-01 00:12:55</td>
      <td>2017-01-01 00:36:02</td>
      <td>513</td>
      <td>W 56 St &amp; 10 Ave</td>
      <td>40.768254</td>
      <td>-73.988639</td>
      <td>494</td>
      <td>W 26 St &amp; 8 Ave</td>
      <td>40.747348</td>
      <td>-73.997236</td>
      <td>18569</td>
      <td>Subscriber</td>
      <td>1986.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>16364627</th>
      <td>1287</td>
      <td>2017-12-31 23:40:35</td>
      <td>2018-01-01 00:02:02</td>
      <td>531</td>
      <td>Forsyth St &amp; Broome St</td>
      <td>40.718939</td>
      <td>-73.992663</td>
      <td>498</td>
      <td>Broadway &amp; W 32 St</td>
      <td>40.748549</td>
      <td>-73.988084</td>
      <td>19064</td>
      <td>Subscriber</td>
      <td>1983.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364628</th>
      <td>1279</td>
      <td>2017-12-31 23:40:35</td>
      <td>2018-01-01 00:01:55</td>
      <td>531</td>
      <td>Forsyth St &amp; Broome St</td>
      <td>40.718939</td>
      <td>-73.992663</td>
      <td>498</td>
      <td>Broadway &amp; W 32 St</td>
      <td>40.748549</td>
      <td>-73.988084</td>
      <td>32939</td>
      <td>Subscriber</td>
      <td>1983.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16364629</th>
      <td>482</td>
      <td>2017-12-31 23:40:38</td>
      <td>2017-12-31 23:48:41</td>
      <td>379</td>
      <td>W 31 St &amp; 7 Ave</td>
      <td>40.749156</td>
      <td>-73.991600</td>
      <td>507</td>
      <td>E 25 St &amp; 2 Ave</td>
      <td>40.739126</td>
      <td>-73.979738</td>
      <td>16313</td>
      <td>Subscriber</td>
      <td>1993.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364630</th>
      <td>1303</td>
      <td>2017-12-31 23:40:49</td>
      <td>2018-01-01 00:02:33</td>
      <td>531</td>
      <td>Forsyth St &amp; Broome St</td>
      <td>40.718939</td>
      <td>-73.992663</td>
      <td>498</td>
      <td>Broadway &amp; W 32 St</td>
      <td>40.748549</td>
      <td>-73.988084</td>
      <td>28788</td>
      <td>Subscriber</td>
      <td>1987.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364631</th>
      <td>322</td>
      <td>2017-12-31 23:41:35</td>
      <td>2017-12-31 23:46:58</td>
      <td>499</td>
      <td>Broadway &amp; W 60 St</td>
      <td>40.769155</td>
      <td>-73.981918</td>
      <td>3165</td>
      <td>Central Park West &amp; W 72 St</td>
      <td>40.775794</td>
      <td>-73.976206</td>
      <td>19080</td>
      <td>Subscriber</td>
      <td>1988.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364632</th>
      <td>1461</td>
      <td>2017-12-31 23:42:45</td>
      <td>2018-01-01 00:07:07</td>
      <td>3135</td>
      <td>E 75 St &amp; 3 Ave</td>
      <td>40.771129</td>
      <td>-73.957723</td>
      <td>3135</td>
      <td>E 75 St &amp; 3 Ave</td>
      <td>40.771129</td>
      <td>-73.957723</td>
      <td>33034</td>
      <td>Subscriber</td>
      <td>1968.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364633</th>
      <td>257</td>
      <td>2017-12-31 23:43:23</td>
      <td>2017-12-31 23:47:40</td>
      <td>349</td>
      <td>Rivington St &amp; Ridge St</td>
      <td>40.718502</td>
      <td>-73.983299</td>
      <td>401</td>
      <td>Allen St &amp; Rivington St</td>
      <td>40.720196</td>
      <td>-73.989978</td>
      <td>30823</td>
      <td>Subscriber</td>
      <td>1993.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364634</th>
      <td>347</td>
      <td>2017-12-31 23:43:57</td>
      <td>2017-12-31 23:49:44</td>
      <td>3637</td>
      <td>Fulton St &amp; Waverly Ave</td>
      <td>40.683239</td>
      <td>-73.965996</td>
      <td>120</td>
      <td>Lexington Ave &amp; Classon Ave</td>
      <td>40.686768</td>
      <td>-73.959282</td>
      <td>25776</td>
      <td>Subscriber</td>
      <td>1983.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364635</th>
      <td>87</td>
      <td>2017-12-31 23:44:23</td>
      <td>2017-12-31 23:45:50</td>
      <td>515</td>
      <td>W 43 St &amp; 10 Ave</td>
      <td>40.760094</td>
      <td>-73.994618</td>
      <td>3236</td>
      <td>W 42 St &amp; Dyer Ave</td>
      <td>40.758985</td>
      <td>-73.993800</td>
      <td>29177</td>
      <td>Subscriber</td>
      <td>1967.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364636</th>
      <td>177</td>
      <td>2017-12-31 23:45:29</td>
      <td>2017-12-31 23:48:26</td>
      <td>3429</td>
      <td>Hanson Pl &amp; Ashland Pl</td>
      <td>40.685068</td>
      <td>-73.977908</td>
      <td>3419</td>
      <td>Douglass St &amp; 4 Ave</td>
      <td>40.679279</td>
      <td>-73.981540</td>
      <td>33045</td>
      <td>Subscriber</td>
      <td>1989.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364637</th>
      <td>225</td>
      <td>2017-12-31 23:45:43</td>
      <td>2017-12-31 23:49:29</td>
      <td>3260</td>
      <td>Mercer St &amp; Bleecker St</td>
      <td>40.727064</td>
      <td>-73.996621</td>
      <td>403</td>
      <td>E 2 St &amp; 2 Ave</td>
      <td>40.725029</td>
      <td>-73.990697</td>
      <td>31102</td>
      <td>Subscriber</td>
      <td>1987.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364638</th>
      <td>531</td>
      <td>2017-12-31 23:46:10</td>
      <td>2017-12-31 23:55:02</td>
      <td>423</td>
      <td>W 54 St &amp; 9 Ave</td>
      <td>40.765849</td>
      <td>-73.986905</td>
      <td>448</td>
      <td>W 37 St &amp; 10 Ave</td>
      <td>40.756604</td>
      <td>-73.997901</td>
      <td>19007</td>
      <td>Subscriber</td>
      <td>1955.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16364639</th>
      <td>184</td>
      <td>2017-12-31 23:46:15</td>
      <td>2017-12-31 23:49:20</td>
      <td>3431</td>
      <td>E 35 St &amp; 3 Ave</td>
      <td>40.746524</td>
      <td>-73.977885</td>
      <td>472</td>
      <td>E 32 St &amp; Park Ave</td>
      <td>40.745712</td>
      <td>-73.981948</td>
      <td>33182</td>
      <td>Subscriber</td>
      <td>1970.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364640</th>
      <td>189</td>
      <td>2017-12-31 23:46:43</td>
      <td>2017-12-31 23:49:52</td>
      <td>504</td>
      <td>1 Ave &amp; E 16 St</td>
      <td>40.732219</td>
      <td>-73.981656</td>
      <td>487</td>
      <td>E 20 St &amp; FDR Drive</td>
      <td>40.733143</td>
      <td>-73.975739</td>
      <td>31315</td>
      <td>Subscriber</td>
      <td>1986.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364641</th>
      <td>313</td>
      <td>2017-12-31 23:47:24</td>
      <td>2017-12-31 23:52:37</td>
      <td>513</td>
      <td>W 56 St &amp; 10 Ave</td>
      <td>40.768254</td>
      <td>-73.988639</td>
      <td>3236</td>
      <td>W 42 St &amp; Dyer Ave</td>
      <td>40.758985</td>
      <td>-73.993800</td>
      <td>26542</td>
      <td>Subscriber</td>
      <td>1984.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364642</th>
      <td>788</td>
      <td>2017-12-31 23:47:55</td>
      <td>2018-01-01 00:01:04</td>
      <td>2008</td>
      <td>Little West St &amp; 1 Pl</td>
      <td>40.705693</td>
      <td>-74.016777</td>
      <td>249</td>
      <td>Harrison St &amp; Hudson St</td>
      <td>40.718710</td>
      <td>-74.009001</td>
      <td>30785</td>
      <td>Subscriber</td>
      <td>1985.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364643</th>
      <td>263</td>
      <td>2017-12-31 23:48:35</td>
      <td>2017-12-31 23:52:58</td>
      <td>3086</td>
      <td>Graham Ave &amp; Conselyea St</td>
      <td>40.715143</td>
      <td>-73.944507</td>
      <td>3106</td>
      <td>Driggs Ave &amp; N Henry St</td>
      <td>40.723250</td>
      <td>-73.943080</td>
      <td>31022</td>
      <td>Subscriber</td>
      <td>1981.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>16364644</th>
      <td>487</td>
      <td>2017-12-31 23:48:39</td>
      <td>2017-12-31 23:56:47</td>
      <td>3077</td>
      <td>Stagg St &amp; Union Ave</td>
      <td>40.708771</td>
      <td>-73.950953</td>
      <td>389</td>
      <td>Broadway &amp; Berry St</td>
      <td>40.710446</td>
      <td>-73.965251</td>
      <td>25366</td>
      <td>Subscriber</td>
      <td>1985.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364645</th>
      <td>1323</td>
      <td>2017-12-31 23:48:48</td>
      <td>2018-01-01 00:10:52</td>
      <td>236</td>
      <td>St Marks Pl &amp; 2 Ave</td>
      <td>40.728419</td>
      <td>-73.987140</td>
      <td>430</td>
      <td>York St &amp; Jay St</td>
      <td>40.701485</td>
      <td>-73.986569</td>
      <td>31643</td>
      <td>Subscriber</td>
      <td>1996.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364646</th>
      <td>952</td>
      <td>2017-12-31 23:49:16</td>
      <td>2018-01-01 00:05:08</td>
      <td>455</td>
      <td>1 Ave &amp; E 44 St</td>
      <td>40.750020</td>
      <td>-73.969053</td>
      <td>3238</td>
      <td>E 80 St &amp; 2 Ave</td>
      <td>40.773914</td>
      <td>-73.954395</td>
      <td>31959</td>
      <td>Subscriber</td>
      <td>1953.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364647</th>
      <td>411</td>
      <td>2017-12-31 23:49:34</td>
      <td>2017-12-31 23:56:25</td>
      <td>3288</td>
      <td>E 88 St &amp; 1 Ave</td>
      <td>40.778301</td>
      <td>-73.948813</td>
      <td>3292</td>
      <td>5 Ave &amp; E 93 St</td>
      <td>40.785785</td>
      <td>-73.957481</td>
      <td>26930</td>
      <td>Subscriber</td>
      <td>1991.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364648</th>
      <td>433</td>
      <td>2017-12-31 23:49:36</td>
      <td>2017-12-31 23:56:50</td>
      <td>3288</td>
      <td>E 88 St &amp; 1 Ave</td>
      <td>40.778301</td>
      <td>-73.948813</td>
      <td>3292</td>
      <td>5 Ave &amp; E 93 St</td>
      <td>40.785785</td>
      <td>-73.957481</td>
      <td>31549</td>
      <td>Subscriber</td>
      <td>1990.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364649</th>
      <td>606</td>
      <td>2017-12-31 23:50:04</td>
      <td>2018-01-01 00:00:11</td>
      <td>515</td>
      <td>W 43 St &amp; 10 Ave</td>
      <td>40.760094</td>
      <td>-73.994618</td>
      <td>494</td>
      <td>W 26 St &amp; 8 Ave</td>
      <td>40.747348</td>
      <td>-73.997236</td>
      <td>32812</td>
      <td>Subscriber</td>
      <td>1967.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364650</th>
      <td>1088</td>
      <td>2017-12-31 23:50:08</td>
      <td>2018-01-01 00:08:16</td>
      <td>296</td>
      <td>Division St &amp; Bowery</td>
      <td>40.714131</td>
      <td>-73.997047</td>
      <td>174</td>
      <td>E 25 St &amp; 1 Ave</td>
      <td>40.738177</td>
      <td>-73.977387</td>
      <td>24875</td>
      <td>Subscriber</td>
      <td>1979.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16364651</th>
      <td>429</td>
      <td>2017-12-31 23:52:25</td>
      <td>2017-12-31 23:59:34</td>
      <td>447</td>
      <td>8 Ave &amp; W 52 St</td>
      <td>40.763707</td>
      <td>-73.985162</td>
      <td>3172</td>
      <td>W 74 St &amp; Columbus Ave</td>
      <td>40.778567</td>
      <td>-73.977550</td>
      <td>29712</td>
      <td>Subscriber</td>
      <td>1982.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364652</th>
      <td>397</td>
      <td>2017-12-31 23:54:22</td>
      <td>2018-01-01 00:01:00</td>
      <td>3417</td>
      <td>Baltic St &amp; 5 Ave</td>
      <td>40.679577</td>
      <td>-73.978550</td>
      <td>3418</td>
      <td>Plaza St West &amp; Flatbush Ave</td>
      <td>40.675021</td>
      <td>-73.971115</td>
      <td>30841</td>
      <td>Subscriber</td>
      <td>1957.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16364653</th>
      <td>332</td>
      <td>2017-12-31 23:54:44</td>
      <td>2018-01-01 00:00:16</td>
      <td>3236</td>
      <td>W 42 St &amp; Dyer Ave</td>
      <td>40.758985</td>
      <td>-73.993800</td>
      <td>513</td>
      <td>W 56 St &amp; 10 Ave</td>
      <td>40.768254</td>
      <td>-73.988639</td>
      <td>30417</td>
      <td>Subscriber</td>
      <td>1984.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364654</th>
      <td>565</td>
      <td>2017-12-31 23:56:07</td>
      <td>2018-01-01 00:05:33</td>
      <td>254</td>
      <td>W 11 St &amp; 6 Ave</td>
      <td>40.735324</td>
      <td>-73.998004</td>
      <td>411</td>
      <td>E 6 St &amp; Avenue D</td>
      <td>40.722281</td>
      <td>-73.976687</td>
      <td>16125</td>
      <td>Subscriber</td>
      <td>1991.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16364655</th>
      <td>1659</td>
      <td>2017-12-31 23:57:16</td>
      <td>2018-01-01 00:24:56</td>
      <td>495</td>
      <td>W 47 St &amp; 10 Ave</td>
      <td>40.762699</td>
      <td>-73.993012</td>
      <td>3163</td>
      <td>Central Park West &amp; W 68 St</td>
      <td>40.773407</td>
      <td>-73.977825</td>
      <td>33328</td>
      <td>Subscriber</td>
      <td>1988.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16364656</th>
      <td>1279</td>
      <td>2017-12-31 23:58:56</td>
      <td>2018-01-01 00:20:16</td>
      <td>3135</td>
      <td>E 75 St &amp; 3 Ave</td>
      <td>40.771129</td>
      <td>-73.957723</td>
      <td>3143</td>
      <td>5 Ave &amp; E 78 St</td>
      <td>40.776321</td>
      <td>-73.964274</td>
      <td>31023</td>
      <td>Subscriber</td>
      <td>1968.0</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
<p>16364657 rows × 15 columns</p>
</div>




```python
citi_bikes_2017.count()
```




    Trip Duration              16364657
    Start Time                 16364657
    Stop Time                  16364657
    Start Station ID           16364657
    Start Station Name         16364657
    Start Station Latitude     16364657
    Start Station Longitude    16364657
    End Station ID             16364657
    End Station Name           16364657
    End Station Latitude       16364657
    End Station Longitude      16364657
    Bike ID                    16364657
    User Type                  16348748
    Birth Year                 14734322
    Gender                     16364657
    dtype: int64




```python
citi_bikes_2017.to_csv("ny_citi_bikes_2017.csv", index=False)
```
