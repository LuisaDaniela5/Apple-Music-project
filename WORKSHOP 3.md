# WORKSHOP 3.



- Miguel Ángel Tauta García - 20242005126 

- Luisa Daniela Correa Torres - 20242020048 


_Object-oriented programming_

_ENG. Carlos Andres Sierra Virgüez._





# 1. PROJECT DEFINITION

### 1.1 Project Name: 
Apple Music.

### 1.2 Description:
This project will be a small version of a music playback application, applying the principles of object-oriented programming. It will have various functions that allow users to search, play, and manage their favorite music easily. 


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

### 3.1 Funcional Requirements

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




### Additional Functional Requirements:

- **Playback Resumption:** The system must allow users to continue playback from where they left off, even after closing the application.

- **Artist Following:** The system must allow users to follow artists in order to receive notifications about new releases and events.

- **Collaborative Playlists:** The system must allow the creation of collaborative playlists, where multiple users can add songs.

- **Shared Sessions:** The system must allow users to start a real-time session where other users can join and suggest songs.

- **Playlist Organization by Folders:** The system must allow users to group their playlists by categories or folders.

- **Personalized Recommendations at Sign-Up:** Upon registration, the system must provide the user with a short music questionnaire to generate personalized playlists.

- **Weekly Personalized Playlist:** The system must automatically generate a weekly playlist based on the user's history and preferences.


### Changes Made:

Seven new functional requirements were added. These respond to newly defined user stories and are aligned with the SOLID principles:

* **Single Responsibility Principle (SRP)**: Each new functionality is designed to be managed by classes with clearly defined responsibilities, such as history tracking, shared sessions, or recommendations.

* **Open/Closed Principle (OCP)**: These features were designed to be added without altering the existing behavior of the system.

* **Dependency Inversion Principle (DIP)**: Some features, such as recommendations or artist following, can be implemented using interfaces, making future extensions easier.


### 3.2 Non-Functional Requirements

1. **Performance:** The application must load music results in under 5 seconds. 

2. **Scalability:** The system must be able to handle at least 1,000 concurrent users. 

3. **Usability:** The interface must be intuitive and adapt correctly to both mobile and desktop devices. 

4. **Security:** Passwords must be securely stored. 

5. **Compatibility:** The application must be compatible with modern browsers and mobile operating systems (IOS and Android). 


### Additional Non-Functional Requirements:

* **Modularity**: The system architecture must be divided into independent modules to facilitate maintenance and the addition of new functionalities.

* **Maintainability**: The code must be clearly structured and documented to ease modification and understanding by other developers.

* **Flexibility in Data Handling**: Key functionalities must rely on decoupled structures, allowing parts of the system to be changed without affecting the rest.

* **Error Traceability**: The system must securely log failure events or exceptions for later review.

* **Automated Testing**: Core functionalities must be testable through unit and integration tests.

### Changes Made:

Five new non-functional requirements were added to ensure the system's internal quality:

* **Modularity and Maintainability** align with the SRP (Single Responsibility Principle) and OCP (Open/Closed Principle), enabling changes to be made without affecting other parts of the system.

* **Flexibility** is directly related to the DIP (Dependency Inversion Principle), ensuring that high-level classes do not depend on concrete implementations.

* **Traceability and Testing** support the application of DIP and SRP, improving error management and quality assurance.




# 4. USER STORIES: 

 - “As a new user, I want to complete a music questionnaire upon registration so the app can recommend personalized playlists from the start.” 

 - “As a frequent user, I want to receive a weekly playlist based on my listening experience so I can discover new music similar to my tastes.” 

  - “As a user, I want to be able to resume playback from where I left off, even if I close the app, so I don't lose track of my progress.” 

 - “As a user, I want to be able to follow artists to receive notifications about new releases and upcoming events.” 

 - “As a user, I want to group my playlists by categories or folders to keep my music organized.” 

 - “As a user, I want to be able to create collaborative playlists with friends, where everyone can add and vote on songs.” 

 - “As a user, I want an option where others can join my session in real time and suggest songs.” 

### NEW USER STORIES:
 
