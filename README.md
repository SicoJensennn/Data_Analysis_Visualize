# Data_Analysis_Visualize

## 1. [DataFrame_Intro](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/01_DataFrames_Intro.ipynb)

+ attributes of dataFrame
  + `type(df)`
  + `df.shape`
  + `df.columns`
  + `df.size`
+ see the content
  + `head`
  + `tail`
  + `info`
+ modify the column names in `read_csv`



## 2. [Basic Computation Methods](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/02_Basic_Methods_Computation.ipynb)

+ `min`, `max`, `sum`
+ `mean`, `median`
+ `mode`
+ `describe`



## 3. [Series](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/03_Series_Columns.ipynb)

+ select columns

+ `min`, `sum`, `max`

+ `index`, `values`

+ create Series with `pd.Series()`

+ `unique`, `nlargest`, `nsmallest`, `value_counts`

+ `plot`

  ```python
  df.series.plot(kind = "")
  df[[a,b]].plot(kind = "", x = "a", y = "b")
  ```

  kind: hist, line, bar, barh, hist, box, kde, density, area, pie, scatter, hexbin.



## 4. [Index and Sorting](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/04_Indexes_and_Sorting.ipynb)

+ `set_index`
+ `sort_values`
+ `sort_index`
+ `loc`, `iloc`



## 5. [Filter Data](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/05_Filtering_DataFrames.ipynb)

+ `==`, `<=`, `>=`
+ `between`
+ `isin`
+ combine
  + `&`
  + `|`
  + `~`
+ `isna`, `notna`



## 6. [Add & Delete Columns](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/06_Add_Delete_Column.ipynb)

+ `drop`

+ add column

  + normal way
  + `insert`

+ dynamic column: `+`

  ```python
  relative = titanic["sibsp"] + titanic["parch"]
  ```



## 7. [Change Values](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/07_Modify_Values.ipynb)

+ `rename`

  ```python
  countries.rename(columns = replace)
  countries.rename(index = change, inplace = True)
  ```

+ `replace`

+ Using `loc` to change values

  ```python
  countries.loc[["Finland", "Denmark"],["Regional indicator"]] = "Scandinavia"
  ```



## 8. [Data Type](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/08_DataTypes.ipynb)

+ `astype`
+ `to_numeric`
+ `dropna`
+ `fillna`



## 9. [Dates](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/09_Working_With_Dates.ipynb)

+ `to_datetime`

+ `df.dt.year`

+ comparing dates

## 10. [Matplotlib](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/10_Matplotlib.ipynb)

+ `plt.plot(x, y)`

+ Figure

  Figure is the top level thing, including couple of plots.

  `plt.figure()`

  `plt.figure(figsize = (), dip = )`

  `dip`: control the number of pixel per inch.

+ Style

  + check available style: `plt.style.available`
  + use style: `plt.style.use()`
  + linewidth, linestyle

+ Title & Label

  + `plt.title`: the name of the plot.
  + `plt.label`: the name of x/y axis.
  + `plt.tick`: the frequency of x/y axis.
  + `plt.lim`: the range of x/y axis.

+ Bar plots

  `plt.bar()`

  `plt.barh()`

+ Histogram

  `plt.hist(color = , bins = , alpha = )`

  `bins`：the number of equal-width bins in the range.

  `alpha`: transparency.



## 11. [Pandas](https://github.com/SicoJensennn/Data_Analysis_Visualize/blob/main/11_Pandas_Matplotlib.ipynb)

+ `Dataframe.plot(kind, title, xlabel, fontsize)`

  + `kind`: default line, can also use kind = "bar", "hist".

+ Box plots

  <img src="C:\Users\u1474799\AppData\Roaming\Typora\typora-user-images\image-20240618160247317.png" alt="image-20240618160247317" style="zoom:50%;" />

  + `df.boxplot()`

+ Scatter plot

  `df.plot.scatter(marker =)`

+ Automatic subplots

  `df.plot(subplots = True, sharex = False)`

  `subplots = True` : Make separate subplots for each column.

  ```
  fig, axs = plt.subplots(1,2)
  axs[0].
  axs[1].
  ```

+ Save Figure

  `plt.savefig("name")`

  

