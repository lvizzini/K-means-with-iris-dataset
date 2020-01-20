# K-means-with-iris-dataset
summary(iris)
boxplot(iris.new)

normalize <- function(x){
  return ((x-min(x))/(max(x)-min(x)))
}

iris.new<-iris[,1:4]

iris.new$Sepal.Length<- normalize(iris$Sepal.Length)
iris.new$Sepal.Width<- normalize(iris$Sepal.Width)
iris.new$Petal.Length<- normalize(iris$Petal.Length)
iris.new$Petal.Width<- normalize(iris$Petal.Width)
boxplot(iris.new)

result<- kmeans(iris.new,3)
