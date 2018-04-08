## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
A cookie is a file on a user's computer that stores information sent to the server
2. What’s the difference between a session and a cookie?
A session is stored server side that is tracked by the information in the cookie
3. What’s a flash and when do you want to use flashes?
4. Why do people say “HTTP is stateless”?
The information is sent and the connection is closed.
There's no constant connection well, there kind of is now with http keep alives and other tools
5. What’s authentication? Explain.
Authentication is allowing users to log in and how to access information
6. What’s the difference between authentication and authorization?
authorization is checking whether a user has access to information before displaying it
7. What’s a before filter?
A before filter allows methods to run before a page is loaded
8. How do we keep track of a user once they’ve logged in?
By verifying them based on information in the session
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
Namespace allows adding something that. Nesting allows it being added to the path based on the other resource
10. At a high level, what tools can you use to implement authorization? How would you use them?
A users table, with passwords stored after hashing via encryption all overlayed on an ssl connection
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An enum is a way to declare aliases for integer values stored in the database. it is declared in the model
12. What are some strategies you can use to keep your views DRY?
Using form_for for multiple views with partials

### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```  

given.sort_by do |holidays|
  holidays[:holiday][:name]
end

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
value.split('$')[1].to_i

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week
