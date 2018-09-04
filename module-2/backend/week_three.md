## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
* rails new name_of_projects
2. What do Models generally inherit from in rails?
* ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
* ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
* horses/:id
5. What rake task is useful when looking at routes, and what information does it give you?
* `rails routes` tells you all the paths for web pages you made available when you added them to config/routes.rb
6. What is an example of a route helper? When would you use them?
* a route helper is the suffix `_path` added to the end of the route prefix listed in rails routes. You can use them in the controller to redirect, in the views for links, and for testing with Capybara.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* I have not tried the `_url` for any purpose so I'm not sure.
8. What are strong params and why are they necessary?
* Strong params are required by Rails whenever you create an object. This is for security so a malicious user cannot inject anything harmful into your database.
9. What role does `form_for` play in helping us create our forms?
* `form_for` is the first line of a form, we have used forms to take input when creating or editing an instance.
10. How does `form_for` know where to submit the user's input?
* It knows because of the arguments it takes. The last argument tells the form what object to post to.
11. Create a form using a `form_for` helper to create a new `Horse`.
`<% form_for @horse do |f| %>
<%= f.label :name %>
<%= f.text_field :name %>
<%= f.label :breed %>
<%= f.text_field :breed %>
<%= f.label :birthday %>
<%= f.date_field :birthday %>
<%= f.submit %>`
12. Why do we want to validate our models?
* We need to validate our models to be sure that any row we enter into the database has the minimum amount of functions that it will not cause errors in our program.
13. What are the steps of the DNS lookup?
* First the client's device checks within its cache to see if it knows where to find the domain name. If not, the client's device checks with the following sources in order: root, TLD, and finally if necessary Authoritative, which confirms domain names with the reigstrar.

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `
  * My answer:
  `within(.personal-info) do
    expect(page).to have_content("#{@person.name}")
   end`
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?
`@horse.move.prance` I am not sure, this question is unclear to me.
16. Given the following hash:
```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
* You need to call one key to return true and chain two keys to return 3.
17. What is inheritance?
* Inheritance is how a model can use the methods of another model.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week - so I am focusing on small pieces one at a time.
