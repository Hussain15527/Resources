# Lecture: 
## [MongoDB (Bro Code)](https://www.youtube.com/watch?v=c2M-rlkkT5o)





# Quick Notes:
## 1. Creation 
`db.createCollection(<collection name>`
to create a collection of desired name


<br>

## 2. Change pointer`
`use <collection name>`
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


<br>

## 7. Projection
`dp.students.find({},{name:true})` prints only name
`dp.students.find({},{name:true,age:true})` print name and age
  
<br>
  
  
## 8. Filter and update
  `dp.students.updateOne({filter},{update})`
  `filter` is for finding elemetns
  `update` update the value of any attribute
  ### example:
  `dp.students.updateOne({name:"mujtaba hussain"},{$set:{age:90}})`<br>
  here `mujtaba hussain` is choosen from the collections and its `age` is changed to 90.
  
  <br>
  
## 9. Update Many
  `db.students.updateMany({fulltime:{$exists:false}},{$set:{fulltime:false}})`
  
  This code finds all for which `fulltime`  does not exist and then set `fulltime` to false
  
  
## 10. Delete:
  `dp.students.deleteOne({name:"sonu"})` <br>
  delets the any item that as name as `sonu`
  
  <br>
  
  `dp.students.deleteMany({salary:{$exists:false}})` <br>
  deletes all the items which does not have salary attribute
  
 <br>
  
 ## 11. comparrison:
  `dp.students.find({age:{$lt:20}})` <br>
  
  gives all the items whose age is less than 20. <br>
  
  ``` 
  lt : less than
  lte: less than and equal to
  gt: greater than
  gte: greater than and equal to 
  et: equal to 
  ne: not equal to
  ```
  
  <br>
  
## 12. Index
  `db.students.createIndex(name:1)` <br>
  
  create the index in the asscending order of the namw
  
