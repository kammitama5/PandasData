

```python
import pandas as pd
import numpy as np
df = pd.read_csv('census.csv')
df = df[df['SUMLEV'] == 50]
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SUMLEV</th>
      <th>REGION</th>
      <th>DIVISION</th>
      <th>STATE</th>
      <th>COUNTY</th>
      <th>STNAME</th>
      <th>CTYNAME</th>
      <th>CENSUS2010POP</th>
      <th>ESTIMATESBASE2010</th>
      <th>POPESTIMATE2010</th>
      <th>...</th>
      <th>RDOMESTICMIG2011</th>
      <th>RDOMESTICMIG2012</th>
      <th>RDOMESTICMIG2013</th>
      <th>RDOMESTICMIG2014</th>
      <th>RDOMESTICMIG2015</th>
      <th>RNETMIG2011</th>
      <th>RNETMIG2012</th>
      <th>RNETMIG2013</th>
      <th>RNETMIG2014</th>
      <th>RNETMIG2015</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>Alabama</td>
      <td>Autauga County</td>
      <td>54571</td>
      <td>54571</td>
      <td>54660</td>
      <td>...</td>
      <td>7.242091</td>
      <td>-2.915927</td>
      <td>-3.012349</td>
      <td>2.265971</td>
      <td>-2.530799</td>
      <td>7.606016</td>
      <td>-2.626146</td>
      <td>-2.722002</td>
      <td>2.592270</td>
      <td>-2.187333</td>
    </tr>
    <tr>
      <th>2</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>Alabama</td>
      <td>Baldwin County</td>
      <td>182265</td>
      <td>182265</td>
      <td>183193</td>
      <td>...</td>
      <td>14.832960</td>
      <td>17.647293</td>
      <td>21.845705</td>
      <td>19.243287</td>
      <td>17.197872</td>
      <td>15.844176</td>
      <td>18.559627</td>
      <td>22.727626</td>
      <td>20.317142</td>
      <td>18.293499</td>
    </tr>
    <tr>
      <th>3</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>5</td>
      <td>Alabama</td>
      <td>Barbour County</td>
      <td>27457</td>
      <td>27457</td>
      <td>27341</td>
      <td>...</td>
      <td>-4.728132</td>
      <td>-2.500690</td>
      <td>-7.056824</td>
      <td>-3.904217</td>
      <td>-10.543299</td>
      <td>-4.874741</td>
      <td>-2.758113</td>
      <td>-7.167664</td>
      <td>-3.978583</td>
      <td>-10.543299</td>
    </tr>
    <tr>
      <th>4</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>7</td>
      <td>Alabama</td>
      <td>Bibb County</td>
      <td>22915</td>
      <td>22919</td>
      <td>22861</td>
      <td>...</td>
      <td>-5.527043</td>
      <td>-5.068871</td>
      <td>-6.201001</td>
      <td>-0.177537</td>
      <td>0.177258</td>
      <td>-5.088389</td>
      <td>-4.363636</td>
      <td>-5.403729</td>
      <td>0.754533</td>
      <td>1.107861</td>
    </tr>
    <tr>
      <th>5</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>9</td>
      <td>Alabama</td>
      <td>Blount County</td>
      <td>57322</td>
      <td>57322</td>
      <td>57373</td>
      <td>...</td>
      <td>1.807375</td>
      <td>-1.177622</td>
      <td>-1.748766</td>
      <td>-2.062535</td>
      <td>-1.369970</td>
      <td>1.859511</td>
      <td>-0.848580</td>
      <td>-1.402476</td>
      <td>-1.577232</td>
      <td>-0.884411</td>
    </tr>
    <tr>
      <th>6</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>11</td>
      <td>Alabama</td>
      <td>Bullock County</td>
      <td>10914</td>
      <td>10915</td>
      <td>10887</td>
      <td>...</td>
      <td>-30.953709</td>
      <td>-5.180127</td>
      <td>-1.130263</td>
      <td>14.354290</td>
      <td>-16.167247</td>
      <td>-29.001673</td>
      <td>-2.825524</td>
      <td>1.507017</td>
      <td>17.243790</td>
      <td>-13.193961</td>
    </tr>
    <tr>
      <th>7</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>13</td>
      <td>Alabama</td>
      <td>Butler County</td>
      <td>20947</td>
      <td>20946</td>
      <td>20944</td>
      <td>...</td>
      <td>-14.032727</td>
      <td>-11.684234</td>
      <td>-5.655413</td>
      <td>1.085428</td>
      <td>-6.529805</td>
      <td>-13.936612</td>
      <td>-11.586865</td>
      <td>-5.557058</td>
      <td>1.184103</td>
      <td>-6.430868</td>
    </tr>
    <tr>
      <th>8</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>15</td>
      <td>Alabama</td>
      <td>Calhoun County</td>
      <td>118572</td>
      <td>118586</td>
      <td>118437</td>
      <td>...</td>
      <td>-6.155670</td>
      <td>-4.611706</td>
      <td>-5.524649</td>
      <td>-4.463211</td>
      <td>-3.376322</td>
      <td>-5.791579</td>
      <td>-4.092677</td>
      <td>-5.062836</td>
      <td>-3.912834</td>
      <td>-2.806406</td>
    </tr>
    <tr>
      <th>9</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>17</td>
      <td>Alabama</td>
      <td>Chambers County</td>
      <td>34215</td>
      <td>34170</td>
      <td>34098</td>
      <td>...</td>
      <td>-2.731639</td>
      <td>3.849092</td>
      <td>2.872721</td>
      <td>-2.287222</td>
      <td>1.349468</td>
      <td>-1.821092</td>
      <td>4.701181</td>
      <td>3.781439</td>
      <td>-1.290228</td>
      <td>2.346901</td>
    </tr>
    <tr>
      <th>10</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>19</td>
      <td>Alabama</td>
      <td>Cherokee County</td>
      <td>25989</td>
      <td>25986</td>
      <td>25976</td>
      <td>...</td>
      <td>6.339327</td>
      <td>1.113180</td>
      <td>5.488706</td>
      <td>-0.076806</td>
      <td>-3.239866</td>
      <td>6.416167</td>
      <td>1.420264</td>
      <td>5.757384</td>
      <td>0.230419</td>
      <td>-2.931307</td>
    </tr>
    <tr>
      <th>11</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>21</td>
      <td>Alabama</td>
      <td>Chilton County</td>
      <td>43643</td>
      <td>43631</td>
      <td>43665</td>
      <td>...</td>
      <td>-1.372935</td>
      <td>-2.653369</td>
      <td>0.480044</td>
      <td>0.456017</td>
      <td>-2.253483</td>
      <td>-0.823761</td>
      <td>-2.447504</td>
      <td>0.868651</td>
      <td>0.957636</td>
      <td>-1.752709</td>
    </tr>
    <tr>
      <th>12</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>23</td>
      <td>Alabama</td>
      <td>Choctaw County</td>
      <td>13859</td>
      <td>13858</td>
      <td>13841</td>
      <td>...</td>
      <td>-15.455274</td>
      <td>-0.737028</td>
      <td>-8.766391</td>
      <td>-1.274984</td>
      <td>-5.291205</td>
      <td>-15.528177</td>
      <td>-0.737028</td>
      <td>-8.766391</td>
      <td>-1.274984</td>
      <td>-5.291205</td>
    </tr>
    <tr>
      <th>13</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>25</td>
      <td>Alabama</td>
      <td>Clarke County</td>
      <td>25833</td>
      <td>25840</td>
      <td>25767</td>
      <td>...</td>
      <td>-6.194363</td>
      <td>-17.667705</td>
      <td>-0.318345</td>
      <td>-8.686428</td>
      <td>-5.613667</td>
      <td>-6.077488</td>
      <td>-17.509958</td>
      <td>-0.159172</td>
      <td>-8.486280</td>
      <td>-5.411736</td>
    </tr>
    <tr>
      <th>14</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>27</td>
      <td>Alabama</td>
      <td>Clay County</td>
      <td>13932</td>
      <td>13932</td>
      <td>13880</td>
      <td>...</td>
      <td>-10.744102</td>
      <td>-13.345130</td>
      <td>4.902871</td>
      <td>5.702648</td>
      <td>3.912450</td>
      <td>-10.816697</td>
      <td>-13.345130</td>
      <td>4.977157</td>
      <td>5.776708</td>
      <td>3.986270</td>
    </tr>
    <tr>
      <th>15</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>29</td>
      <td>Alabama</td>
      <td>Cleburne County</td>
      <td>14972</td>
      <td>14972</td>
      <td>14973</td>
      <td>...</td>
      <td>-3.673524</td>
      <td>-5.151880</td>
      <td>7.345821</td>
      <td>3.654485</td>
      <td>-3.123961</td>
      <td>-3.673524</td>
      <td>-5.151880</td>
      <td>7.345821</td>
      <td>3.654485</td>
      <td>-3.123961</td>
    </tr>
    <tr>
      <th>16</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>31</td>
      <td>Alabama</td>
      <td>Coffee County</td>
      <td>49948</td>
      <td>49948</td>
      <td>50177</td>
      <td>...</td>
      <td>0.377640</td>
      <td>7.675579</td>
      <td>-13.146535</td>
      <td>-3.602859</td>
      <td>2.214774</td>
      <td>2.166460</td>
      <td>11.513368</td>
      <td>-10.438741</td>
      <td>-0.767822</td>
      <td>5.350738</td>
    </tr>
    <tr>
      <th>17</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>33</td>
      <td>Alabama</td>
      <td>Colbert County</td>
      <td>54428</td>
      <td>54428</td>
      <td>54514</td>
      <td>...</td>
      <td>-0.073423</td>
      <td>1.065051</td>
      <td>1.762390</td>
      <td>1.835688</td>
      <td>-0.110260</td>
      <td>0.513964</td>
      <td>1.469035</td>
      <td>2.276420</td>
      <td>2.533249</td>
      <td>0.588052</td>
    </tr>
    <tr>
      <th>18</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>35</td>
      <td>Alabama</td>
      <td>Conecuh County</td>
      <td>13228</td>
      <td>13228</td>
      <td>13208</td>
      <td>...</td>
      <td>-4.861559</td>
      <td>-7.504690</td>
      <td>-6.107224</td>
      <td>-14.645416</td>
      <td>2.684140</td>
      <td>-4.861559</td>
      <td>-7.504690</td>
      <td>-6.107224</td>
      <td>-14.645416</td>
      <td>2.684140</td>
    </tr>
    <tr>
      <th>19</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>37</td>
      <td>Alabama</td>
      <td>Coosa County</td>
      <td>11539</td>
      <td>11758</td>
      <td>11758</td>
      <td>...</td>
      <td>-33.930581</td>
      <td>-10.291443</td>
      <td>-4.313831</td>
      <td>-22.958017</td>
      <td>-5.387581</td>
      <td>-34.017138</td>
      <td>-10.380162</td>
      <td>-4.403703</td>
      <td>-23.049483</td>
      <td>-5.387581</td>
    </tr>
    <tr>
      <th>20</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>39</td>
      <td>Alabama</td>
      <td>Covington County</td>
      <td>37765</td>
      <td>37765</td>
      <td>37796</td>
      <td>...</td>
      <td>6.696899</td>
      <td>-4.612668</td>
      <td>0.740271</td>
      <td>3.697932</td>
      <td>-0.316945</td>
      <td>6.881460</td>
      <td>-4.559952</td>
      <td>0.793147</td>
      <td>3.750759</td>
      <td>-0.264121</td>
    </tr>
    <tr>
      <th>21</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>41</td>
      <td>Alabama</td>
      <td>Crenshaw County</td>
      <td>13906</td>
      <td>13906</td>
      <td>13853</td>
      <td>...</td>
      <td>1.729792</td>
      <td>3.950156</td>
      <td>-1.864936</td>
      <td>3.084648</td>
      <td>3.439504</td>
      <td>2.666763</td>
      <td>5.099293</td>
      <td>-0.502098</td>
      <td>4.734577</td>
      <td>5.087600</td>
    </tr>
    <tr>
      <th>22</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>43</td>
      <td>Alabama</td>
      <td>Cullman County</td>
      <td>80406</td>
      <td>80410</td>
      <td>80473</td>
      <td>...</td>
      <td>-1.404233</td>
      <td>-1.019628</td>
      <td>4.071247</td>
      <td>5.087142</td>
      <td>7.915406</td>
      <td>-1.031427</td>
      <td>-0.634159</td>
      <td>4.542916</td>
      <td>5.593387</td>
      <td>8.417777</td>
    </tr>
    <tr>
      <th>23</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>45</td>
      <td>Alabama</td>
      <td>Dale County</td>
      <td>50251</td>
      <td>50251</td>
      <td>50358</td>
      <td>...</td>
      <td>-10.749798</td>
      <td>-5.277150</td>
      <td>-15.236079</td>
      <td>-11.979785</td>
      <td>-5.107706</td>
      <td>-9.575283</td>
      <td>-0.776637</td>
      <td>-12.640155</td>
      <td>-9.503292</td>
      <td>-1.998668</td>
    </tr>
    <tr>
      <th>24</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>47</td>
      <td>Alabama</td>
      <td>Dallas County</td>
      <td>43820</td>
      <td>43820</td>
      <td>43803</td>
      <td>...</td>
      <td>-15.635599</td>
      <td>-11.308243</td>
      <td>-16.745678</td>
      <td>-9.344789</td>
      <td>-14.687232</td>
      <td>-15.727573</td>
      <td>-11.378047</td>
      <td>-16.792849</td>
      <td>-9.368689</td>
      <td>-14.711389</td>
    </tr>
    <tr>
      <th>25</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>49</td>
      <td>Alabama</td>
      <td>DeKalb County</td>
      <td>71109</td>
      <td>71115</td>
      <td>71142</td>
      <td>...</td>
      <td>0.294677</td>
      <td>-9.302391</td>
      <td>-1.748807</td>
      <td>0.267830</td>
      <td>0.028141</td>
      <td>1.375159</td>
      <td>-8.656001</td>
      <td>-1.029539</td>
      <td>1.198187</td>
      <td>0.956790</td>
    </tr>
    <tr>
      <th>26</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>51</td>
      <td>Alabama</td>
      <td>Elmore County</td>
      <td>79303</td>
      <td>79296</td>
      <td>79465</td>
      <td>...</td>
      <td>3.235576</td>
      <td>0.822717</td>
      <td>1.760531</td>
      <td>-1.507057</td>
      <td>2.067820</td>
      <td>3.674511</td>
      <td>1.558176</td>
      <td>2.306047</td>
      <td>-0.951175</td>
      <td>2.757093</td>
    </tr>
    <tr>
      <th>27</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>53</td>
      <td>Alabama</td>
      <td>Escambia County</td>
      <td>38319</td>
      <td>38319</td>
      <td>38309</td>
      <td>...</td>
      <td>-3.449988</td>
      <td>-3.855889</td>
      <td>-4.822706</td>
      <td>-1.189831</td>
      <td>1.190902</td>
      <td>-3.397716</td>
      <td>-3.803428</td>
      <td>-4.769999</td>
      <td>-1.136950</td>
      <td>1.243830</td>
    </tr>
    <tr>
      <th>28</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>55</td>
      <td>Alabama</td>
      <td>Etowah County</td>
      <td>104430</td>
      <td>104427</td>
      <td>104442</td>
      <td>...</td>
      <td>-1.015919</td>
      <td>2.062637</td>
      <td>-1.931884</td>
      <td>-1.726932</td>
      <td>-2.082234</td>
      <td>-0.632554</td>
      <td>2.446383</td>
      <td>-1.518596</td>
      <td>-1.234901</td>
      <td>-1.588308</td>
    </tr>
    <tr>
      <th>29</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>57</td>
      <td>Alabama</td>
      <td>Fayette County</td>
      <td>17241</td>
      <td>17241</td>
      <td>17231</td>
      <td>...</td>
      <td>-5.015601</td>
      <td>-0.646640</td>
      <td>-3.725937</td>
      <td>0.296745</td>
      <td>-2.797536</td>
      <td>-5.132243</td>
      <td>-0.705426</td>
      <td>-3.785079</td>
      <td>0.237396</td>
      <td>-2.857058</td>
    </tr>
    <tr>
      <th>30</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>59</td>
      <td>Alabama</td>
      <td>Franklin County</td>
      <td>31704</td>
      <td>31709</td>
      <td>31734</td>
      <td>...</td>
      <td>-1.638750</td>
      <td>-5.459394</td>
      <td>-8.043702</td>
      <td>-1.267849</td>
      <td>-2.401719</td>
      <td>0.063029</td>
      <td>-3.471291</td>
      <td>-5.700261</td>
      <td>1.553115</td>
      <td>0.442422</td>
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
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>3162</th>
      <td>50</td>
      <td>2</td>
      <td>3</td>
      <td>55</td>
      <td>129</td>
      <td>Wisconsin</td>
      <td>Washburn County</td>
      <td>15911</td>
      <td>15911</td>
      <td>15930</td>
      <td>...</td>
      <td>-6.873936</td>
      <td>7.338289</td>
      <td>-6.732724</td>
      <td>3.510452</td>
      <td>-5.123279</td>
      <td>-6.747809</td>
      <td>7.464811</td>
      <td>-6.605691</td>
      <td>3.638104</td>
      <td>-4.995197</td>
    </tr>
    <tr>
      <th>3163</th>
      <td>50</td>
      <td>2</td>
      <td>3</td>
      <td>55</td>
      <td>131</td>
      <td>Wisconsin</td>
      <td>Washington County</td>
      <td>131887</td>
      <td>131885</td>
      <td>131967</td>
      <td>...</td>
      <td>-0.794876</td>
      <td>0.785279</td>
      <td>-2.215465</td>
      <td>1.601149</td>
      <td>-0.434498</td>
      <td>-0.431504</td>
      <td>1.162817</td>
      <td>-1.763330</td>
      <td>2.104796</td>
      <td>0.059931</td>
    </tr>
    <tr>
      <th>3164</th>
      <td>50</td>
      <td>2</td>
      <td>3</td>
      <td>55</td>
      <td>133</td>
      <td>Wisconsin</td>
      <td>Waukesha County</td>
      <td>389891</td>
      <td>389938</td>
      <td>390076</td>
      <td>...</td>
      <td>-0.765799</td>
      <td>2.128860</td>
      <td>0.038132</td>
      <td>0.760109</td>
      <td>-0.719858</td>
      <td>0.102448</td>
      <td>3.180527</td>
      <td>1.189727</td>
      <td>2.077633</td>
      <td>0.593567</td>
    </tr>
    <tr>
      <th>3165</th>
      <td>50</td>
      <td>2</td>
      <td>3</td>
      <td>55</td>
      <td>135</td>
      <td>Wisconsin</td>
      <td>Waupaca County</td>
      <td>52410</td>
      <td>52410</td>
      <td>52422</td>
      <td>...</td>
      <td>3.111756</td>
      <td>-2.241873</td>
      <td>6.292687</td>
      <td>-0.441031</td>
      <td>-0.480617</td>
      <td>3.359933</td>
      <td>-2.011937</td>
      <td>6.561277</td>
      <td>-0.134227</td>
      <td>-0.173022</td>
    </tr>
    <tr>
      <th>3166</th>
      <td>50</td>
      <td>2</td>
      <td>3</td>
      <td>55</td>
      <td>137</td>
      <td>Wisconsin</td>
      <td>Waushara County</td>
      <td>24496</td>
      <td>24496</td>
      <td>24506</td>
      <td>...</td>
      <td>4.930022</td>
      <td>-2.404973</td>
      <td>-4.097017</td>
      <td>-4.906711</td>
      <td>-4.397793</td>
      <td>5.174486</td>
      <td>-2.160399</td>
      <td>-3.810226</td>
      <td>-4.535615</td>
      <td>-4.024395</td>
    </tr>
    <tr>
      <th>3167</th>
      <td>50</td>
      <td>2</td>
      <td>3</td>
      <td>55</td>
      <td>139</td>
      <td>Wisconsin</td>
      <td>Winnebago County</td>
      <td>166994</td>
      <td>166994</td>
      <td>167059</td>
      <td>...</td>
      <td>0.316712</td>
      <td>2.889873</td>
      <td>0.833819</td>
      <td>-2.406192</td>
      <td>-4.557985</td>
      <td>0.842573</td>
      <td>3.502335</td>
      <td>1.531624</td>
      <td>-1.545153</td>
      <td>-3.685304</td>
    </tr>
    <tr>
      <th>3168</th>
      <td>50</td>
      <td>2</td>
      <td>3</td>
      <td>55</td>
      <td>141</td>
      <td>Wisconsin</td>
      <td>Wood County</td>
      <td>74749</td>
      <td>74749</td>
      <td>74807</td>
      <td>...</td>
      <td>-4.081523</td>
      <td>-5.019090</td>
      <td>-6.901200</td>
      <td>-5.596471</td>
      <td>-3.958322</td>
      <td>-3.733590</td>
      <td>-4.562809</td>
      <td>-6.442917</td>
      <td>-5.040889</td>
      <td>-3.414223</td>
    </tr>
    <tr>
      <th>3170</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>1</td>
      <td>Wyoming</td>
      <td>Albany County</td>
      <td>36299</td>
      <td>36299</td>
      <td>36428</td>
      <td>...</td>
      <td>3.708956</td>
      <td>2.637812</td>
      <td>-3.544634</td>
      <td>-3.334877</td>
      <td>-9.911169</td>
      <td>6.736119</td>
      <td>6.433032</td>
      <td>0.719587</td>
      <td>1.429233</td>
      <td>-5.166460</td>
    </tr>
    <tr>
      <th>3171</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>3</td>
      <td>Wyoming</td>
      <td>Big Horn County</td>
      <td>11668</td>
      <td>11668</td>
      <td>11672</td>
      <td>...</td>
      <td>4.868258</td>
      <td>2.804930</td>
      <td>16.815908</td>
      <td>-8.026420</td>
      <td>5.095861</td>
      <td>4.868258</td>
      <td>3.144921</td>
      <td>17.236306</td>
      <td>-7.608378</td>
      <td>5.513554</td>
    </tr>
    <tr>
      <th>3172</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>5</td>
      <td>Wyoming</td>
      <td>Campbell County</td>
      <td>46133</td>
      <td>46133</td>
      <td>46244</td>
      <td>...</td>
      <td>-2.843479</td>
      <td>15.601020</td>
      <td>-5.895711</td>
      <td>-8.550911</td>
      <td>10.916963</td>
      <td>-2.649606</td>
      <td>15.558684</td>
      <td>-5.916543</td>
      <td>-8.509402</td>
      <td>10.978525</td>
    </tr>
    <tr>
      <th>3173</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>7</td>
      <td>Wyoming</td>
      <td>Carbon County</td>
      <td>15885</td>
      <td>15885</td>
      <td>15837</td>
      <td>...</td>
      <td>-7.581980</td>
      <td>-13.081441</td>
      <td>3.178134</td>
      <td>-2.970641</td>
      <td>-23.300971</td>
      <td>-7.392431</td>
      <td>-12.636926</td>
      <td>3.623073</td>
      <td>-2.338590</td>
      <td>-22.600668</td>
    </tr>
    <tr>
      <th>3174</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>9</td>
      <td>Wyoming</td>
      <td>Converse County</td>
      <td>13833</td>
      <td>13833</td>
      <td>13826</td>
      <td>...</td>
      <td>-12.847499</td>
      <td>15.493820</td>
      <td>19.035533</td>
      <td>-20.550587</td>
      <td>-0.070403</td>
      <td>-12.774915</td>
      <td>16.502720</td>
      <td>20.093063</td>
      <td>-19.358233</td>
      <td>1.126443</td>
    </tr>
    <tr>
      <th>3175</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>11</td>
      <td>Wyoming</td>
      <td>Crook County</td>
      <td>7083</td>
      <td>7083</td>
      <td>7114</td>
      <td>...</td>
      <td>-1.544618</td>
      <td>-4.202564</td>
      <td>1.397819</td>
      <td>6.378258</td>
      <td>18.629317</td>
      <td>-0.982939</td>
      <td>-3.642222</td>
      <td>2.096729</td>
      <td>7.071547</td>
      <td>19.309219</td>
    </tr>
    <tr>
      <th>3176</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>13</td>
      <td>Wyoming</td>
      <td>Fremont County</td>
      <td>40123</td>
      <td>40123</td>
      <td>40222</td>
      <td>...</td>
      <td>2.747083</td>
      <td>7.782673</td>
      <td>-4.990688</td>
      <td>-12.331633</td>
      <td>-13.673610</td>
      <td>3.093562</td>
      <td>8.027411</td>
      <td>-4.747240</td>
      <td>-12.013555</td>
      <td>-13.352750</td>
    </tr>
    <tr>
      <th>3177</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>15</td>
      <td>Wyoming</td>
      <td>Goshen County</td>
      <td>13249</td>
      <td>13247</td>
      <td>13408</td>
      <td>...</td>
      <td>14.293649</td>
      <td>3.961413</td>
      <td>-8.079028</td>
      <td>-7.017803</td>
      <td>-11.899450</td>
      <td>14.886132</td>
      <td>4.841727</td>
      <td>-6.903896</td>
      <td>-5.761986</td>
      <td>-10.635133</td>
    </tr>
    <tr>
      <th>3178</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>17</td>
      <td>Wyoming</td>
      <td>Hot Springs County</td>
      <td>4812</td>
      <td>4812</td>
      <td>4813</td>
      <td>...</td>
      <td>3.322604</td>
      <td>6.208609</td>
      <td>3.095336</td>
      <td>-6.017222</td>
      <td>-5.454164</td>
      <td>5.191569</td>
      <td>6.001656</td>
      <td>2.888981</td>
      <td>-6.224712</td>
      <td>-5.663940</td>
    </tr>
    <tr>
      <th>3179</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>19</td>
      <td>Wyoming</td>
      <td>Johnson County</td>
      <td>8569</td>
      <td>8569</td>
      <td>8581</td>
      <td>...</td>
      <td>4.995063</td>
      <td>-4.058912</td>
      <td>-0.812583</td>
      <td>-10.715742</td>
      <td>0.933652</td>
      <td>5.227392</td>
      <td>-4.058912</td>
      <td>-0.812583</td>
      <td>-10.715742</td>
      <td>0.933652</td>
    </tr>
    <tr>
      <th>3180</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>21</td>
      <td>Wyoming</td>
      <td>Laramie County</td>
      <td>91738</td>
      <td>91881</td>
      <td>92271</td>
      <td>...</td>
      <td>-1.200428</td>
      <td>15.547274</td>
      <td>4.787847</td>
      <td>-1.226133</td>
      <td>0.278940</td>
      <td>-0.973320</td>
      <td>17.914554</td>
      <td>6.003143</td>
      <td>-0.207819</td>
      <td>1.673640</td>
    </tr>
    <tr>
      <th>3181</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>23</td>
      <td>Wyoming</td>
      <td>Lincoln County</td>
      <td>18106</td>
      <td>18106</td>
      <td>18091</td>
      <td>...</td>
      <td>-9.802564</td>
      <td>-11.566801</td>
      <td>13.564556</td>
      <td>6.125989</td>
      <td>1.555544</td>
      <td>-9.691801</td>
      <td>-11.566801</td>
      <td>13.619696</td>
      <td>6.234414</td>
      <td>1.662823</td>
    </tr>
    <tr>
      <th>3182</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>25</td>
      <td>Wyoming</td>
      <td>Natrona County</td>
      <td>75450</td>
      <td>75450</td>
      <td>75472</td>
      <td>...</td>
      <td>7.189319</td>
      <td>23.066162</td>
      <td>24.322042</td>
      <td>-0.958472</td>
      <td>-0.061057</td>
      <td>7.689674</td>
      <td>23.749508</td>
      <td>25.085233</td>
      <td>-0.110593</td>
      <td>0.793743</td>
    </tr>
    <tr>
      <th>3183</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>27</td>
      <td>Wyoming</td>
      <td>Niobrara County</td>
      <td>2484</td>
      <td>2484</td>
      <td>2492</td>
      <td>...</td>
      <td>-0.401849</td>
      <td>0.806452</td>
      <td>29.066295</td>
      <td>-12.603387</td>
      <td>7.492114</td>
      <td>-0.401849</td>
      <td>0.806452</td>
      <td>29.066295</td>
      <td>-12.603387</td>
      <td>7.492114</td>
    </tr>
    <tr>
      <th>3184</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>29</td>
      <td>Wyoming</td>
      <td>Park County</td>
      <td>28205</td>
      <td>28205</td>
      <td>28259</td>
      <td>...</td>
      <td>4.582951</td>
      <td>8.057765</td>
      <td>7.641997</td>
      <td>-9.252437</td>
      <td>-2.878980</td>
      <td>6.486639</td>
      <td>11.127389</td>
      <td>10.877797</td>
      <td>-5.585731</td>
      <td>0.856839</td>
    </tr>
    <tr>
      <th>3185</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>31</td>
      <td>Wyoming</td>
      <td>Platte County</td>
      <td>8667</td>
      <td>8667</td>
      <td>8678</td>
      <td>...</td>
      <td>4.373094</td>
      <td>5.392073</td>
      <td>2.634593</td>
      <td>6.055759</td>
      <td>4.662270</td>
      <td>4.373094</td>
      <td>4.933173</td>
      <td>2.176403</td>
      <td>5.598720</td>
      <td>4.207414</td>
    </tr>
    <tr>
      <th>3186</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>33</td>
      <td>Wyoming</td>
      <td>Sheridan County</td>
      <td>29116</td>
      <td>29116</td>
      <td>29146</td>
      <td>...</td>
      <td>0.958559</td>
      <td>8.425487</td>
      <td>4.546373</td>
      <td>3.678069</td>
      <td>-3.298406</td>
      <td>2.122524</td>
      <td>9.342778</td>
      <td>5.523001</td>
      <td>4.781489</td>
      <td>-2.198937</td>
    </tr>
    <tr>
      <th>3187</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>35</td>
      <td>Wyoming</td>
      <td>Sublette County</td>
      <td>10247</td>
      <td>10247</td>
      <td>10244</td>
      <td>...</td>
      <td>-23.741784</td>
      <td>15.272374</td>
      <td>-40.870074</td>
      <td>-16.596273</td>
      <td>-22.870900</td>
      <td>-21.092907</td>
      <td>16.828794</td>
      <td>-39.211861</td>
      <td>-14.409938</td>
      <td>-20.664059</td>
    </tr>
    <tr>
      <th>3188</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>37</td>
      <td>Wyoming</td>
      <td>Sweetwater County</td>
      <td>43806</td>
      <td>43806</td>
      <td>43593</td>
      <td>...</td>
      <td>1.072643</td>
      <td>16.243199</td>
      <td>-5.339774</td>
      <td>-14.252889</td>
      <td>-14.248864</td>
      <td>1.255221</td>
      <td>16.243199</td>
      <td>-5.295460</td>
      <td>-14.075283</td>
      <td>-14.070195</td>
    </tr>
    <tr>
      <th>3189</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>39</td>
      <td>Wyoming</td>
      <td>Teton County</td>
      <td>21294</td>
      <td>21294</td>
      <td>21297</td>
      <td>...</td>
      <td>-1.589565</td>
      <td>0.972695</td>
      <td>19.525929</td>
      <td>14.143021</td>
      <td>-0.564849</td>
      <td>0.654527</td>
      <td>2.408578</td>
      <td>21.160658</td>
      <td>16.308671</td>
      <td>1.520747</td>
    </tr>
    <tr>
      <th>3190</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>41</td>
      <td>Wyoming</td>
      <td>Uinta County</td>
      <td>21118</td>
      <td>21118</td>
      <td>21102</td>
      <td>...</td>
      <td>-17.755986</td>
      <td>-4.916350</td>
      <td>-6.902954</td>
      <td>-14.215862</td>
      <td>-12.127022</td>
      <td>-18.136812</td>
      <td>-5.536861</td>
      <td>-7.521840</td>
      <td>-14.740608</td>
      <td>-12.606351</td>
    </tr>
    <tr>
      <th>3191</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>43</td>
      <td>Wyoming</td>
      <td>Washakie County</td>
      <td>8533</td>
      <td>8533</td>
      <td>8545</td>
      <td>...</td>
      <td>-11.637475</td>
      <td>-0.827815</td>
      <td>-2.013502</td>
      <td>-17.781491</td>
      <td>1.682288</td>
      <td>-11.990126</td>
      <td>-1.182592</td>
      <td>-2.250385</td>
      <td>-18.020168</td>
      <td>1.441961</td>
    </tr>
    <tr>
      <th>3192</th>
      <td>50</td>
      <td>4</td>
      <td>8</td>
      <td>56</td>
      <td>45</td>
      <td>Wyoming</td>
      <td>Weston County</td>
      <td>7208</td>
      <td>7208</td>
      <td>7181</td>
      <td>...</td>
      <td>-11.752361</td>
      <td>-8.040059</td>
      <td>12.372583</td>
      <td>1.533635</td>
      <td>6.935294</td>
      <td>-12.032179</td>
      <td>-8.040059</td>
      <td>12.372583</td>
      <td>1.533635</td>
      <td>6.935294</td>
    </tr>
  </tbody>
</table>
<p>3142 rows × 100 columns</p>
</div>




```python
%%timeit -n 10
for state in df['STNAME'].unique():
    avg = np.average(df.where(df['STNAME']==state).dropna()['CENSUS2010POP'])
    print('Counties in state ' + state + ' have an average population of ' + str(avg))
