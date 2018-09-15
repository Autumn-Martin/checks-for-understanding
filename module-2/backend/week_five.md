### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
* flash[:notice]
2. Where is cart information/temporary information usually stored?
* in a session
3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
* reasons not to: we could care less about that info, it will tax our database space for no reason...
* reasons to: we are Amazon, we want to remember what users have put in their cart before (whether they bought it or not) for analysis/to show them ads about it, we have a ton of space to store data...
4. What is the purpose of the asset pipeline?
* allows us to minify and compress files
5. Why do we precompile our assets?
* it makes loading an app faster
6. What do each of the following tags do?

```
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

* from the top:
  * the 1st: include style and reset files in our app
  * the 2nd: include javascript files in our app
  * the 3rd: include image files in our app

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
* set up - tell users the right versions of ruby and rails to install, gems, and set up process
* appeal to more users, who won't have to dig so much to access and use your product
* fully explain the goals of your project for clarity in project direction later, possibly include a future directions section that explains these future plans
* include a pitch and screenshots of your project to attract more users
* tell others a ton about your project, which they wouldn't get from just the name, and also showcase your ability to professionally present your hard work.
* show others (for example, with screenshots and gifs), that your project is functional & looks great
* links to relevant urls, like the heroku site where your app is hosted

8. What are the top four accessibility issues that we as developers should be aware of?
* (1) cognitive, (2) visual, (3) hearing, and (4) motor/dexterity impairments

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
* callback
* a create method

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
`scope :active, true` maybe

11. What is the difference between a scope and a class method?
* I don't recall learning that.

### Review Questions:  
12. Given the following hash:  

```ruby
hash = {cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  * ```hash[:cart]["48"] = 4 ```
  12b. How would you increase the quantity of item 29?  
  * if I was to increase the quantity of item 29 by x, I would: ```hash[:cart][:29] += x```
  12c. How would you find out how many items your user is thinking about purchasing?   
  * ```hash[:cart].count```
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?
* polymorphism: allows two different object to be passed through the same method
* duck-typing: if it quacks like a duck, if it walks like a duck, if it looks like a duck...it's probably a duck; this is how polymorphism can be incorporated
* 2 ways to use this: (1) to dry up code (2) to reduce typing

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
``` ruby
old_num = "(630) 854-5483"
old_num.delete("()").gsub(/[ -]/,".")
```


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week
