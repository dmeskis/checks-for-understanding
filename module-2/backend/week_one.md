## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  Get- Read
  Put- Update/replace
  Post- Create
  Patch- Update/modify
  Delete- Delete

2. What is Sinatra?
  Sinatra is a lightweight web framework built on top of Rack.
3. What is MVC?
  Model, views, controllers. It is a software design pattern that separates
  an application into parts and divides the logic amongst these parts.
4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  So that we can be RESTful.
5. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables.
6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  @count = '1'
7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  name = 'Mr. Ed' :locals => {:name => params[:name]}
8. What's the purpose of ERB?
  Embedded ruby allows us to use ruby code in our HTML to assist in rendering
  our web page.
9. Why do I need a development AND test database?

10. What is CRUD and why is it important?
  Create. Read. Update. Destroy. It is a very important concept applied throughout
  the programming world. For example REST is a superset of CRUD. It also affects
  databases and end users.
11. What does HTTP stand for?
  Hyper text transfer protocol
12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <% %> <%= %>, the second is an implicit puts operation.
13. What's an ORM? What does it do?
  Object Relational mapping. It is a technique that lets you query and manipulate
  data from a database using an object-oriented paradigm.
14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ActiveRecord
15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  Get - read, put - update, post - create, delete -delete, redirect
16. What's a migration?
 An incremental change to a database.
17. When you create a migration, does it automatically modify your database?
  No, you must run rake db:migrate
18. How does a model relate to a database?
  A model usually refers to an organization of data that is stored in your database.
  Within this model can be logic to manipulate that data.
19. What is the difference between `#new` and `#create`?
  New creates an instance of an object, create tries to do that as well as save it
  to the database.
20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    `
    SELECT * FROM animals
21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?
  SELECT * FROM animals WHERE number_of_legs=4

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
  films = CSV.read('films.csv')
  films.shift
  films.each do |film|
    film.create(id: film[0], title: film[1], description: film[2])
23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?

  activities[:hiking][:supplies] << 'granola bar'

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  encapsulation, data abstraction, data hiding, inheritance

### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
