# Exercise 1

### Step 1. Go to https://www.kaggle.com/openfoodfacts/world-food-facts/data

### Step 2. Download the dataset to your computer and unzip it.

### Step 3. Use the tsv file and assign it to a dataframe called food


```python
import pandas as pd 
import numpy as np 

df = pd.read_table("D:/Courses/Projects/en.openfoodfacts.org.products.tsv")
df
```

    C:\Users\Mua\anaconda3\lib\site-packages\IPython\core\interactiveshell.py:3444: DtypeWarning: Columns (0,3,5,19,20,24,25,26,27,28,36,37,38,39,48) have mixed types.Specify dtype option on import or set low_memory=False.
      exec(code_obj, self.user_global_ns, self.user_ns)
    




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
      <th>code</th>
      <th>url</th>
      <th>creator</th>
      <th>created_t</th>
      <th>created_datetime</th>
      <th>last_modified_t</th>
      <th>last_modified_datetime</th>
      <th>product_name</th>
      <th>generic_name</th>
      <th>quantity</th>
      <th>...</th>
      <th>fruits-vegetables-nuts_100g</th>
      <th>fruits-vegetables-nuts-estimate_100g</th>
      <th>collagen-meat-protein-ratio_100g</th>
      <th>cocoa_100g</th>
      <th>chlorophyl_100g</th>
      <th>carbon-footprint_100g</th>
      <th>nutrition-score-fr_100g</th>
      <th>nutrition-score-uk_100g</th>
      <th>glycemic-index_100g</th>
      <th>water-hardness_100g</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3087</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>openfoodfacts-contributors</td>
      <td>1474103866</td>
      <td>2016-09-17T09:17:46Z</td>
      <td>1474103893</td>
      <td>2016-09-17T09:18:13Z</td>
      <td>Farine de blé noir</td>
      <td>NaN</td>
      <td>1kg</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4530</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>Banana Chips Sweetened (Whole)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>14.0</td>
      <td>14.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4559</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>Peanuts</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>16087</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489055731</td>
      <td>2017-03-09T10:35:31Z</td>
      <td>1489055731</td>
      <td>2017-03-09T10:35:31Z</td>
      <td>Organic Salted Nut Mix</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>12.0</td>
      <td>12.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>16094</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489055653</td>
      <td>2017-03-09T10:34:13Z</td>
      <td>1489055653</td>
      <td>2017-03-09T10:34:13Z</td>
      <td>Organic Polenta</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
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
      <th>356022</th>
      <td>99567453</td>
      <td>http://world-en.openfoodfacts.org/product/9956...</td>
      <td>usda-ndb-import</td>
      <td>1489059076</td>
      <td>2017-03-09T11:31:16Z</td>
      <td>1491244499</td>
      <td>2017-04-03T18:34:59Z</td>
      <td>Mint Melange Tea A Blend Of Peppermint, Lemon ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>356023</th>
      <td>9970229501521</td>
      <td>http://world-en.openfoodfacts.org/product/9970...</td>
      <td>tomato</td>
      <td>1422099377</td>
      <td>2015-01-24T11:36:17Z</td>
      <td>1491244499</td>
      <td>2017-04-03T18:34:59Z</td>
      <td>乐吧泡菜味薯片</td>
      <td>Leba pickle flavor potato chips</td>
      <td>50 g</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>356024</th>
      <td>9977471758307</td>
      <td>http://world-en.openfoodfacts.org/product/9977...</td>
      <td>openfoodfacts-contributors</td>
      <td>1497018549</td>
      <td>2017-06-09T14:29:09Z</td>
      <td>1500730305</td>
      <td>2017-07-22T13:31:45Z</td>
      <td>Biscottes bio</td>
      <td>NaN</td>
      <td>300g</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>356025</th>
      <td>9980282863788</td>
      <td>http://world-en.openfoodfacts.org/product/9980...</td>
      <td>openfoodfacts-contributors</td>
      <td>1492340089</td>
      <td>2017-04-16T10:54:49Z</td>
      <td>1492340089</td>
      <td>2017-04-16T10:54:49Z</td>
      <td>Tomates aux Vermicelles</td>
      <td>NaN</td>
      <td>67g</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>356026</th>
      <td>999990026839</td>
      <td>http://world-en.openfoodfacts.org/product/9999...</td>
      <td>usda-ndb-import</td>
      <td>1489072709</td>
      <td>2017-03-09T15:18:29Z</td>
      <td>1491244499</td>
      <td>2017-04-03T18:34:59Z</td>
      <td>Sugar Free Drink Mix, Peach Tea</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>356027 rows × 163 columns</p>
