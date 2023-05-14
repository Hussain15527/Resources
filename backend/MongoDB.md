# Lecture: 
## [MongoDB (Bro Code)](https://www.youtube.com/watch?v=c2M-rlkkT5o)





# Quick Notes:
## 1. `db.createCollection(<collection name>`
to create a collection of desired name


<br>

## 2. `use <collection name>`
to change the current pointer to desired collection

<br>

## *say the collection name to be `students`* ##
## 3. Insertion ##
`db.students.insertOne({name:"mujtaba",age:20,cgpa:8})` 

This adds this object in the collection `students` 


<br>

## 4(a). Print 
`db.students.find()`
Prints all the element of the collections `students`

## 4(b). Print with condition 
`db.students.find({age:19})`
Prints all the students whose age is 19.

<br>

## 5. Sort  
`db.students.find().sort({<attribute_name>:1/-1})`
sorting in asscending, use `1`, and `-1` for descending.

<br>

## 6. Limit
`db.students.find().limit(<number>)`
Prints the `number` numbers of elements of the collections 

## 7. Projection
`dp.students.find({},{name:true})` prints only name
`dp.students.find({},{name:true,age:true})` print name and age
