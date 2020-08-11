## Web Scraping
Web Scraping simply means programmatically using Python or any other language grabbing data from websites. 

The easiest way to get data from a website is usually using an API. Some websites allow us to just access it easily or they might have an API but it's only restricted to certain register. Maybe we have to register or pay for it. Maybe they don't offer an API . So instead we might want to just scrape the HTML or the Website and see what we can use. 

### What is web scraping used for ?

A wide variety of uses of web scraping, Each business or individual has unique needs.

- **For Lead Generation**

  To gather contact details like email id , phone no & address of an organization or an individual.

- **For Reputation and Brand Monitoring**

  To actively build brand intelligence and monitor brand perceptions. To understand how customers feel about product or service.

- **For Machine Learning**

  Machine Learning requires data,lots of data. So to gather the data across millions of web pages.

- **For Competitor Analysis**

  To extract competitor data, customer sentiment etc. in a structured, usable format

- **For Building Price Comparison Website**

  To collect prices of same item across different website and compare the best price at which we can get it.

- **For Social Media Analysis**

  To  collect data from social media to gauge the consumer trend and the way they react to campaigns.

- **For News Monitoring**

  To analyze and monitor events. To keep track of information regarding certain products, companies or persons.

#### Are you using web scraping for driving the growth of your business ??

##### If not you should, **DATA HAS A BETTER IDEA.**

### What can you Scrape ?

It depends on website to website. Some websites allows web scraper to scrape the data and some doesn't. It depends. So you can check it by simply adding a line of text at end of URL

www.xyz.com/robots.txt 

Add /robots.txt and check what data can you scrape from the websites.

### How can your Scrape ?

You can simply scrape websites easily by using chrome plugins if you search Google Chrome plugin web scraper . You can get it easily.

### How Google , Bing and Yahoo Scrape Data ??

They have a crawler that is a program that crawled websites and read websites to understand what the website is about. If the website mentioned car details or different text related to car. Well they decide this is about is about car details. So when anyone searcher car details they get this list of websites.

## Web Scraping Using Python



### Pre-Requisites

- Install Python
- Download Beautiful Soup Module
  - pip install beautifulsoup4
- Download Requests Module
  - pip install requests

**What Beautiful Soup does ??**

Beautiful Soup is a library that makes it easy to scrape information from web pages. It sits atop an HTML or XML parser, providing Pythonic idioms for iterating, searching, and modifying the parse tree. It allows us to parse. That is we can use Beautiful Soup to convert this from a string to an actual object that we can manipulate and use . Using python to modify this data to what we want.

<img src="https://res.cloudinary.com/dygfr5kt4/image/upload/v1597111879/soup_txwsxu.png"/>



### How To Use ??

[Beautiful Soup](http://www.crummy.com/software/BeautifulSoup/) is a Python library for pulling data out of HTML and XML files. It works with your favorite parser to provide idiomatic ways of navigating, searching, and modifying the parse tree. It commonly saves programmers hours or days of work.

Beautiful soup allows to use the actual HTML and grab different data so use the data that we have gathered.

So we can think of this as web-browser that we are using without the actual data.
We try to grab the data from the url.

   -  res = requests.get('https://news.ycombinator.com/news')

To convert the requested data from from a string to that we can actually use. Beautiful Soup make this task simple for us.

- soup = BeautifulSoup(res.text , 'html.parser')

Now we can use this BeautifulSoup object called soup to extract various data.

Some ways to navigate the HTML Structure to extract information :- 

1. soup.title

   **-->** Display the title of the html file enclosed with title tag.

2. soup.title.string

   **-->** Display the title only not the tag.

3. soup.head

   **-->** Display all the statement inside the head tag.

4. soup.p

   **-->** Display the first statement inside the paragraph tag.

5. soup.a

   **-->** Display the first statement inside the anchor tag.

6. soup.find_all('a')

   **-->** Display all the statement inside the anchor tag.

7. soup.find(id="link3")

   --> Display all the statement with id=link3.

   For Further Information. Read the BeautifulSoup [Documentation](http://www.crummy.com/software/BeautifulSoup/)

### Beautiful Selectors

One of the best ways in my opinion to actually use this soup object is to use the select method on it and select allows to grab a piece of data from soup object that we downloaded and created using what we call a CSS selector.

 But a CSS selector allows us to select the data using css selector.

- soup.select('a')

  **-->** It going to select all the a tag.

- soup.select('.abcde')

  **-->** It going to select all the span with class name abcde.

- soup.select('#dadcba')

  **-->** It going to select all the span with id dadcba.


Now let us use our knowledge to make a project which is very useful in daily life using Web Scraping. [Web-Scraper](https://github.com/sauravchaudharysc/Web-Scraper)

  
