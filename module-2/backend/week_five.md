### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
* In the controller, position in the message in the action method that you want to display the message to the user whenever it is run. In your application.html.erb layout, you also need to specify where on the page you consistently want the various flash messages to display. 

2. Where is cart information/temporary information usually stored?
* Cart and other temporary user data is usually stored in a cookie and additional information about the user is stored (usually remotely, except with Rails) in a session. 

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
* One reason not to store a cart in the database is because the behavior of users entering items into their cart is volatile in the sense that users frequently add and remove items in and out of their cart. This volume of changes would not be efficient for the database to handle. 

4. What is the purpose of the asset pipeline?
* The asset pipeline is how we format and introduct the images and styling we want to be read and utilizd by our app. I would like to review and learn more about this.

5. Why do we precompile our assets?
* Since Rails is comparatively slow with regard to fetching data, precompiling our assets squishes similar filetypes together and does other memory-saving actions, such as shortening variable names, to improve app performance.

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
* the stylesheet has a library and defaults for what styling options are available to you. 
* javascript - I assume this makes javascript available to your app
* image_tag - this displays an image

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
* A great readme shows that YOU understand your code well enough to explain it to someone else, it makes your code usable/intelligible to someone else, and it allows you to guide the story of what the reader learns about your code (and by extension, what they learn about you as a programmer).  

8. What are the top four accessibility issues that we as developers should be aware of?
I am not sure if these are in the top four, but I think developers should be aware of: 
* Responsive design
* With html, using semantic tags so that accessibility devices can interpret your pages helpfully for the user who needs accessibility support.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
* It is a callback. I do not recall having used `before_save` in a Rails app. I will assume it performs a save action before running the next line of code. 

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```
* I cannot recall previously using scope unless I have done it without knowing the term 'scope.'
11. What is the difference between a scope and a class method?
* See above

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  * `ruby[:cart]['48'] = 4`
  12b. How would you increase the quantity of item 29?
  * `ruby[:cart]['29'] += 1`
  12c. How would you find out how many items your user is thinking about purchasing?   
  * Access the cart session
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications? 
* I need to review polymorphism
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
* with a gsub


### Self Assessment:
* I answered the questions without resources to the best of my current ability, and self-identified when I did not know the answer.

Choose One:
* I feel overwhelmed by the content presented this week - I want to spend more time on all of it!

