[![](https://raw.github.com/karan/Qnowledge/master/logo.png)](https://github.com/karan/Qnowledge#usage)

Knowledge API for Quora.

Provides access to various details of any question using simple REST API:

- Topics
    - Questions in a Topic
- Question:
    - Title
    - Details
    - Topics
- Answers (Upto 6 top answers):
    - Author
    - Votes
    - Rank
    - Answer body
    - Answer body (HTML)

**Author: [Hasan Diwan](mailto:hasandiwan+quora@gmail.com)**

### Start

    $ pip install -r requirements.txt   # install dependencies
    $ python app.py                     # start the api

### Deploy to Heroku

    $ pip install -r requirements.txt   # install dependencies
    $ heroku create
    $ heroku addons:add newrelic
    $ (git add, git commit)
    $ git push heroku master

### Usage

Base URL is wherever you deploy it.

**Output:** JSON

### Get questions in a topic

#### `GET /topic=<url>`

Example:

`http://localhost:5000/topic=http://www.quora.com/India`

### Get the question details

#### `GET /url=<url>`

Example:

http://localhost:5000/url=https://www.quora.com/Google/What-are-the-changes-made-to-the-host-matching-phase-for-Google-Summer-Internships-from-2013-to-2014`

Output:

    {
    "answers": [
        {
        "answer": "A2AThe process is the same as last summer (unless I missed an important memo!).Embed QuoteVia  Elynn Lee.", 
        "answer_html": "A2A<br/><br/>The process is the same as last summer (unless I missed an important memo!).", 
        "author": {
            "bio": "Google University Programs", 
            "name": "Jessica Safir"
        }, 
        "rank": 1, 
        "votes": "3"
        }, 
        {
        "answer": "A2A.As far as I know, the process has not changed between last year and this year.Embed Quote", 
        "answer_html": "A2A.<br/><br/>As far as I know, the process has not changed between last year and this year.", 
        "author": {
            "bio": "SDE Intern - Google Forms - Summer 2013 and 2014, 2013-2014 Google Student Ambassador for UT Austin", 
            "name": "Elynn Lee"
        }, 
        "rank": 2, 
        "votes": "3"
        }, 
    <==-------------- snip --------------==>

Donations
=============

If *Qnowledge* has helped you in any way, and you'd like to help the developer, please consider donating.

**- Flattr: [https://flattr.com/profile/hasandiwan](https://flattr.com/profile/hasandiwan)**


Contribute
========

If you want to add any new features, or improve existing ones, feel free to [send a pull request](https://github.com/hasandiwan/Qnowledge)!
