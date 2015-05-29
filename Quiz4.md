## 06 Statistical Inference - Quiz 4

####1.Question 1 :

A pharmaceutical company is interested in testing a potential blood pressure lowering medication. Their first examination considers only subjects that received the medication at baseline then two weeks later. 
The data are as follows (SBP in mmHg)

Subject	Baseline	Week 2
1	140	132
2	138	135
3	150	151
4	148	146
5	135	130

Consider testing the hypothesis that there was a mean reduction in blood pressure? Give the P-value for the associated two sided T test.
(Hint, consider that the observations are paired.)

subject<-c(1,2,3,4,5)

Baseline<-c(140,138,150,148,135)

Week2<-c(132,135,151,146,130)

BPLMData<-data.frame(subject, Baseline, Week2)

> BPLMData
  subject Baseline Week2
1       1      140   132
2       2      138   135
3       3      150   151
4       4      148   146
5       5      135   130

> TTest<-t.test(x=BPLMData$Baseline, y=BPLMData$Week2, alt="two.sided", paired=TRUE)
> TTest$p.value
[1] 0.08652278

#####Ans : 0.0865 ~ 0.087

####2.Question 2 : 
A sample of 9 men yielded a sample average brain volume of 1,100cc and a standard deviation of 30cc. What is the complete 
set of values of μ0 that a test of H0:μ=μ0 would fail to reject the null hypothesis in a two sided 5% Students t-test?

n<-9
mu0<-




















