## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
* AR is an Object Relational Mapper which simplifies SQL queries and integrates with Ruby on Rails.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
* You can call ActiveRecords on Team such as #all and #find.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
* Team.find(4)
* Team.select(:owner).where(id: 4)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
* Owner.where(team_id: 4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
* A teacher has many students.
* A student belongs to a teacher. 
* The foreign key teacher_id will appear in the Student class.
6. Define foreign key, primary key, and schema.
* The primary key is the ID that all rows in a database have, either automatically incremented or assigned from a seed file, test setup, or other manual instance creation. The foreign key is when the id of a second class appears in the first class to associate instances together.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
* The primary key in Table 1 can appear in another table as a foreign key associating that instance of Table 1 with an instance of Table 2.
8. What are the parts of an HTTP response?
First the request from client or response from server, then the header, then the body (optional). 


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel overwhelmed by the content presented this week - but I enjoy the content! Absorbing and trying things out!
