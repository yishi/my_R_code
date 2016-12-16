# my_R_code

Here is a repository for my R code.

########################################### May 2016 ###############################
Recently, I read the book - Practical Data Science Cookbook.

I practice my code capacity not only in R but also in Python.

I use the automobile [**data**](http://www.fueleconomy.gov/feg/epadata/vehicles.csv.zip) from U.S. Department of Energy to do data analysis, which is the example from the chapter 2 of the book, the R code is in this directory, the Python code is in [**here**](http://nbviewer.jupyter.org/github/yishi/Data-Analysis-Series-in-Python/blob/master/Data_Analysis_Series_VI.ipynb).

I also save my R code, which is from the example of the chapter 5 of the book, mainly use the package **dplyr** and **data.table** to deal with this socalled middle size of data, which could fit the memory of our laptop computer, but maybe kill our programming time.

We always talk about big data, TB, PB, but I think we had better sharpen our skills using middle data first, such as data clean, data transformation, make prediction or classification or some other models, compare these models and choose the best, then deploy this model and to test it in the real scene.

########################################### December 2016 ###############################
Several days ago, I discover a new package about text mining, **text2vec**, this package is great, I use this package and other packages to predict the defect name from the defect description text, this idea if similar to sentiment analysis, just change response variable Y values from positive/negative to defect name1/2/3/...

Below is a flowchart about text mining.

text data
  
  |  
segmentation（for chinese text）jiebaR package
  |
transform to structural data, such as matrix, use text2vec package, English text could split the sentence to word in this package, which is similar to segmentation
1. data clean
first of all, delete stop words
second, choose the number of the word to make vector, n-gram
third, delete very common and very unusual terms
fourth, whether to use hashing trick, which could shorten the run time when there have large collections of documents
fifth, make a document-term matrix
2. transform document-term matrix
normalization：decrease the influence of the lengths of the documents
tf-idf：increase the weight of terms which are specific and decrease the weight for terms used in most documents
 |
use model, such as sentiment analysis, use classification model, to predict positive or negative


chinese version flowchart  

文本
  |
分词（针对中文）jiebaR
  |
转换成结构化的数据，如矩阵  text2vec包  （英文可以直接在这里把词分离开，相当于分词），
1 进行数据清洗
首先，删除停用词，
其次，选择使用词的个数，n-gram
第三，删除大量常出现的无用词，删除少量偶尔出现的词 
第四，是否使用hashing trick去向量化词语，在数据量大的时候，可以提高速度
第五，生成文档-词语矩阵
2. 矩阵的转换
normalization：消除句子长度的影响（提高惜字如金者的影响力）
tf-idf：对每个词的权重进行调整（降低常用字的份量）
 |
使用模型，如情感分析，使用分类模型，预测积极或消极