</div>




```python
df.describe(include="all")
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
      <th>code</th>
      <th>url</th>
      <th>creator</th>
      <th>created_t</th>
      <th>created_datetime</th>
      <th>last_modified_t</th>
      <th>last_modified_datetime</th>
      <th>product_name</th>
      <th>generic_name</th>
      <th>quantity</th>
      <th>...</th>
      <th>fruits-vegetables-nuts_100g</th>
      <th>fruits-vegetables-nuts-estimate_100g</th>
      <th>collagen-meat-protein-ratio_100g</th>
      <th>cocoa_100g</th>
      <th>chlorophyl_100g</th>
      <th>carbon-footprint_100g</th>
      <th>nutrition-score-fr_100g</th>
      <th>nutrition-score-uk_100g</th>
      <th>glycemic-index_100g</th>
      <th>water-hardness_100g</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>3.560010e+05</td>
      <td>356001</td>
      <td>356024</td>
      <td>3.560240e+05</td>
      <td>356017</td>
      <td>3.560270e+05</td>
      <td>356027</td>
      <td>338515</td>
      <td>57714</td>
      <td>119285</td>
      <td>...</td>
      <td>3228.000000</td>
      <td>404.000000</td>
      <td>182.000000</td>
      <td>1383.000000</td>
      <td>0.0</td>
      <td>278.000000</td>
      <td>254856.000000</td>
      <td>254856.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>unique</th>
      <td>3.558390e+05</td>
      <td>356001</td>
      <td>3890</td>
      <td>2.248120e+05</td>
      <td>224752</td>
      <td>2.169360e+05</td>
      <td>216836</td>
      <td>249245</td>
      <td>42451</td>
      <td>15563</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>top</th>
      <td>7.065080e+10</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1.489077e+09</td>
      <td>2017-03-09T10:37:09Z</td>
      <td>1.439142e+09</td>
      <td>2015-08-09T17:35:42Z</td>
      <td>Ice Cream</td>
      <td>Pâtes alimentaires au blé dur de qualité supér...</td>
      <td>500 g</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>freq</th>
      <td>3.000000e+00</td>
      <td>1</td>
      <td>169868</td>
      <td>2.000000e+01</td>
      <td>20</td>
      <td>3.000000e+01</td>
      <td>30</td>
      <td>411</td>
      <td>201</td>
      <td>5285</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>33.392680</td>
      <td>60.360124</td>
      <td>15.362637</td>
      <td>52.102675</td>
      <td>NaN</td>
      <td>335.790664</td>
      <td>9.166137</td>
      <td>8.980656</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>std</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>32.906834</td>
      <td>29.262350</td>
      <td>3.692658</td>
      <td>19.028361</td>
      <td>NaN</td>
      <td>423.244817</td>
      <td>8.999870</td>
      <td>9.151757</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>min</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>8.000000</td>
      <td>6.000000</td>
      <td>NaN</td>
      <td>0.000000</td>
      <td>-15.000000</td>
      <td>-15.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>0.000000</td>
      <td>45.000000</td>
      <td>12.000000</td>
      <td>33.000000</td>
      <td>NaN</td>
      <td>82.650000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>25.000000</td>
      <td>58.000000</td>
      <td>15.000000</td>
      <td>52.000000</td>
      <td>NaN</td>
      <td>190.950000</td>
      <td>10.000000</td>
      <td>9.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>55.000000</td>
      <td>93.000000</td>
      <td>15.000000</td>
      <td>70.000000</td>
      <td>NaN</td>
      <td>378.700000</td>
      <td>16.000000</td>
      <td>16.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>max</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>25.000000</td>
      <td>100.000000</td>
      <td>NaN</td>
      <td>2842.000000</td>
      <td>40.000000</td>
      <td>40.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>11 rows × 163 columns</p>
</div>



### Step 4. See the first 5 entries


```python
df.head(5)
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
      <th>code</th>
      <th>url</th>
      <th>creator</th>
      <th>created_t</th>
      <th>created_datetime</th>
      <th>last_modified_t</th>
      <th>last_modified_datetime</th>
      <th>product_name</th>
      <th>generic_name</th>
      <th>quantity</th>
      <th>...</th>
      <th>fruits-vegetables-nuts_100g</th>
      <th>fruits-vegetables-nuts-estimate_100g</th>
      <th>collagen-meat-protein-ratio_100g</th>
      <th>cocoa_100g</th>
      <th>chlorophyl_100g</th>
      <th>carbon-footprint_100g</th>
      <th>nutrition-score-fr_100g</th>
      <th>nutrition-score-uk_100g</th>
      <th>glycemic-index_100g</th>
      <th>water-hardness_100g</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3087</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>openfoodfacts-contributors</td>
      <td>1474103866</td>
      <td>2016-09-17T09:17:46Z</td>
      <td>1474103893</td>
      <td>2016-09-17T09:18:13Z</td>
      <td>Farine de blé noir</td>
      <td>NaN</td>
      <td>1kg</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4530</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>Banana Chips Sweetened (Whole)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>14.0</td>
      <td>14.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4559</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>1489069957</td>
      <td>2017-03-09T14:32:37Z</td>
      <td>Peanuts</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>16087</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489055731</td>
      <td>2017-03-09T10:35:31Z</td>
      <td>1489055731</td>
      <td>2017-03-09T10:35:31Z</td>
      <td>Organic Salted Nut Mix</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>12.0</td>
      <td>12.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>16094</td>
      <td>http://world-en.openfoodfacts.org/product/0000...</td>
      <td>usda-ndb-import</td>
      <td>1489055653</td>
      <td>2017-03-09T10:34:13Z</td>
      <td>1489055653</td>
      <td>2017-03-09T10:34:13Z</td>
      <td>Organic Polenta</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 163 columns</p>
