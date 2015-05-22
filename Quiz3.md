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

####3.Question 3 : n an effort to improve running performance, 5 runners were either given a protein supplement or placebo. Then, after a suitable washout period, they were given the opposite treatment. Their mile times were recorded under both the treatment and placebo, yielding 10 measurements with 2 per subject. The researchers intend to use a T test and interval to investigate the treatment. Should they use a paired or independent group T test and interval?

Independent  would mean unrelated. Paired is for same group with diff tests so 

#####Ans : A PAIRED INTERVAL

####4.Question 4 : In a study of emergency room waiting times, investigators consider a new and the standard triage systems. To test the systems, administrators selected 20 nights and randomly assigned the new triage system to be used on 10 nights and the standard system on the remaining 10 nights. They calculated the nightly median waiting time (MWT) to see a physician. The average MWT for the new system was 3 hours with a variance of 0.60 while the average MWT for the old system was 5 hours with a variance of 0.68. Consider the 95% confidence interval estimate for the differences of the mean MWT associated with the new system. Assume a constant variance. What is the interval? Subtract in this order (New System - Old System).




#####Ans :


