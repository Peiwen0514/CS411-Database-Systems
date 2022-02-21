## Project Title

Rate My Game 

## Project Summary

We will implement a game rating website that allows users to create their accounts. Through this account, users will be able to rate and review games on the website, and the history of the reviews will be saved so that users can notice the difference between their reviews and the average game rating. The website will also recommend games of the same type to the user based on users' ratings. This is a feature that can be used to realize the commercial value of our project, for example, to promote new games. If people prefer not to create an account, the website will display the game's description, average rating, and reviews from other users. Besides, the site will cover filters and sorting features, which will allow people to look up games within a specific price/rating range or sort the games in ascending/descending order of ratings/price. 

## Description

We intend to implement a user-friendly web page, through which users will be able to keep track of their favorite games, etc. The main thing is that we want to avoid the appearance of ads that are not related to the game. Similar sites place ads based on the user's browser browsing history; for example, if the user has recently searched for shoes, shoes' ads will appear on the pages even when browsing a game site. Our website will limit the categories of ads and only recommend games of the same type based on the user's preferences. 

## Usefulness

Similar websites/applications include Imagine Games Network, Metacritic, Game Spot. However, the difference between ours and theirs is that ours is geared towards students and accommodating various preferences and the power of consumption for students. 
Secondly, there are amounts of robots on websites to swipe fake ratings to attract users. Our target group is students, and there is no interesting relationship, so it is more objective. 

## Realness

The data is divided into user information, game information, game reference rating, and rating of the game of the user. 

There are three main sources of data:
The first is to integrate the data of the existing game rating websites and give a website's rating and description with a reference value.  (From Games Network, Metacritic, Game Spot).
The second source is Extract game information from some public game databases. 
The third is that After the user registers with the website, obtain the evaluation of the game from users. 

## Functionality

**a. Data Description**

We will crawl game ratings and user comments data from different open-source websites (For example Steam). The following are the data tables we will store. 

|   Game     |            |
| :-----------: | :----------------------: |
| Game_id      |        VARCHAR(50)       |
| Name    |          VARCHAR(50)        |
| Captain     |         VARCHAR(50)    |
| Type     |  INT |
| Price     |       INT     |
| Discount     |   BOOLEAN |
| AVG-Rating     |        INT      |
| If_Free     |  VARCHAR(50) |
| release_time     |       DATETIME       |
| Age     |  INT  |
| Num_Like     |  INT  |


|   Gametype     |            |
| :-----------: | :----------------------: |
| Type      |        VARCHAR(50) (Primary key)     |
| Game_id    |          VARCHAR(50)        |

|   Rating     |            |
| :-----------: | :----------------------: |
| Game_id      |        VARCHAR(50)        |
| Comment    |          VARCHAR(50)        |

|  User (A_Team):     |            |
| :-----------: | :----------------------: |
| User Id      |        VARCHAR(50)        |
| Password    |          VARCHAR(50)        |
| Rating_history    |          VARCHAR(50)        |
  
|  Rating_history:     |            |
| :-----------: | :----------------------: |
| User_Id      |        VARCHAR(50)        |
| Game_id    |          VARCHAR(50)        |
| AVG_Rating    |          FLOATING        |
| Rating    |          INT       |

**b. Basic Functionalities** 

**1) Search Engine**: In the Home page of our website, user could search the game they are interested in, then the webpage will jump to our Game Detail page. <br> 
**2) Filter of Price**: In the Home page of our website, we will provide a filter that supports filter out games within a user-given price range. <br> 
**3) Filter of Type**: In the Home page of our website, we will provide a filter that could presents different kinds of games and rank them in the order of popularity. <br> 
**4) Rate Ranking**: In the Ranking page of our website, we will present a ranking table which shows that the most popular games and the top-ranking games.  <br> 
**5) Game Rating**: In the Game Detail page of our website, which could be reached through clicking on the icon or game name, we will provide an interactive rating function for our website users. Each user could rate the games they are interested in. And those new ratings can be used to calculate the order or ranking of games. <br> 
**6) Rate Comparing**: Along with the rating function, every user could see their rating in comparison with the average rating of this game. <br> 

**c. Creative Components** 

**1) Recommendation System**: Our website will use the rating data of different users to implement a recommendation system that will recommend games to users based on their preferences and their gaming habits. Users will be recommended and advertised with more relevant and interesting games on our website. <br> 
**2) Auto-Complete Search**: Our search engine will look at the real searches that are being conducted on our website and discover common and trending ones, this will give user suggestions while they are searching. <br> 

## UI Mockup
Main Page:
![Image text](https://github-dev.cs.illinois.edu/sp22-cs411/sp22-cs411-team004-A_TEAM/blob/6c67600916fe0a305db8f1bdfa96890982bb482b/doc/img-folder/Main_Page.jpg)
Game Detail Page:  
![Image text](https://github-dev.cs.illinois.edu/sp22-cs411/sp22-cs411-team004-A_TEAM/blob/6c67600916fe0a305db8f1bdfa96890982bb482b/doc/img-folder/Game_Detail_Page.jpg)

## Work Distribution

Data Crawler: qixuanx2  
Database: qixuanx2, peiwen4  
Frontend: jiayuny3,  qixuanx2  
Backend: zhihuiw, peiwen4

