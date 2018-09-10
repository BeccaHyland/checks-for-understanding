## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
* A cookie is a small data storage unit that a website sends to each client. It contains identification info such as the user's password / username. 
2. What’s the difference between a session and a cookie?
* The session contains a larger amount of information about the client's preferences and history that won't fit in the cookie. Unlike the cookie, it is usually stored remotely, with one exception being Rails. 
3. What’s a flash and when do you want to use flashes?
* A flash is a temporary (usually) message to the user which is administered by the controller and not the view. 
4. Why do people say “HTTP is stateless”?
* HTTP is stateless because it has no memory of client requests or actions. 
5. What’s authentication? Explain.
* Authentication is logging in / logging out of an application. Its purpose is for security and to give users access to only their own information and/or site customization.
6. What’s the difference between authentication and authorization?
* Authorization means that some app functionality / pages will only be available to admin users, not regular users, and some app functionality will not be available to a visitor who visits the site without an account.
7. What’s a before filter?
* A before filter sets the first condition in a file's logic. 
8. How do we keep track of a user once they’ve logged in?
* The session keeps track of the user by storing selected actions the user does.
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
* Namespacing is different than nesting resources because namespacing creates a duplicate resource with difference functionality for the user or admin. Nested routes allow pages content to be filtered. 
10. At a high level, what tools can you use to implement authorization? How would you use them?
* To implement authorization, you can use a before filter in an admin base controller (redirecting the user to a 404 message if they are not an admin), namespacing and methods in the application controller such as current_user? and current admin? . You will also need an admin version of some user controllers depending on the added admin functionality needed.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
* An enum allows each user to be assigned a role, which is stored in the session. Declare an enum in the user model. 
12. What are some strategies you can use to keep your views DRY?
* Form partials are one way to keep your views DRY. Another important way is to write code used by all pages, like the nav bar, in the application.html.erb file, which is located in views/layouts.


### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
set the array equal to a variable such as `days`
* names = days.map do |day|
day[:holiday][:name]
end
* names.sort
* .sort
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
* for $300 you can use #gsub(/\D/, '')
* not sure about 300.00


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
--> something in between here :)
* I feel overwhelmed by the content presented this week

