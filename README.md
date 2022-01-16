# Pennbook
## Pennbook is a mini, yet scalable Facebook clone featuring 5 main components: user accounts with a username (UID) and hashed password with support for account changes and registration, account posts and updates with comments that are displayed on a user’s wall, home page, a direct message and group chat functionality with online users, the ability for users to add friends and visualize their network of friends, and a newsfeed customized to the user’s interests. 

## Tech Stack
React was used for the frontend, Material UI for styling, Node.js/Express for the backend, DynamoDB to create database tables for backend storage, socket.io to allow browser-server communication for chat, Apache Spark and Amazon's Elastic MapReduce to handle big data analysis, and EC2 for hosting. Beyond the required tech stack, we decided to use React because it allows us to define reusable, custom components that are attached to state, offers high performance ​​with a virtual DOM program and server-side rendering, and seamless support for dynamic content by updating state after a set interval. 

## Features Implemented
1. Login that allows a user to login through a username and password combo (hashed bcrypt) 
2. User registration with username, password, email, first & last name, affiliation, and >=2 news category interests
3. Account changes (password, affiliation, email, interests)
4. Walls in reverse chronological order w/ ability to post status updates on your own or friends' walls
5. Home page: Home page with status updates, new friendships, and status updates, profile updates (posts) made by friends--with commenting supported for each post
6. Search: A user search field in the navigation bar that allows the user to search for other users by name
7. Friends: Can add and remove friends + a list of their current friends along with online status 
8. Visualizer:  Can visualize their network of friends, friends’ friends, etc
9. Dynamic content: Posts and comments, as well as the list of online friends are refreshed periodically
10. Chat: When user’s friend is currently online, the user can invite the friend to a chatsession, and the friend will receive a notification in notifiation side panel. The contents of a chat session are be persistent and stored in DB. Supports group chats by opening a new (group) chat session when a 3rd online user is added to chat. Messages in a chat (or group chat) session are be ordered consistently by timestamp.
11. News: New articles appear in each user’s feeds at least once every hour. Users are able to “like” articles that are shown to them. The articles in their feed will be selected in a weighted random fashion, using weights computed with an implementation of the adsorption algorithm in Spark. Users are able to search for news articles explicitly.
12. Tagging: You can tag users to link to their wall on a post by doing @userID.
