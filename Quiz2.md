## 06 Statistical Inference - Quiz 2 

####1.Question 1 : What is the variance of the distribution of the average an IID draw of n observations from a population with mean μ and variance σ2

#####Ans : σ2 / n 


####2. Question 2 : Suppose that diastolic blood pressures (DBPs) for men aged 35-44 are normally distributed with a mean of 80 (mm Hg) and a standard deviation of 10. About what is the probability that a random 35-44 year old has a DBP less than 70?

#####Ans

DBP<-70

sd<-10

we have X=N(mu=80, var=sd^2)

mu<-80

pnorm(DBP, mu, sd) = around 16%

#### 3. Question 3 : Brain volume for adult women is normally distributed with a mean of about 1,100 cc for women with a standard deviation of 75 cc. What brain volume represents the 95th percentile?

#####Ans : 

Use Qnorm.

mu<-1100

sd<-75

var<-sd^2

quant<-0.95

qnorm(quant, mu, sd) = 
#####1223.364

#### 4. Question 4 : Refer to the previous question. Brain volume for adult women is about 1,100 cc for women with a standard deviation of 75 cc. Consider the sample mean of 100 random adult women from this population. What is the 95th percentile of the distribution of that sample mean?

#####Ans : 

u<-1100

sd<-75

var<-sd^2

quant<-0.95

stderr<- sd/ sqrt(100)  <!---  The 100 is the value of n -->

qnorm(quant, mu, stderr ) = 
#####1112.336

#### 5. Question 5 : You flip a fair coin 5 times, about what's the probability of getting 4 or 5 heads?

#####Ans : 
considering lower.tail	=logical; if TRUE (default), probabilities are P[X ≤ x], otherwise, P[X > x

lets use BINOM dis

n<-5

p<-0.5

quant<-3

1-pbinom(quant, n, p)  <!--- or use pbinom(quant, n, p, lower.tail=FALSE) -->
#####0.1875 which is 19%

#### 6. Question 6 : The respiratory disturbance index (RDI), a measure of sleep disturbance, for a specific population has a mean of 15 (sleep events per hour) and a standard deviation of 10. They are not normally distributed. Give your best estimate of the probability that a sample mean RDI of 100 people is between 14 and 16 events per hour?

#####Ans : using CLT theorem

mu<-15

sd<-10

var<-sd^2

n<-100

stderr<- sd/ sqrt(n)

pnorm(16, mu, stderr) - pnorm(14, mu, stderr)  == around 68%

#### 7. Question 7 : Consider a standard uniform density. The mean for this density is .5 and the variance is 1 / 12. You sample 1,000 observations from this distribution and take the sample mean, what value would you expect it to be near?

#####Ans : 

Logically it is the same or by qnorming

qnorm(0.5, mean=0.5, sd= (1/12) / sqrt(1000) )  gives 0.5


#### 8. Question 8 : The number of people showing up at a bus stop is assumed to be Poisson with a mean of 5 people per hour. You watch the bus stop for 3 hours. About what's the probability of viewing 10 or fewer people?

#####Ans : 

X is poisson dist. (refer lecture 06/03 on poisson)

mean <- 5

t <- 3

quant<-10

ppois(quant, lambda= mean * t) = 
##### 0.1184644 which is around 0.12




