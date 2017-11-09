1. What is the most influential book or blog post you’ve read regarding web development?

As a web developer, I read a broad selection of works that discuss web development. This ranges from books on different computer languages to stack overflow. As for the most influential work I’ve read regarding web development, I would have to say my friend recommending me to check out Udacity was the corner stone to my journey as a web developer.

It was right after I graduated from college and I only had a minor in computer science. I wanted to pursue web development as my full time job but felt as if my minor wasn’t enough. My friend who is a web developer told me to look into this online schooling called “Udacity” as they offer a large selection of courses regarding computer science. I went to the Udacity website and I was immediately hooked. I took the free python developer class and after I finished that I went straight into the Full Stack Nanodegree. As I am finishing my Nanodegree, I am now as confident as ever that web development is the field that I am going to pursue as my career.


2. Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?

I had recently developed a single page application using Google Maps API and FourSquares API while displaying markers of popular locations in Brooklyn, NY. This was the frontend project in Udacitys Full Stack Nano degree. This project taught myself how to implement a viewModel to represent data and operations on the UI without having the view and model interact directly

One issue I ran into while creating this App was utilizing a viewModel to properly display my locations. The framework I used was KnockoutJS. KnockoutJS was used to create the viewModel that would filter out the names of each location when typed into a search bar. At first I thought creating my viewModel would be a breeze as I saw examples on how it can be created. Little did I know that assuming this would be a big mistake in my development process. I jumped right into code and had issues debugging for two full days as I assumed I was really close to finding a solution. After the two days of not finding a solution I decided that I needed to take a step back and read each step of KnockoutJS' documentation. After about 2 hours of reading documentation and coding I was able to solve the problem! It was right then that I realized I made a mistake by not going through KnockoutJS' documentation thoroughly. Every time I work on a project now I know to make sure to read the documentation before diving into the code.

3. If you were to start your full-stack developer position today, what would be your goals a year from now?

Udacity has helped my Web Development skills in Python, JavaScript, SQL, HTML, CSS and frameworks/libraries such as jQuery and Flask. I would love to continue this growth as a developer. I feel as I have a solid foundation and with each day of programming I am learning more and more. So a year from now would love to see myself continue the growth I have accomplished. With that being said, I would to not just help myself but to help the company and my co-workers as well.

4. List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?

DDoS Attacks: This is one type of attack a web application is vulnerable to and they stand for distributed denial of service. DDoS attacks target a server over and over again to sabotage that site. The increase of traffic on the server can cause the site to load very slowly for real users, and can even shut the site down completely.

Prevent: There are a few solutions to preventing DDoS attacks. One is have a Firewall to block these potential attackers. Another is to have over provision of bandwidth. This will help in the case of having more bandwidth available to your web server so that these attacks will be less effective. Another would be to call your ISP or hosting provider if you don’t host your own server. Warn them that you are under attack.

SQL Injection: This type of attack is more serious as they try to take information from databases, and any site that uses a database is more than likely to hold personal information about their users. This can include name, address, credit card info, etc. The way SQL injection works is that the attacker adds SQL code to a web form to gain access to the resources in the database. The attacker does not only have the information but also has the ability to drop and edit tables within the database.

Prevent: To prevent this type of attack your website should filter all user input. Another way would is to have a firewall. These firewalls will be set a specific set of rules to filter dangerous web requests. Another way would be to have your database be multi leveled so some users have minimum privileges in the database.

5.  Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (<ul>...</ul>) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

```# create function with argument called strings
def html_list(strings):
    print("<ul>")
# Iterate over strings
    for s in strings:
        ul = "<li>" + str(s) + "</li>"
        print(ul)
    print("</ul>")
# create list
bands = ['Foo Fighters', 'Nirvana', 'Audio Slave', 'Kings of Leon']
# execute function with list
html_list(bands)
```

6. Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.

``` from flask import Flask
app = Flask(__name__)

import json
import random


# This route will show the outcome of the two dice
@app.route('/roll_dice')
def roll_dice():
  # This creates two dice with six sides each and will roll both at random
  for i in range(0, 1):
  # Assign the result of the die roll
    dice1 = random.randint(1, 6)
    dice2 = random.randint(1, 6)

  # Creates object that holds outcome of each roll
  outcome = json.dumps({'dice1': dice1, 'dice2': dice2}, sort_keys=True)

  # This returns the two dice in json format
  return outcome


if __name__ == '__main__':
 app.debug = True
 app.run()
 ```
