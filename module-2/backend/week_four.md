## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  A cookie is a small string file(4kb) used to store data client side to make the
  user experience more pleasurable. For example storing browsing habits, favorites, etc.
2. What’s the difference between a session and a cookie?
  A session is similar to a cookie but it is stored server side and is hidden.
3. What’s a flash and when do you want to use flashes?
  A flash is a notification that appears in the browser, you want to use it to alert
  a user of something. e.g. something executed succesfully or something failed
4. Why do people say “HTTP is stateless”?
  HTTP is stateless because it sends a request to the server every time for data.
5. What’s authentication? Explain.
  Authentication is essentially giving the browser a role, allowing them to access more content.
6. What’s the difference between authentication and authorization?
  Authorization is similar to authentication but extends it to different roles, allowing
  different content to be accessed depending on the role.
7. What’s a before filter?
  A before filter or before action is code run before any controller actions,
  so you could verify a user is indeed authorized to access that controller action
  using said filter.
8. How do we keep track of a user once they’ve logged in?
  Session[:user_id]
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  You want to namespace to group controllers under a certain category. For example you may
  want to namespace a set of admin controllers. You want to nest a resource that are logically
  the child resource of other resources. E.g. Magazine has many ads you'd want to nest
  ads under magazines.
10. At a high level, what tools can you use to implement authorization? How would you use them?
  There are several gems you can use, such as cancan or pundit.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  An enum is used in a situation where something can be in a handful of states, e.g.
  a phone number could be home, office, mobile, or an order could be shipped, pending, etc.
  In order to use an enum you need to use an integer. You declare an enum in the
  model file.
12. What are some strategies you can use to keep your views DRY?
  Use Render, templates, etc.



### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

puts array.sort_by { |holiday| holiday[:name] }

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
  "$300".strip_dollar_sign.to_i


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
