## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  ActiveRecord is a Ruby library for working with relational SQL databases.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  Team.all, Team.find(1), Team.order, these methods are accessed through the inheritance of ActiveRecord methods.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  Team.find(4).name
4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  Team.where(owner_id: 4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  It will be a many to many relationship. Many students have many teachers. There will be a join table called TeacherStudents that link the two.
6. Define foreign key, primary key, and schema.
  A foreign key is an identifier for the primary key of a related table. The primary key identifies each row of a table. The schema is the overall structure of your database tables.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
  The foreign key of one table holds the primary key of another table. This is how we relate databases and access data through these relationships.
8. What are the parts of an HTTP response?
  Status- protocol, status code, status text
  headers- give more info about the response
  body- content



### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
  .where, finds a condition in the model
  .order, orders things
  .average, averages things
  .limit, limits the amount of results returned from a query
  .find, finds a thing
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
  migration - builds a migration file
  create - creates your databases
  migrate - fills your database tables based on migrations
3. What two columns does `t.timestamps null: false` create in our database?
  created_at, updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  school has many teachers or also possible, many schools have many teachers
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
  maybe a description of the relationship
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
  Things that are being repeated. Gotta DRY up that code.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
