## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb. --
* GET - display a read-only view
* POST - create a piece of data from input
* PUT - replace (update) data
* PATCH - alter (update) data
* DELETE - delete

2. What is Sinatra? --
* Sinatra is a website-building framework for Ruby developers. It saves time with built-in structures to access the web and combine Ruby with styling languages. 

3. What is MVC? --
* Model View Controller is a design pattern for developing software. It makes software easier to collaborate on and maintain by consistently organizing the progrma logic into three categories: View, the presentation logic; Model, the data logic; and Controller, the "showrunner" or "business logic" that combines objects from the models and views to create commands for the program to carry out.

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes? --
* This makes our program intelligible to other developers. It is helpful to follow conventions so everyone is on the same page with code that can be understood by more than one person. 

5. What types of variables are accessible in our view templates without explicitly passing them? --
* Instance variables that were created in the controller path or in the model files are available to the view templates.

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template? --

  ```ruby
  get '/horses' do
  @count = 1
  @name = "Mr. Ed"
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view? (see above)

8. What's the purpose of ERB? --
* An ERB file allows the writing of HTML and Ruby in the same file, so you can set up a page with HTML and call Ruby inside the HTML as needed. However it is recommended to do as little Ruby logic as possible in these view files. 

9. Why do I need a development AND test database?--
* I think the test database only holds any table data that you created in your setup, while the development database's tables will have a different dataset, such as from a seed file, and the two need to be kept separate so you can write tests based on only your own predefined data (setup).

10. What is CRUD and why is it important?--
* Create, Read, Update, and Destroy / Delete are the four necessary actions for any app that uses a database. Apps we develop must be able to perform these functions in order to access and maintain the database.

11. What does HTTP stand for?--
* Hypertext Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?--
* <% RUBY OPERATIONS HERE %> <%= RUBY OPERATION TO HAVE ITS RETURN VALUE DIRECTLY OUTPUT TO SCREEN HERE %>

13. What's an ORM? What does it do?--
* Object Relational Mapper. It converts relational data from the database into Ruby objects in real time. The developer doesn't have to think about raw data as much, and can isntead interact with objects using attributes and methods. 

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?--
* Active Record

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.--
* get "/' -view the homepage
* get '/index-kind-of-name' - view the index of model instances
* get '/new'- view create new instance page
* post '/index-kind-of-name' - create and save a new instance
* get '/index/:id'- see one instance of the model
* get '/index/:id/edit' - view the edit page for one instance, or maybe this is instead available directly on the SHOW
* put/patch '/index/:id' - edit an instance and store the change
* delete '/index/:id - delete an instance

16. What's a migration?--
* A migration is a new version of the database that you create each time there is a change to one of the app models. 

17. When you create a migration, does it automatically modify your database?--
* Yes, if you first create_migration with a name, make your changes in that file, and then db:migrate, this sequence updates the schema file which the database reads to know its organization

18. How does a model relate to a database?
* A model is the blueprint for each instance of an object, and each instance becomes a row in a table in the database. 

19. What is the difference between `#new` and `#create`?
* #new makes a new object whereas #create makes AND saves the new object.

20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
  
    `
    * SELECT * FROM animals;

21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?
SELECT * FROM animals
* WHERE number_of_legs = 4;

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film? -- In a seeds.rb file, require the film.rb model that you made to reflect the csv contents and your program needs, add this to seeds.rb:
```CSV.foreach(films.csv, headers: true, header_converters: :symbol) do |film|
    Film.create(id:          film[:id],
                title:       film[:title],
                description: film[:description])
 ```
  

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
* `activities[hiking][supplies] << 'granola bar'`

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.
I do not have a strong memory of this. 

### Self Assessment:
Choose One: (erase the others)
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel overwhelmed by the content presented this week