- "As a user, I want to receive notifications with personalized music recommendations based on my listening habits, so I can discover songs I haven't heard yet."
 **Implementation**: The Dependency Inversion Principle (DIP) will be applied by separating the history analysis logic from the presentation component. The recommendation module will be defined through an interface to allow the integration of different future algorithms.

- "As a user, I want to rate songs with stars or 'likes', so that the system can better understand my preferences."
 **Implementation**: The Single Responsibility Principle (SRP) will be applied: the class responsible for playback history will not handle ratings. Instead, a dedicated class will be created to manage user preferences and ratings.

- "As a user, I want to see statistics about my activity (number of songs played, most listened genres, total listening time) so I can better understand my musical habits."
 **Implementation**: Statistics will be decoupled from the player using interfaces, allowing different types of visualizations or analyses to be implemented without altering the data. This follows both the Dependency Inversion Principle (DIP) and the Open/Closed Principle (OCP).



# 5. CRC CARDS

| **Class: User** |  |
|-----------------|--|
| - Register. | - Playlist. |
| - Log in. | - Song. |
| - Manage personal informaton. | - Playback session. |
| - Create and manage playlist. | - Artist. |
| - Save favorite songs. | - System of recommendation. |
| - Complete music preference questionnaire. | - Questionnarie. |
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
| - Allow voting on songs. | - CollaborationManager. |
| - Assign category or folder for organization. | - CategoryManager. |


| **Class: Recommendation System** |  |
|----------------------------------|--|
| - Analyze user history. | - User. |
| - Suggest songs or playlists. | - Song. |
| - Generate personalized playlists.. | - Questionnaire. |
| - Recommend weekly playlists based on listening habits. | - Playback Session. |


| **Class: Playback Session** |  |
|-----------------------------|--|
| - Control playback status. | - User. |
| - Save current playback point. | - Song. |
| - Control volume, quality, random mode. | - User settings. |


| **Class: Questionnaire.** |  |
|-------------------------------------|--|
| - Store user's music preferences from registration. | - User. |
| - Provide data to the Recommendation System. | - REcommendation System. |


| **Class: CollaborationManager.** |  |
|-------------------------------------|--|
| - Manage collaborative playlists. | - Playlist. |
| - Handle voting, user suggestions, and real-time participation. | - User. |


| **Class: CategoryManager.** |  |
|-------------------------------------|--|
| - Group playlists by category or folder. | - User. |
| - Allow user to rename, create, or remove categories. | - Playlist. |

Here, in addition to creating new CRC cards, more responsibilities and collaborations were implemented, expanding the interaction between classes.  


**New CRC cards:**

Three new classes were added to comply with SOLID principles:

1. **Questionnaire.**

2. **CollaborationManager.**

3. **CategoryManager.**

-  Each class fulfills a single responsibility (SRP).

- The classes collaborate based on functional needs; no unnecessary connections were added.

- Existing classes were enriched with new responsibilities and connected to their actual dependencies.

- The system remains modular, scalable, and open to extensions without modifying existing code (OCP).


# 6. MOCKUPS.

### 6.1 Muckups apple music for mobile devices

