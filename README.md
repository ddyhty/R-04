# R-04
#创建向量
4.5:10.5
c(1,2,3:6,c(3,5),7)

#vector函数
vector("numeric",5)
vector("complex",5)
vector("logica",5)
vector("character")
vector("list",5)

numeric(5)
complex(5)
logical(5)
character(5)

#seq函数
seq.int(2,16)
seq.int(2,16,2)
seq.int(16,2,-2)

#seq_len函数
n <-0
2:0
seq_len(n)

#seq_along函数
K <- c("fhg","fty","rth","fe","er","erg")
for(i in seq_along(K))print(K[i])

#length函数
length(5:88)
length(c(TRUE,FALSE,NA,NaN))

A <- c(2,34,6,7,8,9,4)
length(A) <-4
A
length(A) <-7
A

#name函数

c(sn=1,dwg=2,tes=3,"gfh" = 4,5)

x <- 1:5  
names(x) <- c("sn","dwg","tes","gfh" ,"")
x
names(x)
names(1:5)

#[]的用法
x <- (1:5)^2
x[c(2,4)]
x[c(-1,-3,-5)] 
x[c(FALSE,TRUE,FALSE,TRUE,FALSE)] 

names(x) <- c("one","four","nine","sixteen" ,"twentyfive")
x[c("four","sixteen")]

x[c(-1,3)]
x[c(2,NA)]
x[c(FALSE,NA,FALSE,TRUE,FALSE)] 
x[c(-1,-3,NA)]

x[8]
x[2.8]
x[3.2]
x[-2]
x[]

#which函数
which(x>16)
which.min(x)
which.max(x)

#向量循环和反复
##单独数字加向量
1:5 +2
2+1:5
##长向量是短向量的倍数
1:5+1:20
##rep函数
rep(1:5,4)
rep(1:5,each=4)
rep(1:5,times=4)
rep(1:5,length.out =6)
rep.int(1:5,4)
rep.len(1:5,7)

#矩阵和数组
##array函数
 (three_d_array <- array(
 15:50,
 dim = c(3,4,2),
 dimnames = list(
   c("1","2","3"),
   c("ds","dse","ddwe","dwe3"),
   c("ddd","ggg")
 )
))

class(three_d_array)

##matrix函数
(a_matrix <- matrix(
   1:6,
   nrow=2,
   byrow = TRUE,
   dimnames = list(
     c("1","2"),
     c("ds","f","fsr")
   )
 ))

##
class(a_matrix)

dim(three_d_array)
dim(a_matrix)

nrow(a_matrix)
ncol(a_matrix)

length(a_matrix)
length(three_d_array)

dim(a_matrix) <- c(6,1)
a_matrix


 identical(nrow(a_matrix) ,NROW(a_matrix))
 identical(ncol(a_matrix) ,NCOL(a_matrix))

H <- c(1,22,45,667,8,9,90)
nrow(H)
NROW(H)

ncol(H)
NCOL(H)

#行、列
rownames(a_matrix)
colnames(a_matrix)
dimnames(a_matrix)

rownames(three_d_array)
colnames(three_d_array)
dimnames(three_d_array)

#索引数组
a_matrix[1,c("dse","ddwe")]

a_matrix[1,]

a_matrix[,c("dse","ddwe")

#合并矩阵
(another_matrix <- matrix(
   seq.int(3,36,3),
   nrow = 4,
   dimnames =list(
     c("3","4","5","6"),
     c("ad","ds","gr")
   )
 ))
c(a_matrix,another_matrix)
cbind(a_matrix,another_matrix)

rbind(a_matrix,another_matrix)

#数组算术
a_matrix + another_matrix
a_matrix * another_matrix

#t函数
t(a_matrix )

#
a_matrix %*%t(a_matrix)
1:2%o%2:3
outer(1:2,2:3)

(m <- matrix(c(1,2,3,4,5,67,8,6,3),nrow=3))
m^-1
(inverse_of_m<- solve(m))
m %*% inverse_of_m

Q1:如何创建一个包含0,0.25，0.5,0.75和1的向量
A1：seq.int(0,1,0.25)

Q2：描述两种命名向量元素的方式
A2: 1.直接命名，如将向量1命名为apple，即c(apple = 1)
2.在向量创建后用names函数为元素添加名字
如 x <- 1:3
   names(x) <- c(“ds”,”h”,”kl”)


Q3:向量索引中的四种类型是什么？
A3：1.给向量传入一个正数，会返回此位置上的向量元素（其第1个位置是1）
2.传入负数，会返回除了这些位置的其他元素
3.传入一个逻辑向量，会返回一个只包含索引为TRUE的元素的向量
4.对于已经命名的向量，传入命名的字符向量，会返回包含这些名字的元素

Q4：一个3*4*5的数组的长度是多少？
A4：60

Q5：你会用哪个操作来执行这两个矩阵的内积？
A5：使用%*%或crossprod()函数进行

#练习
1.
 x <- (1:20)*((1:20)+1)/2
 names(x) <- letters[1:20]
 x[c("a","e","i","o","u")]

2.
a<- c(seq.int(11,0,-1),seq.int(1:11))
> diag(a)
