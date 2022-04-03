# Bookify

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
Bookify is a simple app that allows users to find books through Google Books database.

### App Evaluation
- **Category:** Book/ Education
- **Mobile:** Update new books and user reviews in real time 
- **Story:** Allow users to research about books, manage their books, and have recommendations on new books to read
- **Market:** Anyone who reads books can utilize the app to track their books and find new books. 
- **Habit:**
    * Users can use the app multiple times a day to research new books 
    * Features such as "Random book recommender" will recommend books for users to continue reading
- **Scope:** Start out small with just viewing book info and liking books. Optional user stories include random book recommendation. In further version, can be exapnded into a social network of book readers where each user has a book profile and can interact to talk about their book preferences with each other. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User see app icon in home screen and styled launch screen
* User can login
* User can logout
* User can register
* User can access/change profile
* User can see info for each book
* Access bookshelf
    * like, delete
* Review? User can see reviews from others?


**Optional Nice-to-have Stories**
* Write review of book
* Generate random book recommendation
    * save book

### 2. Screen Archetypes


* Login page
   * User can login

* Register page
* Settings page
* Profile page
* Bookshelf page

* Book page
    - like
    - review
    - delete
* Random book generator page
    - modal page with info
    - add to bookshelf

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Bookshelf
* Random book generator
* Profile
* Settings
* (Book page presented modally) 

**Flow Navigation** (Screen to Screen)

* Register page
    * Home page

* Login page
    * Home page
    * bookshelf page
  

* Settings page
* Profile page
* Bookshelf page [Stream]

* Book page
    - like
    - review
    - delete
* Random book generator page
    - modal page with info
    - add to bookshelf

## Wireframes
[Add picture of your hand sketched wireframes in this section]

0. Launch page
1. Login Page
2. Auth page
3. Dashboard
    - bookshelf
    - random book generator
4. bookshelf
    - like
    - review
    - delete
5. random book generator
    - modal page with info
    - add to bookshelf

<img src="https://i.imgur.com/fYkpn4B.gif" width=300>

### [BONUS] Digital Wireframes & Mockups!
<img src="https://i.imgur.com/HxrKvL7.png" width=600>

### [BONUS] Interactive Prototype
- **Figma Prototype**: https://www.figma.com/file/oMdNLc4eQEmV5q5J3jrmpf/Bookify-Wireframe?node-id=0%3A1

## Schema 
[This section will be completed in Unit 9]
### Models
#### user
| Property  | Type | Description |
| ------------- | ------------- | ------------- |
| userId  | String  | unique id for the user (default field)|
| likedBooks  | List(book)  | List of liked books |
| viewedBooks  | List(book)  | List of viewed books |
| writtenrReviews  | List(review)  | written reviews from this user |


#### book
| Property  | Type | Description |
| ------------- | ------------- | ------------- |
| bookId  | String  | unique id for the book (default field)|
| synopsis  | String  | book synopsis |
| image  | File  | book snapshot |
| author  | String  | book author |
| publishDate  | DateTime  | book pubished date |
| reviews  | List(review)  | book reviews |

#### review
| Property  | Type | Description |
| ------------- | ------------- | ------------- |
| reviewId  | String  | unique id for the review (default field)|
| userID  | String  | unique id for the user  |
| bookId  | String  | unique id for the book (default field)|
| publishDate  | DateTime  | review pubished date |
| reviewText  | String  | review content |


### Networking
- [Add list of network requests by screen ]
- [Create basic snippets for each Parse network request]
- [OPTIONAL: List endpoints if using existing API such as Yelp]b