![Image](https://github.com/user-attachments/assets/d29060fb-3c7c-4c6e-b968-609789718ad5)

### 6.2 Muckups apple music for website.

![Image](https://github.com/user-attachments/assets/2a27ed62-3a8d-41c5-802a-7ec3fe34797b)



# 7 UML CLASS DIAGRAM.
![new UML](https://github.com/user-attachments/assets/dbeb3a9f-5c3f-4d49-86c9-e782d063e1b8)



# 8. IMPLEMENTATION PLAN FOR OBJECT-ORIENTED PROGRAMMING CONCEPTS.

### 8.1 Encapsulation

Encapsulation will be implemented through the use of private attributes and public access methods (getters and setters), limiting direct manipulation of internal class data. This technique will be applied particularly in the User class, to protect sensitive information such as the user's password or personal preferences. It will also be used to preserve the integrity of playlists and playback settings, ensuring that data cannot be directly modified in an unsafe manner from other parts of the system. 

Encapsulation will also help hide the internal complexity of certain classes, exposing only the methods necessary for interaction with other classes in the system. 

 

### 8.2 Inheritance 

Inheritance will be used to model object hierarchies with common behaviors. For example, you could define a User base class with general attributes and methods, from which classes such as PremiumUser or GuestUser inherit, extending or restricting functionality based on the account type. 

This approach will facilitate code reuse and allow you to adapt specific functionality without duplicating logic for each user type. 

 

### 8.3 Polymorphism

Polymorphism will be applied primarily through method overriding in classes that share the same interface or base class. This will be reflected in methods such as play(), which can be defined differently in classes such as Song, PlayList, or PlayHistory. 

Additionally, the use of interfaces or abstract classes will allow for more flexible code, where objects can be treated uniformly, even if their behavior varies depending on their type. 

This principle will be essential for implementing advanced features such as custom shuffle or filter execution in searches. 

 

### 8.4 Preliminary Code Organization

A package or module structure is proposed, organized according to the functional responsibilities of each system component: 

 - users/: authentication management, registration, account management, and roles. 

 - playback/: classes related to songs, playlists, history, and playback logic. 

- configuration/: custom settings, timer, preload, preferences. 

- search/: filters and advanced search logic. 

- utilities/: auxiliary classes or shared tools (validations, formats, etc.). 

- This organization will encourage modular development, ease of testing, and future scalability of the project.


# 9. Implementation of SOLID Principles

### 9.1 Single Responsibility Principle:

**Definition**: A class should do one thing, and therefore, it should have only one reason to change.

**Implementation**: We aim to apply this principle by identifying specific responsibilities and creating a class for each one, ensuring that each class has a single, well-defined responsibility. For example:

* **UserManager**: Responsible exclusively for user registration, authentication, and information updates.
* **PlaylistManager**: Handles only the logic related to creating, editing, and deleting playlists.
* **Player**: Responsible for playing songs and managing playback modes such as shuffle.

This clear separation of responsibilities improves code organization and makes long-term maintenance easier.


### 9.2 Open/Closed Principle:

**Definition**: A class should be open for extension but closed for modification.

**Implementation**: System classes will be designed so they can be extended without needing to be modified. For example, the recommendation feature will be implemented through a **Recommender** interface, allowing different recommendation algorithms to be added without altering the main application logic. This will make it possible to incorporate new recommendation methods (based on preferences, recent behavior, popularity, etc.) without modifying existing classes. Thus, the system remains open to extension but closed to modification.


### 9.3 Liskov Substitution Principle:

**Definition**: Subclasses must be able to replace their superclasses without altering the system's behavior.

**Implementation**: This will be ensured by properly organizing class hierarchies, avoiding that subclasses remove expected functionalities or change predefined contracts.

This is especially relevant for user types. For example, in the user hierarchy, the **PremiumUser** and **GuestUser** classes extend a base **User** class. Each implements the methods defined by the base class, adapted to their own constraints. Therefore, any component that uses the **User** class can interact with any of its subtypes without needing to know their internal differences, ensuring consistency in execution.


### 9.4 Interface Segregation Principle:

**Definition**: Clients should not be forced to depend on interfaces they do not use.

**Implementation**: The system's interfaces have been split into specific functional subsets to prevent classes from having to implement methods they don't need. For example, search, playback, notifications, and playlist editing functionalities are handled through separate interfaces. This way, a class dedicated to music playback is not forced to implement search or filtering methods, and vice versa. This segmentation promotes code reuse and minimizes coupling between modules.


### 9.5 Dependency Inversion Principle:

**Definition**: High-level modules should not depend on low-level modules. Both should depend on abstractions. Also, abstractions should not depend on details. Details should depend on abstractions.

**Implementation**: To apply the Dependency Inversion Principle, all core classes in the system will be designed to depend on interfaces (abstractions) rather than concrete implementations. Low-level components like the player, search system, or song recommender will implement those interfaces. This allows any module to be replaced or updated without affecting the rest of the system, ensuring flexibility, testability, and structural decoupling.

