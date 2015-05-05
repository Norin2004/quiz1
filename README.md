# quiz1
rprog-014

# question 1
R was developed by statisticians working at

a. Microsoft
b. Johns Hopkins University
c. The University of Auckland
d. StatSci

# answer
The University of Auckland 

# Explanation
The R language was developed by Ross Ihaka and Robert Gentleman who were statisticians at the University of Auckland in New Zealand.

# Question 2
The definition of free software consists of four freedoms (freedoms 0 through 3). Which of the following is NOT one of the freedoms that are part of the definition?

a. The freedom to restrict access to the source code for the software.
b. The freedom to redistribute copies so you can help your neighbor.
c. The freedom to run the program, for any purpose.
d. The freedom to improve the program, and release your improvements to the public, so that the whole community benefits.

# answer
The freedom to restrict access to the source code for the software 

# Explanation
This is not part of the free software definition. Freedoms 1 and 3 require access to the source code.

# Question 3
In R the following are all atomic data types EXCEPT

a. numeric
b. character
c. table
d. integer 

# answer
table 

# Explanation
'table' is not an atomic data type in R.

# Question 4
If I execute the expression x <- 4 in R, what is the class of the object `x' as determined by the `class()' function?

a. complex 			
b. numeric 	 	
c. vector 			
d. matrix

# answer
numeric

# Explanation
> x <-4
> class(x)
[1] "numeric"

# Question 5
What is the class of the object defined by x <- c(4, TRUE)?

a. logical
b. numeric
c. character
d. interger

# answer
numeric 

# Explanation
The numeric class is the "lowest common denominator" here and so all elements will be coerced into that class.
*R does automatic coercion of vectors so that all elements of the vector are the same data class

> x <- c(4, TRUE)
> class(x)
[1] "numeric"


# Question 6
If I have two vectors x <- c(1,3, 5) and y <- c(3, 2, 10), what is produced by the expression rbind(x, y)?

a. a vector of length 2 			
b. a matrix with two rows and three columns 		
c. a 2 by 2 matrix 			
d. a 3 by 2 matrix

# answer
a matrix with two rows and three columns 

# Explanation
The 'rbind' function treats vectors as if they were rows of a matrix. It then takes those vectors and binds them together row-wise to create a matrix.

> x <- c(1, 3, 5)
> y <- c(3, 2, 10)
> rbind(x,y)
  [,1] [,2] [,3]
x    1    3    5
y    3    2   10

# Question 7
A key property of vectors in R is that

a. elements of a vector can only be character or numeric 			
b. the length of a vector must be less than 32,768 			
c. elements of a vector can be of different classes 			
d. elements of a vector all must be of the same class

# answer
elements of a vector all must be of the same class

# Question 8
Suppose I have a list defined as x <- list(2, "a", "b", TRUE). What does x[[1]] give me?

a. a list containing the number 2.  	
b. a numeric vector containing the element 2. 			
c. a list containing a numeric vector of length 1. 			
d. a list containing the letter "a".

#answer
a list containing a numeric vector of length 1

# Explanation
> x <- list(2, "a", "b", TRUE)
> x[[1]]
[1] 2

# Question 9
Suppose I have a vector x <- 1:4 and a vector y <- 2. What is produced by the expression x + y?

a. a numeric vector with elements 1, 2, 3, 6. 			
b. a numeric vector with elements 3, 4, 5, 6. 	 	
c. a numeric vector with elements 3, 2, 3, 6. 			
d. a numeric vector with elements 3, 2, 3, 4.

# answer
a numeric vector with elements 3, 4, 5, 6.

# Explanation
> x <- 1:4
> y <- 2
> x+y
[1] 3 4 5 6

# Question 10
Suppose I have a vector x <- c(17, 14, 4, 5, 13, 12, 10) and I want to set all elements of this vector that are greater than 10 to be equal to 4. What R code achieves this?

a. x[x >= 11] <- 4 			
b. x[x >= 10] <- 4 	
c. x[x < 10] <- 4 			
d. x[x > 4] <- 10

# answer
x[x >= 11] <- 4

# Explanation
> x <- c(17, 14, 4, 5, 13, 12, 10)
> x[x >= 11] <- 4 
> x
[1]  4  4  4  5  4  4 10

# Question 11
In the dataset provided for this Quiz, what are the column names of the dataset?

a. Ozone, Solar.R, Wind 			
b. 1, 2, 3, 4, 5, 6 			
c. Month, Day, Temp, Wind 			
d. Ozone, Solar.R, Wind, Temp, Month, Day

