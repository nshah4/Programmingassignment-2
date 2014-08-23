Programmingassignment-2
=======================

Programming Assignment 2 - Lexical Scoping
makeCacheMatrix <- function(m = matrix()) {
   i <- NULL
   set <- function(matrix) {
     m <<- matrix
     i <<- NULL
     }
   get <- function() {
     m
     }
   setInverse <- function(inverse) {
     i <<- inverse
     }
   getInverse <- function() {
     i
     }
   list(set = set, get = get, 
               setInverse = setInverse, getInverse = getInverse)
   }

makeCacheMatrix


a <- makeCacheMatrix()


summary(a)



a <- makeCacheMatrix(matrix(c(1,2,12,13), nrow = 2, ncol = 2))


a$get()


cacheSolve <- function (a)
{
  s <- a$getSolve()
  if(!is.null(s))
  {
    message("getting cached data")
    return(s)
  }
  data <- a$get()
  s <- Solve(data)
  a$setSolve(s)
  s
}

cacheSolve

s

cacheSolve <- s

cacheSolve



