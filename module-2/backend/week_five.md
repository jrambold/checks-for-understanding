### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
By outputting what's stored in the flash hash in a view file

2. Where is cart information/temporary information usually stored?
in a PORO

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
It's much slower to store and retrieve the information. It can also balloon the database size to keep track of especially for unregistered users that never return. We would want it to persist in a situation where a user can logout or switch computers and have their cart remain similar to how amazon's cart functionality works

4. What is the purpose of the asset pipeline?
To precompile assets for faster delivery to the user

5. Why do we precompile our assets?
It's faster than generating them on the fly as well as ability to compare file hashes for changes

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

puts the application style sheet from the assets into the html as a required file
puts the application javascript from the assets into the html as a required file
puts an image html tag linking to the image in the assets

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
Concise yet destriptive of what it does, how to set it up and how to use it.
It provides a good jumping off point and point of reference to anyone using the program

8. What are the top four accessibility issues that we as developers should be aware of?
Resolution
Browser/rendering engine
Touchscreen/keyboard
No sight/image/text only

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
Callback
In the controller

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

User.find_by(active: true)

11. What is the difference between a scope and a class method?
A class method uses self.method name to call it for all instances of the class while a scope just uses the single instance of the class

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?
  session[:cart][48] = 4
  12b. How would you increase the quantity of item 29?
  session[:cart][29] = new_quantity  
  12c. How would you find out how many items your user is thinking about purchasing?
  session[:cart].length

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
Being able to use an object like a different object. If it walks like a duck treat it like a duck. This is often seen in a variety of objects acting like an array and being able to call array methods on it.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
given.delete("() -").insert(3, '.').insert(8, '.')


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week
