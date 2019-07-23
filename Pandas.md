基本介绍
一维矩阵：

    s=pd.Series([1,3,6,np.nan,44,1])

DataFrame：
    
    dates=pd.date_range("20160101",periods=6,columns=["a","b","c","d"])
    
    df=pd.DateFrame(np.random.randn(6,4),index=dates)#选择日期作为index,如果不选择，默认01234....
 
 
df.dtypes  #每一列的数据属性
df.index  #index序号
df.columns #属性名和数据属性
df.values #每一列的数据
df.describe #数据的平均数，最小值，25%，75%等等
df2.T #矩阵转置
df.sort_index(axis=1,ascending=False) #按照索引列排序
df.sort_index(axis=0,ascending=False) #按照索引行排列
df.sort_values(by="E") #按照值排序

选择数据
df["A"],df.A #两个同一个效果
df[df[0:3],df["20130103":"20130108"]] #dataframe的前三行,以及指定行

select by label:loc
df.loc["20130102"]
df.loc[:,["A","B"]]
df.loc["20130102",["A","B"]]

select by position:iloc
df.iloc[3,1] #索引第三行

mixed selection:ix
df.ix[:3,["A","C"]] #混合筛选

boolen indexing
df[df.A>8]




