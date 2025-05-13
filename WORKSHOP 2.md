# WORKSHOP 2.



- Miguel Ángel Tauta García - 20242005126 

- Luisa Daniela Correa Torres - 20242020048 


_Object-oriented programming_

_ENG. Carlos Andres Sierra Virgüez._





# 1. PROJECT DEFINITION

**1.1 Project Name: Apple Music.**

**1.2 Description:** This project will be a small version of a music playback application, applying the principles of object-oriented programming. It will have various functions that allow users to search, play, and manage their favorite music easily. 


**Main Features:**

- Song playback. 

- Playlist management. 

- Song and artist search. 

- User registration. 


These will be the main features of our project, which will be implemented and expanded as the project progresses. 

 



# 2. PROJECT OBJETIVES.

- **Apply object-oriented programming principles in a practical way:** Implement basic object-oriented programming concepts such as classes, inheritance, polymorphism, and encapsulation in system development. 

- **Create a functional music playback system:** Allow the management and playback of songs through a simple interface. 

- **Implement playlist management:** In this application, users will be able to create, modify, and delete playlists. 

- **Develop a scalable and modular structure:** Facilitate the expansion of the system with new functionalities in the future. 

- **Optimize user experience:** Design an intuitive and easy-to-use interface. 





# 3. REQUIREMENTS.

**3.1 Funcional Requirements**

- **User Registration:** The system must allow users to register by providing their name, email address, and password. 

- **Login:** Users must be able to log in using their email and password. 

- **Music Browsing:** The system must allow users to search for and explore songs, albums, and artists. 

- **Custom Playlist:** The system must allow users to create, edit, and delete their own playlist. 

- **Save Favorite Songs:** Users must be able to mark songs as favorites and easily access them. 

 - **Account Management:** Users must be able to modify their personal information and change their password. 

 - **Song Preloading:** The system must load the next song before th current son ends to avoid interruptions. 

 - **Playback History:** Users must be able to view their history by filtering by song name or date. 

- **Smart Shuffle Mode:** The system must offer an advanced shuffle mode, which avoids repeating songs and prioritizes favorites. 

 - **Sleep timer:** Users can set a time after which the music stops automatically.  

- **Search filters:** The system must allow searching by genre, artist, or song length. 




In this “Functional Requirements” section, we decided to implement more specific program requirements based on user stories to allow the user to have a better experience when using the application. We Implemented: 

 

- “Song preloading” so that the user doesn't have to wait longer than necessary to hear their next song. 

- “Playback history” so that in a hypothetical case, the user might forget the name of a song they listened to a while ago and be able to search for it by the date it was played. 

- “Smart Shuffle mode” we call this smart, as it will prioritize the user's favorite songs, not repeat songs, and can even recommend new songs based on the user's tastes. 

- “Sleep Timer” since people often want to play music for a specific amount of time. This will only make the user experience easier when using our app, as it will save time and allow users to control how long they want to listen to music. 

- Finally, “Search Filters” since with this feature we want to streamline and Facilite the search for each user's favorite songs, depending on the artis, genre, duration, etc. 




**3.2 Non-Functional Requirements**

1. **Performance:** The application must load music results in under 5 seconds. 

2. **Scalability:** The system must be able to handle at least 1,000 concurrent users. 

3. **Usability:** The interface must be intuitive and adapt correctly to both mobile and desktop devices. 

4. **Security:** Passwords must be securely stored. 

5. **Compatibility:** The application must be compatible with modern browsers and mobile operating systems (IOS and Android). 




# 4. NEW USER STORIES: 

 - “As a new user, I want to complete a music questionnaire upon registration so the app can recommend personalized playlists from the start.” 

 - “As a frequent user, I want to receive a weekly playlist based on my listening experience so I can discover new music similar to my tastes.” 

  - “As a user, I want to be able to resume playback from where I left off, even if I close the app, so I don't lose track of my progress.” 

 - “As a user, I want to be able to follow artists to receive notifications about new releases and upcoming events.” 

 - “As a user, I want to group my playlists by categories or folders to keep my music organized.” 

 - “As a user, I want to be able to create collaborative playlists with friends, where everyone can add and vote on songs.” 

 - “As a user, I want an option where others can join my session in real time and suggest songs.” 
 


