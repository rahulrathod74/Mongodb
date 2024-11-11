1. ###### How do you list all the databases present in your MongoDB server?

- show dbs

2. ###### What command is used to create or switch to a database in MongoDB?

- use _database-name_

3. ###### How can you create a collection named "students" in your MongoDB database?

- db.createCollection("students")

4. ##### Write the command to insert a <u>single</u> document into the "students" collection with at least three fields: name, age, and course.

- db.students.insertOne({name: "MASAI",age: 5,course : "Full Stack"})

5. ##### How would you insert multiple documents into the "students" collection in a single command?

- db.students.insertMany([
  {name: "John Doe",age: 8,course : "Full Stack"},
  {name: "Peter Parker",age: 9,course : "Data Science"},
  {name: "MASAI_3",age: 7,course : "Full Stack"}])

6. ##### What command is used to find or read all documents in the "students" collection?

- db.students.find()

7. ##### How can you read or find the first document in the "students" collection?

- db.students.find().limit(1)
- db.students.findOne()

8. ##### Describe the command to update the course field of a specific student named "John Doe" to "Data Science".

- db.students.updateOne(
  {name: "John Doe"},
  {$set:{course: "Data Science"}})

9. ##### What command would you use to increment the age field of all documents in the "students" collection by 1?

- db.students.updateMany(
  {},
  {$inc:{age: 1}}
  )

10. ##### How can you delete a document with a specific name from the "students" collection?[Let's say 'John Doe']

- db.students.deleteOne({name: "John Doe"})

11. ##### Write the command to delete all documents from the "students" collection where the age is greater than or equal to a specific value.[Let's say 7]

- db.students.deleteMany({age:{$gte: 7}})

12. ##### How do you find documents in the "students" collection where the course field is "Data Science"?

- db.students.find({course: "Data Science"})