</div>



### Step 5. What is the number of observations in the dataset?


```python
df.shape[0]
```




    356027



### Step 6. What is the number of columns in the dataset?


```python
df.shape[1]
```




    163



### Step 7. Print the name of all the columns.


```python
df.columns
```




    Index(['code', 'url', 'creator', 'created_t', 'created_datetime',
           'last_modified_t', 'last_modified_datetime', 'product_name',
           'generic_name', 'quantity',
           ...
           'fruits-vegetables-nuts_100g', 'fruits-vegetables-nuts-estimate_100g',
           'collagen-meat-protein-ratio_100g', 'cocoa_100g', 'chlorophyl_100g',
           'carbon-footprint_100g', 'nutrition-score-fr_100g',
           'nutrition-score-uk_100g', 'glycemic-index_100g',
           'water-hardness_100g'],
          dtype='object', length=163)



### Step 8. What is the name of 105th column?


```python
df.columns[105]
```




    '-fructose_100g'



### Step 9. What is the type of the observations of the 105th column?


```python
df.dtypes[105]
```




    dtype('float64')



### Step 10. How is the dataset indexed?


```python
df.index
```




    RangeIndex(start=0, stop=356027, step=1)



### Step 11. What is the product name of the 19th observation?


```python
df["product_name"][105]
```




    'Split Pea Soup Mix'



### The END