```

    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    10 loops, best of 3: 1.24 s per loop



```python
%%timeit -n 10
for group, frame in df.groupby('STNAME'):
    avg = np.average(frame['CENSUS2010POP'])
    print('Counties in state ' + group + ' have an average population of ' + str(avg))
```

    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    Counties in state Alabama have an average population of 71339.3432836
    Counties in state Alaska have an average population of 24490.7241379
    Counties in state Arizona have an average population of 426134.466667
    Counties in state Arkansas have an average population of 38878.9066667
    Counties in state California have an average population of 642309.586207
    Counties in state Colorado have an average population of 78581.1875
    Counties in state Connecticut have an average population of 446762.125
    Counties in state Delaware have an average population of 299311.333333
    Counties in state District of Columbia have an average population of 601723.0
    Counties in state Florida have an average population of 280616.567164
    Counties in state Georgia have an average population of 60928.6352201
    Counties in state Hawaii have an average population of 272060.2
    Counties in state Idaho have an average population of 35626.8636364
    Counties in state Illinois have an average population of 125790.509804
    Counties in state Indiana have an average population of 70476.1086957
    Counties in state Iowa have an average population of 30771.2626263
    Counties in state Kansas have an average population of 27172.552381
    Counties in state Kentucky have an average population of 36161.3916667
    Counties in state Louisiana have an average population of 70833.9375
    Counties in state Maine have an average population of 83022.5625
    Counties in state Maryland have an average population of 240564.666667
    Counties in state Massachusetts have an average population of 467687.785714
    Counties in state Michigan have an average population of 119080.0
    Counties in state Minnesota have an average population of 60964.6551724
    Counties in state Mississippi have an average population of 36186.5487805
    Counties in state Missouri have an average population of 52077.626087
    Counties in state Montana have an average population of 17668.125
    Counties in state Nebraska have an average population of 19638.0752688
    Counties in state Nevada have an average population of 158855.941176
    Counties in state New Hampshire have an average population of 131647.0
    Counties in state New Jersey have an average population of 418661.619048
    Counties in state New Mexico have an average population of 62399.3636364
    Counties in state New York have an average population of 312550.032258
    Counties in state North Carolina have an average population of 95354.83
    Counties in state North Dakota have an average population of 12690.3962264
    Counties in state Ohio have an average population of 131096.636364
    Counties in state Oklahoma have an average population of 48718.8441558
    Counties in state Oregon have an average population of 106418.722222
    Counties in state Pennsylvania have an average population of 189587.746269
    Counties in state Rhode Island have an average population of 210513.4
    Counties in state South Carolina have an average population of 100551.391304
    Counties in state South Dakota have an average population of 12336.0606061
    Counties in state Tennessee have an average population of 66801.1052632
    Counties in state Texas have an average population of 98998.2716535
    Counties in state Utah have an average population of 95306.3793103
    Counties in state Vermont have an average population of 44695.7857143
    Counties in state Virginia have an average population of 60111.2932331
    Counties in state Washington have an average population of 172424.102564
    Counties in state West Virginia have an average population of 33690.8
    Counties in state Wisconsin have an average population of 78985.9166667
    Counties in state Wyoming have an average population of 24505.4782609
    10 loops, best of 3: 25.4 ms per loop



```python
df.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SUMLEV</th>
      <th>REGION</th>
      <th>DIVISION</th>
      <th>STATE</th>
      <th>COUNTY</th>
      <th>STNAME</th>
      <th>CTYNAME</th>
      <th>CENSUS2010POP</th>
      <th>ESTIMATESBASE2010</th>
      <th>POPESTIMATE2010</th>
      <th>...</th>
      <th>RDOMESTICMIG2011</th>
      <th>RDOMESTICMIG2012</th>
      <th>RDOMESTICMIG2013</th>
      <th>RDOMESTICMIG2014</th>
      <th>RDOMESTICMIG2015</th>
      <th>RNETMIG2011</th>
      <th>RNETMIG2012</th>
      <th>RNETMIG2013</th>
      <th>RNETMIG2014</th>
      <th>RNETMIG2015</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>Alabama</td>
      <td>Autauga County</td>
      <td>54571</td>
      <td>54571</td>
      <td>54660</td>
      <td>...</td>
      <td>7.242091</td>
      <td>-2.915927</td>
      <td>-3.012349</td>
      <td>2.265971</td>
      <td>-2.530799</td>
      <td>7.606016</td>
      <td>-2.626146</td>
      <td>-2.722002</td>
      <td>2.592270</td>
      <td>-2.187333</td>
    </tr>
    <tr>
      <th>2</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>Alabama</td>
      <td>Baldwin County</td>
      <td>182265</td>
      <td>182265</td>
      <td>183193</td>
      <td>...</td>
      <td>14.832960</td>
      <td>17.647293</td>
      <td>21.845705</td>
      <td>19.243287</td>
      <td>17.197872</td>
      <td>15.844176</td>
      <td>18.559627</td>
      <td>22.727626</td>
      <td>20.317142</td>
      <td>18.293499</td>
    </tr>
    <tr>
      <th>3</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>5</td>
      <td>Alabama</td>
      <td>Barbour County</td>
      <td>27457</td>
      <td>27457</td>
      <td>27341</td>
      <td>...</td>
      <td>-4.728132</td>
      <td>-2.500690</td>
      <td>-7.056824</td>
      <td>-3.904217</td>
      <td>-10.543299</td>
      <td>-4.874741</td>
      <td>-2.758113</td>
      <td>-7.167664</td>
      <td>-3.978583</td>
      <td>-10.543299</td>
    </tr>
    <tr>
      <th>4</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>7</td>
      <td>Alabama</td>
      <td>Bibb County</td>
      <td>22915</td>
      <td>22919</td>
      <td>22861</td>
      <td>...</td>
      <td>-5.527043</td>
      <td>-5.068871</td>
      <td>-6.201001</td>
      <td>-0.177537</td>
      <td>0.177258</td>
      <td>-5.088389</td>
      <td>-4.363636</td>
      <td>-5.403729</td>
      <td>0.754533</td>
      <td>1.107861</td>
    </tr>
    <tr>
      <th>5</th>
      <td>50</td>
      <td>3</td>
      <td>6</td>
      <td>1</td>
      <td>9</td>
      <td>Alabama</td>
      <td>Blount County</td>
      <td>57322</td>
      <td>57322</td>
      <td>57373</td>
      <td>...</td>
      <td>1.807375</td>
      <td>-1.177622</td>
      <td>-1.748766</td>
      <td>-2.062535</td>
      <td>-1.369970</td>
      <td>1.859511</td>
      <td>-0.848580</td>
      <td>-1.402476</td>
      <td>-1.577232</td>
      <td>-0.884411</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 100 columns</p>