We wanted to implement these new user stories, which are more detailed and functional than the previous ones, as they allow each user to have a more personalized and engaging experience. By focusing on personalization, social discovery, accessibility, and loyalty, the app not only improves its usability but also increases retention, builds emotional connection with users, and stands out in a highly competitive market. These stories are designed to enhance both the functionality and perceived value of the app, ensuring it evolves alongside audience expectations. 

# 5. CRC CARDS

| **Class: User** |  |
|-----------------|--|
| - Register. | - Playlist. |
| - Log in. | - Song. |
| - Create and manage playlist. | - Artist. |
| - Save favorite songs. | - System of recommendation. |
| - Play, pause and manage playlist. | - Playback session. |
| - Follow artists and friends. |  |



| **Class: Song** |  |
|-----------------|--|
| - Store information (name, artist, length, etc.). | - User. |
| - Play songs. | - Playlist. |
| - Provide access to the audio file. | - Playback session. |



| **Class: Playlist** |  |
|---------------------|--|
| - Add/remove songs. | - User. |
| - Play songs in order. | - Song. |
| - Support collaborations. | - Artist. |


| **Class: Recommendation System** |  |
|----------------------------------|--|
| - Analyze user history. | - User. |
| - Suggest songs or playlists. | - Song. |



| **Class: Playback Session** |  |
|-----------------------------|--|
| - Control playback status. | - User. |
| - Save current playback point. | - Song. |
| - Control volume, quality, random mode. | - User settings. |


| **Class: System of Recommendation** |  |
|-------------------------------------|--|
| - Generate automatic playlist. | - User. |
| - Suggest new artist, albums and songs. | - Song. |
|  | - Artist. |
|  | - Playlist. |


Here, in addition to creating new CRC cards, more responsibilities and collaborations were implemented, expanding the interaction between classes.  


**New CRC cards:**

- "Playing Session" allows the user to control the playback status of a song. 

- "Recommendation System" class: we implemented this class to improve playback customization for each user. This class analyzes, generates, and suggests albums, artists, or songs. 


# 6. MOCKUPS.

**6.1 Muckups apple music for mobile devices**

![Image](https://github.com/user-attachments/assets/d29060fb-3c7c-4c6e-b968-609789718ad5)

**6.2 Muckups apple music for website.**

![Image](https://github.com/user-attachments/assets/2a27ed62-3a8d-41c5-802a-7ec3fe34797b)



# 7 UML CLASS DIAGRAM.





# 8. IMPLEMENTATION PLAN FOR OBJECT-ORIENTED PROGRAMMING CONCEPTS.

**8.1 Encapsulation** 

Encapsulation will be implemented through the use of private attributes and public access methods (getters and setters), limiting direct manipulation of internal class data. This technique will be applied particularly in the User class, to protect sensitive information such as the user's password or personal preferences. It will also be used to preserve the integrity of playlists and playback settings, ensuring that data cannot be directly modified in an unsafe manner from other parts of the system. 

Encapsulation will also help hide the internal complexity of certain classes, exposing only the methods necessary for interaction with other classes in the system. 

 

**8.2 Inheritance** 

Inheritance will be used to model object hierarchies with common behaviors. For example, you could define a User base class with general attributes and methods, from which classes such as PremiumUser or GuestUser inherit, extending or restricting functionality based on the account type. 

This approach will facilitate code reuse and allow you to adapt specific functionality without duplicating logic for each user type. 

 

**8.3 Polymorphism**

Polymorphism will be applied primarily through method overriding in classes that share the same interface or base class. This will be reflected in methods such as play(), which can be defined differently in classes such as Song, PlayList, or PlayHistory. 

Additionally, the use of interfaces or abstract classes will allow for more flexible code, where objects can be treated uniformly, even if their behavior varies depending on their type. 

This principle will be essential for implementing advanced features such as custom shuffle or filter execution in searches. 

 

**8.4 Preliminary Code Organization**

A package or module structure is proposed, organized according to the functional responsibilities of each system component: 

 - users/: authentication management, registration, account management, and roles. 

 - playback/: classes related to songs, playlists, history, and playback logic. 

- configuration/: custom settings, timer, preload, preferences. 

- search/: filters and advanced search logic. 

- utilities/: auxiliary classes or shared tools (validations, formats, etc.). 

- This organization will encourage modular development, ease of testing, and future scalability of the project. 
