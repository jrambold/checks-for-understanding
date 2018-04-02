## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
rails new [project] -T -d="postgresql" --skip-turbolinks --skip-spring
2. What do Models generally inherit from in rails?
ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horses, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
rake routes
prefix, verb, uri, pattern, controller#action
6. What is an example of a route helper? When would you use them?
horses_path
rather than hardcoding a path
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
url will give the full url while path will only give the uri
8. What are strong params and why are they necessary?
a private method to use just the specific params to pass
9. What role does `form_for` play in helping us create our forms?
it autogenerates forms with the proper commands based on the object in it
10. How does `form_for` know where to submit the user's input?
based on which variables are passed to it
11. Create a form using a `form_for` helper to create a new `Horse`.
<%= form_for Horse.new do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.submit %>
<% end %>
12. Why do we want to validate our models?
to restrict the input to something valid to add
13. What are the steps of the DNS lookup?
a request is sent to the dns server on port 52 for ip address of the domain
the order of a dns lookup is hostfile/local computer cache/router/isp or configured dns server/backbone dns server/6 root dns servers from ICANN
the dns server responds with an ip address

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
def move
  prance
end
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
furniture[:table][:height]
furniture[:purchased]

16. What is inheritance?
getting methods from another class

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week
