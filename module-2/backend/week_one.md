## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
Get, Post, Put, Patch, Delete
2. What is Sinatra?
A web framework that allows parsing of requests for web pages
4. What is MVC?
Model-View-Controller pattern of laying out parts of a web application
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
It allows other automated tools and sinatra itself to locate things automatically as well as readability and understanding for other programmers without having to figure out the structure.
6. What types of variables are accessible in our view templates without explicitly passing them?
Instance and class variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = '1'
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses' do
    erb :index, locals: { name: 'Mr. Ed' }
  end
  ```

9. What's the purpose of ERB?
  Create an HTML file with ruby injects
10. Why do I need a development AND test database?
  Test database allows you to run testing on a clean database with only injected information without disrupting the development database used to mimic the production database
11. What is CRUD and why is it important?
  create, read, update, destroy
  It's the actions that can be taken on a database information
12. What does HTTP stand for?
hyper text transfer protocal
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= %> prints result
<% %> runs but doesn't print
14. What's an ORM?
Object relationship model
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
Active Record
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

GET to '/restaurants' lists restaurants
GET to '/restaurants/new' opens page to create a new restaurant
POST to '/restaurants' creates a new restaurant
GET to '/restaurants/:id' opens a single restaurant
GET to '/restaurants/:id/edit' opens page to make changes to a single restaurant
PUT to '/restaurants/:id' updates a single restaurant
DELETE to '/restaurants/:id' removes a restaurant

17. What's a migration?
  instructions that modifies a database
18. When you create a migration, does it automatically modify your database?
  no it creates a file with instructions for how to modify it
19. How does a model relate to a database?
  it's a ruby object that represents a table in the database
20. What is the difference between `#new` and `#create`?
  new has to be saved afterwards. create runs both new and save

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

CSV.foreach('films.csv', headers: true, header_converters: symbol) do |film|
    Flim.create(film)
end

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```

How would I add 'granola bar' to things you should have when hiking?

 activities[:hiking][:supplies] << 'granola bar'

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Encapsulation - restricting access to only the parts of a program that need that information
Abstraction - to remove the need of a specific understanding or use of how something works to allow things to be modified at a higher or lower level without effecting the others
Inheritance - reusing code from other objects
Polymorphism - allow code to act the same way using the same method names


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
