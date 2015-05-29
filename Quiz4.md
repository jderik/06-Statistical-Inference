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

BPLMData
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
mu<-1100
sd<-30
quantile<-0.975
ConfidenceInterval = mu + c(-1,1) * qt(quantile, n-1)  * sd/sqrt(n)
ConfidenceInterval

#####Ans : [1] 1076.94 1123.06

####3.Question 3 : 
Researchers conducted a blind taste test of Coke versus Pepsi. Each of four people was asked which of two blinded drinks given in random order that they preferred. The data was such that 3 of the 4 people chose Coke. Assuming that this sample is representative, report a P-value for a test of the hypothesis that Coke is preferred to Pepsi using a one sided exact test.

n<-4

x<-3

BTest <- binom.test(x,n, alternative = "greater") 

BTest$p.value
#####Ans : 0.3125

####4.Question 4 : 
Infection rates at a hospital above 1 infection per 100 person days at risk are believed to be too high and are used as a benchmark. A hospital that had previously been above the benchmark recently had 10 infections over the last 1,787 person days at risk. About what is the one sided P-value for the relevant test of whether the hospital is *below* the standard?

## Using Poisson test

errors <-10
rate<- 1/100
days<-1787

PTest <- poisson.test(errors,T=days, r=rate, alternative="less")

PTest$p.value
#####Ans : [1] 0.03237153

####5.Question 5 : 
Suppose that 18 obese subjects were randomized, 9 each, to a new diet pill and a placebo. Subjects’ body mass indices (BMIs) were measured at a baseline and again after having received the treatment or placebo for four weeks. The average difference from follow-up to the baseline (followup - baseline) was −3 kg/m2 for the treated group and 1 kg/m2 for the placebo group. The corresponding standard deviations of the differences was 1.5 kg/m2 for the treatment group and 1.8 kg/m2 for the placebo group. Does the change in BMI appear to differ between the treated and placebo groups? Assuming normality of the underlying data and a common population variance, give a pvalue for a two sided t test.


Nx<-9 #dietpill
Ny<-9 #placebo





#####Ans :




