# answer
Ozone, Solar.R, Wind, Temp, Month, Day

# Explanation
You can get the column names of a data frame with the `names()' function

> z<-read.csv(file.choose())
> names(z)
[1] "Ozone"   "Solar.R" "Wind"    "Temp"    "Month"   "Day" 

# Question 12
Extract the first 2 rows of the data frame and print them to the console. What does the output look like?

a.  Ozone Solar.R Wind Temp Month Day
1    41     190  7.4   67     5   1
2    36     118  8.0   72     5   2

b.  Ozone Solar.R Wind Temp Month Day
1    18     224 13.8   67     9  17
2    NA     258  9.7   81     7  22

c.  Ozone Solar.R Wind Temp Month Day
1     7      NA  6.9   74     5  11
2    35     274 10.3   82     7  17

  Ozone Solar.R Wind Temp Month Day
1     9      24 10.9   71     9  14
2    18     131  8.0   76     9  29

# Explanation
You can extract the first two rows using the [ operator and an integer sequence to index the rows.

# answer
> z[c(1,2),]
  Ozone Solar.R Wind Temp Month Day
1    41     190  7.4   67     5   1
2    36     118  8.0   72     5   2

# Question 13
How many observations (i.e. rows) are in this data frame?

a. 153 		
b. 129 			
c. 45 			
d. 160

# Explanation
You can use the `nrow()' function to compute the number of rows in a data frame.

# answer

> nrow(z)
[1] 153

# Question 14
Extract the last 2 rows of the data frame and print them to the console. What does the output look like?

a.    Ozone Solar.R Wind Temp Month Day
152    11      44  9.7   62     5  20
153   108     223  8.0   85     7  25

b.    Ozone Solar.R Wind Temp Month Day
152    31     244 10.9   78     8  19
153    29     127  9.7   82     6   7

c.    Ozone Solar.R Wind Temp Month Day
152    18     131  8.0   76     9  29
153    20     223 11.5   68     9  30

d.	    Ozone Solar.R Wind Temp Month Day
152    34     307 12.0   66     5  17
153    13      27 10.3   76     9  18

# Explanation
The `tail()' function is an easy way to extract the last few elements of an R object.

# answer
> tail(z, 2)
    Ozone Solar.R Wind Temp Month Day
152    18     131  8.0   76     9  29
153    20     223 11.5   68     9  30

# Question 15
What is the value of Ozone in the 47th row?

a. 34 			
b. 18 			
c. 21 	
d. 63

# Explanation
The single bracket [ operator can be used to extract individual rows of a data frame

# answer
> z[47,]
   Ozone Solar.R Wind Temp Month Day
47    21     191 14.9   77     6  16

# Question 16
How many missing values are in the Ozone column of this data frame?

a. 37 	 	
b. 78 			
c. 9 			
d. 43

# Explanation
The `is.na' function can be used to test for missing values

# answer
> sub <- subset(z, is.na(Ozone))
> nrow(sub)
[1] 37

# Question 17
What is the mean of the Ozone column in this dataset? Exclude missing values (coded as NA) from this calculation?

a. 18.0 			
b. 42.1 		
c. 53.2 			
d. 31.5

# Explanation
The `mean' function can be used to calculate the mean.

# answer
> mean(z$Ozone[!is.na (z$Ozone)])
[1] 42.12931

# Question 18
Extract the subset of rows of the data frame where Ozone values are above 31 and Temp values are above 90. What is the mean of Solar.R in this subset?

a. 334.0 			
b. 185.9 			
c. 205.0 			
d. 212.8

# Explanation
You need to construct a logical vector in R to match the question's requirements. Then use that logical vector to subset the data frame.

# answer
> w <- subset(z,Ozone > 31 & Temp > 90, select = Solar.R)
> mean(w$Solar.R)
[1] 212.8

# Question 19
What is the mean of "Temp" when "Month" is equal to 6?

a. 85.6 			
b. 90.2 			
c. 79.1 	
d. 75.3

# answer
79.1

#Explanation
> d <- subset(z, Month==6, select = Temp)
> mean(d$Temp)
[1] 79.1

# Question 20
What was the maximum ozone value in the month of May (i.e. Month = 5)?

a. 18 			
b. 100 			
c. 115 	
d. 97

# answer
115

# Explanation
> max(z$Ozone[z$Month ==5 & !is.na(z$Ozone)])
[1] 115
