## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  rails new <folder name>
2. What do Models generally inherit from in rails?
  ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
  ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  resources :horse, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
  rake routes, it shows us the path helper, uri pattern, and controller action
6. What is an example of a route helper? When would you use them?
  objects_path would take us to an index of all objects. use them throughout our app
  to assist in routing and also our tests
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  path is relative while url is absolute
8. What are strong params and why are they necessary?
  strong params are parameters that the developer has limited in use of model assignment.
  they prevent us from trying to pass in invalid parameters or extraneous information into
  our models.
9. What role does `form_for` play in helping us create our forms?
  form_for is a rails method that builds out the html for our forms. Thank you rails!
10. How does `form_for` know where to submit the user's input?
  Based on the object being passed in, e.g. if your passing in a new instance of something
  it would take you to the create controller action.
11. Create a form using a `form_for` helper to create a new `Horse`.
  <%= form_for Horse.new do |f| %>
    <%= f.label :name %>
    <%= f.text_field :name %>

    <%= f.label :breed %>
    <%= f.text_field :breed %>

    <%= f.label :age %>
    <%= f.text_field :age %>

    <%= f.label :age %>
    <%= f.text_field :age %>

    <%= f.submit "Create a Horse" %>
  <% end %>
12. Why do we want to validate our models?
  We validate our models to ensure that their attributes are being properly stored
  in the database.
13. What are the steps of the DNS lookup?
  Our browser sends a request to our ip who sends a request to the root server
  who sends a request to the top level domain server who sends it to the authoritative
  name server who then sends this information back down the path to us.
### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `

  within "#personal-info" do
    expect(page).to have_content(@person.name)
  end
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  Horse.move.prance

16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?

  To return true: furniture[:table][:purchased]
  To return 3:    furniture[:table][:height]

17. What is inheritance?
  Inheritance is when a class is assigned a parent class and then has access to all
  those parent methods.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week