</div>




```python
df = df.set_index('STNAME')

def fun(item):
    if item[0]<'M':
        return 0
    if item[0]<'Q':
        return 1
    return 2

for group, frame in df.groupby(fun):
    print('There are ' + str(len(frame)) + ' records in group ' + ' for processing.')
```

    There are 1177 records in group  for processing.
    There are 1134 records in group  for processing.
    There are 831 records in group  for processing.



```python
df = pd.read_csv('census.csv')
df = df[df['SUMLEV'] == 50]
```


```python
df.groupby('STNAME').agg({'CENSUS2010POP': np.average})
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>CENSUS2010POP</th>
    </tr>
    <tr>
      <th>STNAME</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Alabama</th>
      <td>71339.343284</td>
    </tr>
    <tr>
      <th>Alaska</th>
      <td>24490.724138</td>
    </tr>
    <tr>
      <th>Arizona</th>
      <td>426134.466667</td>
    </tr>
    <tr>
      <th>Arkansas</th>
      <td>38878.906667</td>
    </tr>
    <tr>
      <th>California</th>
      <td>642309.586207</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>78581.187500</td>
    </tr>
    <tr>
      <th>Connecticut</th>
      <td>446762.125000</td>
    </tr>
    <tr>
      <th>Delaware</th>
      <td>299311.333333</td>
    </tr>
    <tr>
      <th>District of Columbia</th>
      <td>601723.000000</td>
    </tr>
    <tr>
      <th>Florida</th>
      <td>280616.567164</td>
    </tr>
    <tr>
      <th>Georgia</th>
      <td>60928.635220</td>
    </tr>
    <tr>
      <th>Hawaii</th>
      <td>272060.200000</td>
    </tr>
    <tr>
      <th>Idaho</th>
      <td>35626.863636</td>
    </tr>
    <tr>
      <th>Illinois</th>
      <td>125790.509804</td>
    </tr>
    <tr>
      <th>Indiana</th>
      <td>70476.108696</td>
    </tr>
    <tr>
      <th>Iowa</th>
      <td>30771.262626</td>
    </tr>
    <tr>
      <th>Kansas</th>
      <td>27172.552381</td>
    </tr>
    <tr>
      <th>Kentucky</th>
      <td>36161.391667</td>
    </tr>
    <tr>
      <th>Louisiana</th>
      <td>70833.937500</td>
    </tr>
    <tr>
      <th>Maine</th>
      <td>83022.562500</td>
    </tr>
    <tr>
      <th>Maryland</th>
      <td>240564.666667</td>
    </tr>
    <tr>
      <th>Massachusetts</th>
      <td>467687.785714</td>
    </tr>
    <tr>
      <th>Michigan</th>
      <td>119080.000000</td>
    </tr>
    <tr>
      <th>Minnesota</th>
      <td>60964.655172</td>
    </tr>
    <tr>
      <th>Mississippi</th>
      <td>36186.548780</td>
    </tr>
    <tr>
      <th>Missouri</th>
      <td>52077.626087</td>
    </tr>
    <tr>
      <th>Montana</th>
      <td>17668.125000</td>
    </tr>
    <tr>
      <th>Nebraska</th>
      <td>19638.075269</td>
    </tr>
    <tr>
      <th>Nevada</th>
      <td>158855.941176</td>
    </tr>
    <tr>
      <th>New Hampshire</th>
      <td>131647.000000</td>
    </tr>
    <tr>
      <th>New Jersey</th>
      <td>418661.619048</td>
    </tr>
    <tr>
      <th>New Mexico</th>
      <td>62399.363636</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>312550.032258</td>
    </tr>
    <tr>
      <th>North Carolina</th>
      <td>95354.830000</td>
    </tr>
    <tr>
      <th>North Dakota</th>
      <td>12690.396226</td>
    </tr>
    <tr>
      <th>Ohio</th>
      <td>131096.636364</td>
    </tr>
    <tr>
      <th>Oklahoma</th>
      <td>48718.844156</td>
    </tr>
    <tr>
      <th>Oregon</th>
      <td>106418.722222</td>
    </tr>
    <tr>
      <th>Pennsylvania</th>
      <td>189587.746269</td>
    </tr>
    <tr>
      <th>Rhode Island</th>
      <td>210513.400000</td>
    </tr>
    <tr>
      <th>South Carolina</th>
      <td>100551.391304</td>
    </tr>
    <tr>
      <th>South Dakota</th>
      <td>12336.060606</td>
    </tr>
    <tr>
      <th>Tennessee</th>
      <td>66801.105263</td>
    </tr>
    <tr>
      <th>Texas</th>
      <td>98998.271654</td>
    </tr>
    <tr>
      <th>Utah</th>
      <td>95306.379310</td>
    </tr>
    <tr>
      <th>Vermont</th>
      <td>44695.785714</td>
    </tr>
    <tr>
      <th>Virginia</th>
      <td>60111.293233</td>
    </tr>
    <tr>
      <th>Washington</th>
      <td>172424.102564</td>
    </tr>
    <tr>
      <th>West Virginia</th>
      <td>33690.800000</td>
    </tr>
    <tr>
      <th>Wisconsin</th>
      <td>78985.916667</td>
    </tr>
    <tr>
      <th>Wyoming</th>
      <td>24505.478261</td>
    </tr>
  </tbody>
</table>
</div>




```python
#print(df.groupby('Category').agg('sum'))
```


```python
print(type(df.groupby(level=0)['POPESTIMATE2010', 'POPESTIMATE2011']))
```

    <class 'pandas.core.groupby.DataFrameGroupBy'>



```python
print(type(df.groupby(level=0)['POPESTIMATE2010']))
```

    <class 'pandas.core.groupby.SeriesGroupBy'>



```python
(df.set_index('STNAME').groupby(level=0)['CENSUS2010POP'].agg({'avg':np.average, 'sum':np.sum}))
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sum</th>
      <th>avg</th>
    </tr>
    <tr>
      <th>STNAME</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Alabama</th>
      <td>4779736</td>
      <td>71339.343284</td>
    </tr>
    <tr>
      <th>Alaska</th>
      <td>710231</td>
      <td>24490.724138</td>
    </tr>
    <tr>
      <th>Arizona</th>
      <td>6392017</td>
      <td>426134.466667</td>
    </tr>
    <tr>
      <th>Arkansas</th>
      <td>2915918</td>
      <td>38878.906667</td>
    </tr>
    <tr>
      <th>California</th>
      <td>37253956</td>
      <td>642309.586207</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>5029196</td>
      <td>78581.187500</td>
    </tr>
    <tr>
      <th>Connecticut</th>
      <td>3574097</td>
      <td>446762.125000</td>
    </tr>
    <tr>
      <th>Delaware</th>
      <td>897934</td>
      <td>299311.333333</td>
    </tr>
    <tr>
      <th>District of Columbia</th>
      <td>601723</td>
      <td>601723.000000</td>
    </tr>
    <tr>
      <th>Florida</th>
      <td>18801310</td>
      <td>280616.567164</td>
    </tr>
    <tr>
      <th>Georgia</th>
      <td>9687653</td>
      <td>60928.635220</td>
    </tr>
    <tr>
      <th>Hawaii</th>
      <td>1360301</td>
      <td>272060.200000</td>
    </tr>
    <tr>
      <th>Idaho</th>
      <td>1567582</td>
      <td>35626.863636</td>
    </tr>
    <tr>
      <th>Illinois</th>
      <td>12830632</td>
      <td>125790.509804</td>
    </tr>
    <tr>
      <th>Indiana</th>
      <td>6483802</td>
      <td>70476.108696</td>
    </tr>
    <tr>
      <th>Iowa</th>
      <td>3046355</td>
      <td>30771.262626</td>
    </tr>
    <tr>
      <th>Kansas</th>
      <td>2853118</td>
      <td>27172.552381</td>
    </tr>
    <tr>
      <th>Kentucky</th>
      <td>4339367</td>
      <td>36161.391667</td>
    </tr>
    <tr>
      <th>Louisiana</th>
      <td>4533372</td>
      <td>70833.937500</td>
    </tr>
    <tr>
      <th>Maine</th>
      <td>1328361</td>
      <td>83022.562500</td>
    </tr>
    <tr>
      <th>Maryland</th>
      <td>5773552</td>
      <td>240564.666667</td>
    </tr>
    <tr>
      <th>Massachusetts</th>
      <td>6547629</td>
      <td>467687.785714</td>
    </tr>
    <tr>
      <th>Michigan</th>
      <td>9883640</td>
      <td>119080.000000</td>
    </tr>
    <tr>
      <th>Minnesota</th>
      <td>5303925</td>
      <td>60964.655172</td>
    </tr>
    <tr>
      <th>Mississippi</th>
      <td>2967297</td>
      <td>36186.548780</td>
    </tr>
    <tr>
      <th>Missouri</th>
      <td>5988927</td>
      <td>52077.626087</td>
    </tr>
    <tr>
      <th>Montana</th>
      <td>989415</td>
      <td>17668.125000</td>
    </tr>
    <tr>
      <th>Nebraska</th>
      <td>1826341</td>
      <td>19638.075269</td>
    </tr>
    <tr>
      <th>Nevada</th>
      <td>2700551</td>
      <td>158855.941176</td>
    </tr>
    <tr>
      <th>New Hampshire</th>
      <td>1316470</td>
      <td>131647.000000</td>
    </tr>
    <tr>
      <th>New Jersey</th>
      <td>8791894</td>
      <td>418661.619048</td>
    </tr>
    <tr>
      <th>New Mexico</th>
      <td>2059179</td>
      <td>62399.363636</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>19378102</td>
      <td>312550.032258</td>
    </tr>
    <tr>
      <th>North Carolina</th>
      <td>9535483</td>
      <td>95354.830000</td>
    </tr>
    <tr>
      <th>North Dakota</th>
      <td>672591</td>
      <td>12690.396226</td>
    </tr>
    <tr>
      <th>Ohio</th>
      <td>11536504</td>
      <td>131096.636364</td>
    </tr>
    <tr>
      <th>Oklahoma</th>
      <td>3751351</td>
      <td>48718.844156</td>
    </tr>
    <tr>
      <th>Oregon</th>
      <td>3831074</td>
      <td>106418.722222</td>
    </tr>
    <tr>
      <th>Pennsylvania</th>
      <td>12702379</td>
      <td>189587.746269</td>
    </tr>
    <tr>
      <th>Rhode Island</th>
      <td>1052567</td>
      <td>210513.400000</td>
    </tr>
    <tr>
      <th>South Carolina</th>
      <td>4625364</td>
      <td>100551.391304</td>
    </tr>
    <tr>
      <th>South Dakota</th>
      <td>814180</td>
      <td>12336.060606</td>
    </tr>
    <tr>
      <th>Tennessee</th>
      <td>6346105</td>
      <td>66801.105263</td>
    </tr>
    <tr>
      <th>Texas</th>
      <td>25145561</td>
      <td>98998.271654</td>
    </tr>
    <tr>
      <th>Utah</th>
      <td>2763885</td>
      <td>95306.379310</td>
    </tr>
    <tr>
      <th>Vermont</th>
      <td>625741</td>
      <td>44695.785714</td>
    </tr>
    <tr>
      <th>Virginia</th>
      <td>7994802</td>
      <td>60111.293233</td>
    </tr>
    <tr>
      <th>Washington</th>
      <td>6724540</td>
      <td>172424.102564</td>
    </tr>
    <tr>
      <th>West Virginia</th>
      <td>1852994</td>
      <td>33690.800000</td>
    </tr>
    <tr>
      <th>Wisconsin</th>
      <td>5686986</td>
      <td>78985.916667</td>
    </tr>
    <tr>
      <th>Wyoming</th>
      <td>563626</td>
      <td>24505.478261</td>
    </tr>
  </tbody>
