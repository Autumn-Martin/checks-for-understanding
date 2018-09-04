## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
* rails new

2. What do Models generally inherit from in rails?
* ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
* ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
*  ```resources: horses, only: [:show]```

5. What rake task is useful when looking at routes, and what information does it give you?
* ```rake routes```
* it gives you path prefix, HTTP verb, URI path, and controller action for each route available

6. What is an example of a route helper? When would you use them?
* new_horse_path
* use to be dynamic and readable
* use to avoid weird characters in your urls

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* `_path` returns the url relative to your domain, best to use incase your server domain ever changes
* `_url` renders the full url

8. What are strong params and why are they necessary?
* strong params allow you to store parameters away from the user
* strong params are necessary for the create action, because if a user was allowed to
pass in an entire form, they could pass in things you don't want
* use to encapsulate permissible parameters

9. What role does `form_for` play in helping us create our forms?
* it is a rails helper method for forms

10. How does `form_for` know where to submit the user's input?
* it knows based on the argument you provide it

11. Create a form using a `form_for` helper to create a new `Horse`.
* ```
<%= form_for @horse do |f| %>
<%= f.label :name %>
<%= f.text_field :name %>
<%= f.submit %>
<% end %>
```

12. Why do we want to validate our models?
* to require an attribute to be present in order for an object to exist

13. What are the steps of the DNS lookup?
* you type a web address in your browser
* browser sends request to DNS to find web sites IP address (HTTP request, with HTTP verb, version, domain name, etc.)
* DNS returns response of the IP address that matches the web address you typed in earlier (HTTP response, with HTTP version, status code, and reason, etc.)

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `
* ```expect(page).to have_content(person.name) ```
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?
* `move[prance]`

16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the difference between how you would return true vs returning 3?
```
furniture[:purchased]
```
versus
```
furniture[:table][:height]
```

17. What is inheritance?
* inheritance is a useful feature where child classes can inherit methods from a parent class, which DRY's up code

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
