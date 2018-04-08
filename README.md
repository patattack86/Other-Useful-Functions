# Other-Useful-Functions
Useful functions 

```{r}
#easy function returning useful statistical moments
mymoments <- function(x){
  a <- moments::kurtosis(x)
  b <- moments::skewness(x)
  c <- mean(x)
  d <- sd(x)
  e <- var(x)
  result <- list(a=a, b=b, c=c, d=d, e=e)
  return(result)

}


#Calculates RMSE quickly and efficiently
RMSE = function(m, o){
  sqrt(mean((m - o)^2))
}

#simple function which returns the mode
Mode <- function(x) {
  ux <- unique(x)
  ux[which.max(tabulate(match(x, ux)))]
}
```