</table>
</div>




```python
(df.set_index('STNAME').groupby(level=0)['POPESTIMATE2010', 'POPESTIMATE2011'].agg({'avg':np.average, 'sum':np.sum}))
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="2" halign="left">sum</th>
      <th colspan="2" halign="left">avg</th>
    </tr>
    <tr>
      <th></th>
      <th>POPESTIMATE2010</th>
      <th>POPESTIMATE2011</th>
      <th>POPESTIMATE2010</th>
      <th>POPESTIMATE2011</th>
    </tr>
    <tr>
      <th>STNAME</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Alabama</th>
      <td>4785161</td>
      <td>4801108</td>
      <td>71420.313433</td>
      <td>71658.328358</td>
    </tr>
    <tr>
      <th>Alaska</th>
      <td>714021</td>
      <td>722720</td>
      <td>24621.413793</td>
      <td>24921.379310</td>
    </tr>
    <tr>
      <th>Arizona</th>
      <td>6408208</td>
      <td>6468732</td>
      <td>427213.866667</td>
      <td>431248.800000</td>
    </tr>
    <tr>
      <th>Arkansas</th>
      <td>2922394</td>
      <td>2938538</td>
      <td>38965.253333</td>
      <td>39180.506667</td>
    </tr>
    <tr>
      <th>California</th>
      <td>37334079</td>
      <td>37700034</td>
      <td>643691.017241</td>
      <td>650000.586207</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>5048254</td>
      <td>5119480</td>
      <td>78878.968750</td>
      <td>79991.875000</td>
    </tr>
    <tr>
      <th>Connecticut</th>
      <td>3579717</td>
      <td>3589759</td>
      <td>447464.625000</td>
      <td>448719.875000</td>
    </tr>
    <tr>
      <th>Delaware</th>
      <td>899791</td>
      <td>907916</td>
      <td>299930.333333</td>
      <td>302638.666667</td>
    </tr>
    <tr>
      <th>District of Columbia</th>
      <td>605126</td>
      <td>620472</td>
      <td>605126.000000</td>
      <td>620472.000000</td>
    </tr>
    <tr>
      <th>Florida</th>
      <td>18849890</td>
      <td>19105533</td>
      <td>281341.641791</td>
      <td>285157.208955</td>
    </tr>
    <tr>
      <th>Georgia</th>
      <td>9713454</td>
      <td>9812280</td>
      <td>61090.905660</td>
      <td>61712.452830</td>
    </tr>
    <tr>
      <th>Hawaii</th>
      <td>1363980</td>
      <td>1378227</td>
      <td>272796.000000</td>
      <td>275645.400000</td>
    </tr>
    <tr>
      <th>Idaho</th>
      <td>1570986</td>
      <td>1584134</td>
      <td>35704.227273</td>
      <td>36003.045455</td>
    </tr>
    <tr>
      <th>Illinois</th>
      <td>12841249</td>
      <td>12861882</td>
      <td>125894.598039</td>
      <td>126096.882353</td>
    </tr>
    <tr>
      <th>Indiana</th>
      <td>6490590</td>
      <td>6516845</td>
      <td>70549.891304</td>
      <td>70835.271739</td>
    </tr>
    <tr>
      <th>Iowa</th>
      <td>3050694</td>
      <td>3065389</td>
      <td>30815.090909</td>
      <td>30963.525253</td>
    </tr>
    <tr>
      <th>Kansas</th>
      <td>2858824</td>
      <td>2869917</td>
      <td>27226.895238</td>
      <td>27332.542857</td>
    </tr>
    <tr>
      <th>Kentucky</th>
      <td>4347937</td>
      <td>4367882</td>
      <td>36232.808333</td>
      <td>36399.016667</td>
    </tr>
    <tr>
      <th>Louisiana</th>
      <td>4544951</td>
      <td>4575381</td>
      <td>71014.859375</td>
      <td>71490.328125</td>
    </tr>
    <tr>
      <th>Maine</th>
      <td>1327695</td>
      <td>1328257</td>
      <td>82980.937500</td>
      <td>83016.062500</td>
    </tr>
    <tr>
      <th>Maryland</th>
      <td>5788409</td>
      <td>5844171</td>
      <td>241183.708333</td>
      <td>243507.125000</td>
    </tr>
    <tr>
      <th>Massachusetts</th>
      <td>6565036</td>
      <td>6611797</td>
      <td>468931.142857</td>
      <td>472271.214286</td>
    </tr>
    <tr>
      <th>Michigan</th>
      <td>9877369</td>
      <td>9876589</td>
      <td>119004.445783</td>
      <td>118995.048193</td>
    </tr>
    <tr>
      <th>Minnesota</th>
      <td>5310903</td>
      <td>5348119</td>
      <td>61044.862069</td>
      <td>61472.632184</td>
    </tr>
    <tr>
      <th>Mississippi</th>
      <td>2970316</td>
      <td>2977999</td>
      <td>36223.365854</td>
      <td>36317.060976</td>
    </tr>
    <tr>
      <th>Missouri</th>
      <td>5996052</td>
      <td>6010587</td>
      <td>52139.582609</td>
      <td>52265.973913</td>
    </tr>
    <tr>
      <th>Montana</th>
      <td>990643</td>
      <td>997746</td>
      <td>17690.053571</td>
      <td>17816.892857</td>
    </tr>
    <tr>
      <th>Nebraska</th>
      <td>1830025</td>
      <td>1842383</td>
      <td>19677.688172</td>
      <td>19810.569892</td>
    </tr>
    <tr>
      <th>Nevada</th>
      <td>2703440</td>
      <td>2718819</td>
      <td>159025.882353</td>
      <td>159930.529412</td>
    </tr>
    <tr>
      <th>New Hampshire</th>
      <td>1316708</td>
      <td>1318344</td>
      <td>131670.800000</td>
      <td>131834.400000</td>
    </tr>
    <tr>
      <th>New Jersey</th>
      <td>8803881</td>
      <td>8842934</td>
      <td>419232.428571</td>
      <td>421092.095238</td>
    </tr>
    <tr>
      <th>New Mexico</th>
      <td>2064741</td>
      <td>2078226</td>
      <td>62567.909091</td>
      <td>62976.545455</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>19402920</td>
      <td>19523202</td>
      <td>312950.322581</td>
      <td>314890.354839</td>
    </tr>
    <tr>
      <th>North Carolina</th>
      <td>9558979</td>
      <td>9651025</td>
      <td>95589.790000</td>
      <td>96510.250000</td>
    </tr>
    <tr>
      <th>North Dakota</th>
      <td>674530</td>
      <td>685326</td>
      <td>12726.981132</td>
      <td>12930.679245</td>
    </tr>
    <tr>
      <th>Ohio</th>
      <td>11540766</td>
      <td>11545442</td>
      <td>131145.068182</td>
      <td>131198.204545</td>
    </tr>
    <tr>
      <th>Oklahoma</th>
      <td>3759596</td>
      <td>3786626</td>
      <td>48825.922078</td>
      <td>49176.961039</td>
    </tr>
    <tr>
      <th>Oregon</th>
      <td>3837972</td>
      <td>3868509</td>
      <td>106610.333333</td>
      <td>107458.583333</td>
    </tr>
    <tr>
      <th>Pennsylvania</th>
      <td>12712014</td>
      <td>12745202</td>
      <td>189731.552239</td>
      <td>190226.895522</td>
    </tr>
    <tr>
      <th>Rhode Island</th>
      <td>1053219</td>
      <td>1051856</td>
      <td>210643.800000</td>
      <td>210371.200000</td>
    </tr>
    <tr>
      <th>South Carolina</th>
      <td>4635894</td>
      <td>4672733</td>
      <td>100780.304348</td>
      <td>101581.152174</td>
    </tr>
    <tr>
      <th>South Dakota</th>
      <td>816299</td>
      <td>824289</td>
      <td>12368.166667</td>
      <td>12489.227273</td>
    </tr>
    <tr>
      <th>Tennessee</th>
      <td>6356585</td>
      <td>6398408</td>
      <td>66911.421053</td>
      <td>67351.663158</td>
    </tr>
    <tr>
      <th>Texas</th>
      <td>25244363</td>
      <td>25654464</td>
      <td>99387.255906</td>
      <td>101001.826772</td>
    </tr>
    <tr>
      <th>Utah</th>
      <td>2775426</td>
      <td>2816440</td>
      <td>95704.344828</td>
      <td>97118.620690</td>
    </tr>
    <tr>
      <th>Vermont</th>
      <td>625984</td>
      <td>626687</td>
      <td>44713.142857</td>
      <td>44763.357143</td>
    </tr>
    <tr>
      <th>Virginia</th>
      <td>8025787</td>
      <td>8110783</td>
      <td>60344.263158</td>
      <td>60983.330827</td>
    </tr>
    <tr>
      <th>Washington</th>
      <td>6743060</td>
      <td>6823229</td>
      <td>172898.974359</td>
      <td>174954.589744</td>
    </tr>
    <tr>
      <th>West Virginia</th>
      <td>1854225</td>
      <td>1854948</td>
      <td>33713.181818</td>
      <td>33726.327273</td>
    </tr>
    <tr>
      <th>Wisconsin</th>
      <td>5690204</td>
      <td>5709720</td>
      <td>79030.611111</td>
      <td>79301.666667</td>
    </tr>
    <tr>
      <th>Wyoming</th>
      <td>564516</td>
      <td>567768</td>
      <td>24544.173913</td>
      <td>24685.565217</td>
    </tr>
  </tbody>
</table>
</div>




```python
(df.set_index('STNAME').groupby(level=0)['POPESTIMATE2010', 'POPESTIMATE2011'].agg({'POPESTIMATE2010':np.average, 'POPESTIMATE2011':np.sum}))
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>POPESTIMATE2010</th>
      <th>POPESTIMATE2011</th>
    </tr>
    <tr>
      <th>STNAME</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Alabama</th>
      <td>71420.313433</td>
      <td>4801108</td>
    </tr>
    <tr>
      <th>Alaska</th>
      <td>24621.413793</td>
      <td>722720</td>
    </tr>
    <tr>
      <th>Arizona</th>
      <td>427213.866667</td>
      <td>6468732</td>
    </tr>
    <tr>
      <th>Arkansas</th>
      <td>38965.253333</td>
      <td>2938538</td>
    </tr>
    <tr>
      <th>California</th>
      <td>643691.017241</td>
      <td>37700034</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>78878.968750</td>
      <td>5119480</td>
    </tr>
    <tr>
      <th>Connecticut</th>
      <td>447464.625000</td>
      <td>3589759</td>
    </tr>
    <tr>
      <th>Delaware</th>
      <td>299930.333333</td>
      <td>907916</td>
    </tr>
    <tr>
      <th>District of Columbia</th>
      <td>605126.000000</td>
      <td>620472</td>
    </tr>
    <tr>
      <th>Florida</th>
      <td>281341.641791</td>
      <td>19105533</td>
    </tr>
    <tr>
      <th>Georgia</th>
      <td>61090.905660</td>
      <td>9812280</td>
    </tr>
    <tr>
      <th>Hawaii</th>
      <td>272796.000000</td>
      <td>1378227</td>
    </tr>
    <tr>
      <th>Idaho</th>
      <td>35704.227273</td>
      <td>1584134</td>
    </tr>
    <tr>
      <th>Illinois</th>
      <td>125894.598039</td>
      <td>12861882</td>
    </tr>
    <tr>
      <th>Indiana</th>
      <td>70549.891304</td>
      <td>6516845</td>
    </tr>
    <tr>
      <th>Iowa</th>
      <td>30815.090909</td>
      <td>3065389</td>
    </tr>
    <tr>
      <th>Kansas</th>
      <td>27226.895238</td>
      <td>2869917</td>
    </tr>
    <tr>
      <th>Kentucky</th>
      <td>36232.808333</td>
      <td>4367882</td>
    </tr>
    <tr>
      <th>Louisiana</th>
      <td>71014.859375</td>
      <td>4575381</td>
    </tr>
    <tr>
      <th>Maine</th>
      <td>82980.937500</td>
      <td>1328257</td>
    </tr>
    <tr>
      <th>Maryland</th>
      <td>241183.708333</td>
      <td>5844171</td>
    </tr>
    <tr>
      <th>Massachusetts</th>
      <td>468931.142857</td>
      <td>6611797</td>
    </tr>
    <tr>
      <th>Michigan</th>
      <td>119004.445783</td>
      <td>9876589</td>
    </tr>
    <tr>
      <th>Minnesota</th>
      <td>61044.862069</td>
      <td>5348119</td>
    </tr>
    <tr>
      <th>Mississippi</th>
      <td>36223.365854</td>
      <td>2977999</td>
    </tr>
    <tr>
      <th>Missouri</th>
      <td>52139.582609</td>
      <td>6010587</td>
    </tr>
    <tr>
      <th>Montana</th>
      <td>17690.053571</td>
      <td>997746</td>
    </tr>
    <tr>
      <th>Nebraska</th>
      <td>19677.688172</td>
      <td>1842383</td>
    </tr>
    <tr>
      <th>Nevada</th>
      <td>159025.882353</td>
      <td>2718819</td>
    </tr>
    <tr>
      <th>New Hampshire</th>
      <td>131670.800000</td>
      <td>1318344</td>
    </tr>
    <tr>
      <th>New Jersey</th>
      <td>419232.428571</td>
      <td>8842934</td>
    </tr>
    <tr>
      <th>New Mexico</th>
      <td>62567.909091</td>
      <td>2078226</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>312950.322581</td>
      <td>19523202</td>
    </tr>
    <tr>
      <th>North Carolina</th>
      <td>95589.790000</td>
      <td>9651025</td>
    </tr>
    <tr>
      <th>North Dakota</th>
      <td>12726.981132</td>
      <td>685326</td>
    </tr>
    <tr>
      <th>Ohio</th>
      <td>131145.068182</td>
      <td>11545442</td>
    </tr>
    <tr>
      <th>Oklahoma</th>
      <td>48825.922078</td>
      <td>3786626</td>
    </tr>
    <tr>
      <th>Oregon</th>
      <td>106610.333333</td>
      <td>3868509</td>
    </tr>
    <tr>
      <th>Pennsylvania</th>
      <td>189731.552239</td>
      <td>12745202</td>
    </tr>
    <tr>
      <th>Rhode Island</th>
      <td>210643.800000</td>
      <td>1051856</td>
    </tr>
    <tr>
      <th>South Carolina</th>
      <td>100780.304348</td>
      <td>4672733</td>
    </tr>
    <tr>
      <th>South Dakota</th>
      <td>12368.166667</td>
      <td>824289</td>
    </tr>
    <tr>
      <th>Tennessee</th>
      <td>66911.421053</td>
      <td>6398408</td>
    </tr>
    <tr>
      <th>Texas</th>
      <td>99387.255906</td>
      <td>25654464</td>
    </tr>
    <tr>
      <th>Utah</th>
      <td>95704.344828</td>
      <td>2816440</td>
    </tr>
    <tr>
      <th>Vermont</th>
      <td>44713.142857</td>
      <td>626687</td>
    </tr>
    <tr>
      <th>Virginia</th>
      <td>60344.263158</td>
      <td>8110783</td>
    </tr>
    <tr>
      <th>Washington</th>
      <td>172898.974359</td>
      <td>6823229</td>
    </tr>
    <tr>
      <th>West Virginia</th>
      <td>33713.181818</td>
      <td>1854948</td>
    </tr>
    <tr>
      <th>Wisconsin</th>
      <td>79030.611111</td>
      <td>5709720</td>
    </tr>
    <tr>
      <th>Wyoming</th>
      <td>24544.173913</td>
      <td>567768</td>
    </tr>
  </tbody>
</table>
</div>




```python
#print(df.groupby('Category).apply(lambda df,a,b:sum(df[a]*df[b]), 'Weight(oz.)', 'Quality'))
# or => without using a lambda
#def totalweight(df, w, q):
#    return sum(df[w] * df[q])
#print(df.groupby('Category').apply(totalweight, 'Weight(oz.)', 'Quantity'))
# outputs:

#Category

#Clothing   20.5
#Health     10.7
#Kitchen    92.5
#Pack       33.0
#Shelter    80.0

```


```python

```
