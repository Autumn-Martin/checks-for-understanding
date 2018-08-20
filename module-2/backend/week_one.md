## Week One - Module 2 Recap

Fork this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  * GET: retrieve a resource from a url
  * POST: create a new resource
  * PUT: update an entire resource
  * PATCH: update part of a resource
  * DELETE: remove/destroy a resource
  Without these verbs, HTTP is stateless!

2. What is Sinatra?
  * Sinatra is a web application library and domain specific language written in Ruby. It is a framework that uses Ruby to serve web apps and uses Rack to interact with the web. It is an alternative to Rails.

3. What is MVC?
  * Model View Controller: a design pattern that allows us to separate software into 3 pieces (data logic, presentation logic, and business logic)

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  * It is ReSTful. A ReSTful route maps HTTP verbs to controller CRUD actions, and depends on both an HTTP verb and the URI.
  * Without this convention, a URI could mean a different different action for one site versus another. It also allows us to do different CRUD actions on the same URI.
  * ReST, or Representational State Transfer is a web architecture style & industry practice. One of its benefits is that it separates the client (or user interface) from the server and data storage, allowing for scalability & portability.

5. What types of variables are accessible in our view templates without explicitly passing them?
  * params variables


6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```

  * ```@count = 1```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  * ```@name= 'Mr.Ed'```

8. What's the purpose of ERB?
  * The purpose of ERB (or embedded ruby) is to allow Ruby code to be used in a plain text document.

9. Why do I need a development AND test database?
  * Having separate databases lets you run tests on test data (or data made solely for the purpose of testing, allowing you to test knowing an expected outcome). This helps us to know that it should be have as expected when pushed to a development environment, which may include a much larger database.

10. What is CRUD and why is it important?
  * Create, Read, Update, Delete
  * CRUD stands for the four major functions of relational database apps.

11. What does HTTP stand for?
  * Hyper Text Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  * ```<%  %>``` indicates to run code in between as Ruby code
  * ```<%=  %>```indicates to run code in between as Ruby code and render the return value

13. What's an ORM? What does it do?
  * Object Relational Mapper: it is a translator between model & database.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  * ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

  Create
    * POST + '/restaurants/new' --> create the new restaurant & redirect
  Read
    * GET + '/' --> render the dashboard
    * GET + '/restaurants' --> render the index page of all restaurants
    * GET + '/restaurants/new' --> render a new restaurant page
    * GET + '/restaurants/:id/edit'--> render a edit restaurant view
  Update
    * PUT/PATCH + '/restaurants/:id'--> update a restaurant & redirect
  Destroy
    * DELETE + '/restaurants/:id' --> delete a restaurant & redirect

16. What's a migration?
  * a file that holds instructions to add a table to database

17. When you create a migration, does it automatically modify your database?
  * No, you have to run ```rake db:migrate```

18. How does a model relate to a database?
  * the schema

19. What is the difference between `#new` and `#create`?
  * `#new` just makes a new instance of an object, whereas `#create` both makes it & saves it.

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
  * SELECT * FROM animals WHERE number_of_legs = 4;

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
  * ```CSV.foreach('films.csv', headers: true, header_converters: :symbol) do |film|
      Film.create(
        id:            film[:id],
        title:         film[:name],
        description:   film[:description],
        )
    end```

23. Given the following hash:
```
activities = {;
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
  * ```activities[:hiking][:supplies] = "granola bar"```

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  * Abstraction: the simplest possible interface is viewed & non-essential info to this interface is hidden
  * Polymorphism: methods may have the same name but different functionality
  * Inheritance: methods may be inherited from parent class to child class to extend functionality without duplication
  * Encapsulation: the important stuff is stored away from the average user (under the hood as private methods)


### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
