## 06 Statistical Inference - Quiz 3

####1.Question 1 :In a population of interest, a sample of 9 men yielded a sample average brain volume of 1,100cc and a standard deviation of 30cc. What is a 95% Student's T confidence interval for the mean brain volume in this new population?
xAVG<-1100

sd<-30

n<-9

alpha<-0.05

ts<-qt(1 - alpha / 2, n - 1) 

round(xAVG + c(-1, 1) * ts * sd / sqrt(n))

#####Ans : [1077,1123]

####2.Question 2 : A diet pill is given to 9 subjects over six weeks. The average  difference in weight (follow up - baseline) is -2 pounds. What would the standard deviation of the difference in weight have to be for the upper endpoint of the 95% T confidence interval to touch 0?

xAVG<- -2

n<- 9

alpha<-0.05

ts <- qt(1 - alpha / 2, n - 1)
s <- -xAVG*sqrt(n) / ts


#####Ans : 2.601903
