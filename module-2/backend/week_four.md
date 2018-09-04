## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
* a cookie is a small client-side storage space for user data, which makes the web stateful by reminding the website server bits of info about the user and the users preferences

2. What’s the difference between a session and a cookie?
* a cookie only lasts until the next request
* a session lasts as long as the user is on the site (i.e. being logged in)

3. What’s a flash and when do you want to use flashes?
* a flash is a quick alert/notice to user
* it is helpful to use flashes to tell a user whether they have successfully
deleted/created/edited something or not

4. Why do people say “HTTP is stateless”?
* http acts as if state is always consistent, i.e. it doesn't recognize one user from
another or one user's preferences from another

5. What’s authentication? Explain.
* authentication is identifying a user (for example, as a user with an account vs. an admin)

6. What’s the difference between authentication and authorization?
* authentication ids who a user is, whereas authorization ids what a user is allowed to see or do based off of their authentication

7. What’s a before filter?
* a filter that demands a requirement be met/ action be performed before other actions

8. How do we keep track of a user once they’ve logged in?
* with a session

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?


10. At a high level, what tools can you use to implement authorization? How would you use them?
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
12. What are some strategies you can use to keep your views DRY?


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
