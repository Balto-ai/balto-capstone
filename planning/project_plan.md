# Project Plan

Pod Members: **Annesa Tran, Christy Xiong, Charles Xu**

## Problem Statement and Description

The main purpose of our proposed app is to (1) provide a centralized dashboard for shelter administrators to store records and track dogs and (2) provide a platform for users to explore and adopt dogs.

The app will include progress tracking (including a live feed of achievements and a section including what instructions a dog can or can’t follow), an administrative tool to keep track of dogs under their care, and a platform to help match potential adopters with dog profiles.

## User Roles

* Adopter: a user who is looking to adopt a dog.
* Shelter administrator/employee: a user who works at an animal shelter.

## User Personas

### Adopter
 
1. Karen is a 25 year old who recently moved to Los Angeles alone for work. Her new job often requires her to come in early, and she usually ends up working late hours as well. She finds that being on her own in the city can be lonely at times and is considering getting a dog. But, with her new commitments at her full-time job, Karen is unsure if she has the time to train a dog.

2. Gina is a 36 year old living in a home in the suburbs outside of Minneapolis, Minnesota. Gina and her partner have always wanted to adopt a dog, but are hesitant because they also have two children, aged 3 and 5. They know that they have the space to keep a large dogm, but since they have young children, they want to make sure that they find a dog that is non-aggressive and family-friendly.

3. John is a 30 year old single man who recently moved to Nevada as a bartender and wants a dog to keep him company during the daytime. John wants a well-trained dog but doesn’t want to break the bank on a dog from a breeder or store, so he’s thinking about going the adoption route.

4. Sandra is a 23 year old college graduate ready to move out and start a new job in Portland, Oregon. During college, she was engaged in animal rights activism and strongly opposes dog breeding and puppy mills. Thus, she wants to adopt a pet from a shelter that treats its animals responsibly and respectfully.

5. Jeffrey is a 19 year old college freshman living with his parents. Although he’s not 100% set on getting a pet dog, he still finds himself checking Balto, adoption sites, pet store listings whenever he has free time in-between classes. 

### Shelter Employee

1. Henry is a manager at an adoption shelter in Orlando that does not follow the no-kill policy. This means that if there are more dogs than spots available, some dogs will be euthanized. Because of this, Henry is motivated to increase the shelter’s adoption rate and also encourage visitors to adopt dogs that have been in the shelter for longer than the recommended five-day period. He is primarily looking for a management system that can track the dogs in their shelter, match online adopters to the dogs in the system, and notify him when the shelter is over-capacity.

2. Mariah is the head administrator at a small adoption shelter in Kansas City. The shelter currently relies heavily on both paper records and Excel spreadsheets to keep track of all the dogs under their care, but this makes it difficult for multiple employees to access records. So, she’s looking to test out cloud-based alternatives for the shelter’s record-keeping.

3. Cindy is an employee at her local animal shelter and has noticed that the older dogs at the shelter do not get adopted nearly as often as the younger ones. Frustrated with this, she is trying to push upper management to focus more on getting the senior dogs to get adopted. 

## User Stories

1. As a shelter employee, I want to have a dedicated account so that I can specifically view the dogs at my shelter.
2. As a shelter employee, I want to view/create/update/delete dog profiles so that we can add to our database of shelter dogs. This involves a form to register a dog to the database.
3. As a shelter employee, I want to view milestones/add milestones, so that we view dog training milestones and add new milestones.
4. As a shelter employee, I want to update and delete milestones so that I can fully customize a dog’s training curriculum.
5. As a shelter employee, I want to view all the dogs in my shelter and view individual dog records so that I can keep track of all the dog profiles I manage. This involves a table of dogs with the ability to filter and search for specific dogs.
6. As a shelter employee, I want to delete dog profiles in the database, both on the profile itself and on the table of all dogs in the database.
7. As a shelter employee, I want to edit what information is shown to potential adopters so that I can promote those dogs to get adopted.
8. As an adopter, I want to have an account so that I can save my user information regarding the dogs I’m interested in.
9. As an adopter, I want to be able to sort and filter adoption listings so that I can look at dogs that match my personal preferences.
10. As an adopter, I want to view a starred list so that I can keep track of the dogs I want to adopt or view their training progression easily. This involves using a star feature on a dog profile and on the rows of the dog table.
11. As an adopter, I want to add and remove to and from my starred list so that the list stays relevant to what I’m looking for. This involves a star button.
12. As an adopter, I want to view information about a specific dog so that I know more about a dog before deciding to adopt.
13. As an adopter, I want to read a feed on a dog’s profile that updates whenever the dog makes progress in their training so that I can keep track of the dog’s training progression. This involves updating the feed whenever our shelter employee has made changes to the dog’s training progress.

## Pages/Screens

[Figma Link](https://www.figma.com/file/a0jPT7oHYiOqXGnYfxgm5I/Wireframe?node-id=77%3A333)

![Figma Wireframe Screenshot](https://i.imgur.com/hoaEM8f.jpg)

### Error Pages

* Access Denied Page
* Not Found Page

### User-facing

* Landing Page
* Login Page
* Register Page
* User Profile Page
* Dog Profile Page
* Adopt Request Page
* Favorites Page
* Explore/Search/Filter All Dogs Page
* Quiz Page

### Admin-facing

* View All Dogs
* Add a dog
* Edit a dog
* Delete a dog
* Add a dog’s training progress
* Update a dog’s training progress
* Delete a dog’s training progress

## Data Model

[LucidChart Link (account required)](https://lucid.app/lucidchart/87596c12-ec86-4e7f-a937-fe339ce775af/edit?viewport_loc=-452%2C131%2C2048%2C858%2C0_0&invitationId=inv_a47cb6ea-9640-42e7-b552-6a6259fc1532#)

![ER Diagram](https://i.imgur.com/UpFOGzt.png)


<table>
  <tr>
   <td colspan="3" >Users — <em>prospective adopters browsing the website</em>
   </td>
  </tr>
  <tr>
   <td>id
   </td>
   <td>Integer, serial, not null
   </td>
   <td>Primary key
   </td>
  </tr>
  <tr>
   <td>first_name
   </td>
   <td>Text, not null
   </td>
   <td>User first name
   </td>
  </tr>
  <tr>
   <td>last_name
   </td>
   <td>Text, not null
   </td>
   <td>User last name
   </td>
  </tr>
  <tr>
   <td>email
   </td>
   <td>Text, not null, unique
   </td>
   <td>User email
   </td>
  </tr>
  <tr>
   <td>password
   </td>
   <td>Text, not null
   </td>
   <td>User password
   </td>
  </tr>
  <tr>
   <td>zip_code
   </td>
   <td>Integer
   </td>
   <td>User zip code
   </td>
  </tr>
  <tr>
   <td>is_admin
   </td>
   <td>Boolean, not null
   </td>
   <td>Whether or not the user is an admin
   </td>
  </tr>
  <tr>
   <td>created_at
   </td>
   <td>Timestamp, not null
   </td>
   <td>When the user account was created
   </td>
  </tr>
  <tr>
   <td>shelter_id
   </td>
   <td>Integer
   </td>
   <td>Foreign key references shelters(id); null if user is not a shelter admin user
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="3" >Shelters — <em>shelters using the service</em>
   </td>
  </tr>
  <tr>
   <td>id
   </td>
   <td>Integer, serial, not null
   </td>
   <td>Primary key
   </td>
  </tr>
  <tr>
   <td>email
   </td>
   <td>Text, not null, unique
   </td>
   <td>Admin email
   </td>
  </tr>
  <tr>
   <td>address
   </td>
   <td>Text, not null
   </td>
   <td>Address of Shelter
   </td>
  </tr>
  <tr>
   <td>city
   </td>
   <td>Text, not null
   </td>
   <td>City the shelter is located in
   </td>
  </tr>
  <tr>
   <td>state
   </td>
   <td>Text, not null
   </td>
   <td>State the shelter is located in
   </td>
  </tr>
  <tr>
   <td>zip_code
   </td>
   <td>Integer, not null
   </td>
   <td>Shelter zip code
   </td>
  </tr>
  <tr>
   <td>phone_number
   </td>
   <td>Integer, not null
   </td>
   <td>Phone number of Shelter
   </td>
  </tr>
  <tr>
   <td>created_at
   </td>
   <td>Timestamp, not null
   </td>
   <td>When the shelter account was created
   </td>
  </tr>
  <tr>
   <td>name
   </td>
   <td>String, not null, unique
   </td>
   <td>Name of the shelter
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="3" >Dogs — <em>dogs currently staying at a shelter</em>
   </td>
  </tr>
  <tr>
   <td>id
   </td>
   <td>Integer, serial, not null
   </td>
   <td>Primary key
   </td>
  </tr>
  <tr>
   <td>name
   </td>
   <td>Text, not null
   </td>
   <td>Name of the dog 
   </td>
  </tr>
  <tr>
   <td>dob
   </td>
   <td>Date, not null
   </td>
   <td>Dog’s date of birth
   </td>
  </tr>
  <tr>
   <td>size
   </td>
   <td>Text, not null
   </td>
   <td>Size of the dog, either “small”, “medium”, or “large”
   </td>
  </tr>
  <tr>
   <td>breed
   </td>
   <td>Text, not null
   </td>
   <td>Breed of the dog
   </td>
  </tr>
  <tr>
   <td>sex
   </td>
   <td>Text, not null
   </td>
   <td>Sex of the dog, either “M” or “F”
   </td>
  </tr>
  <tr>
   <td>color
   </td>
   <td>Text, not null
   </td>
   <td>Color of the dog
   </td>
  </tr>
  <tr>
   <td>desc_1
   </td>
   <td>Text, not null
   </td>
   <td>Description for the prompt “I’m known for being…”
   </td>
  </tr>
  <tr>
   <td>desc_2
   </td>
   <td>Text, not null
   </td>
   <td>Description for the prompt “I’m looking for someone who…”
   </td>
  </tr>
  <tr>
   <td>date_entered
   </td>
   <td>Date, not null
   </td>
   <td>Date of entry into the shelter
   </td>
  </tr>
  <tr>
   <td>image_url
   </td>
   <td>Text, not null
   </td>
   <td>URL to photo of dog
   </td>
  </tr>
  <tr>
   <td>kid_friendly
   </td>
   <td>Boolean, not null
   </td>
   <td>Whether or not the dog is suitable for a household with children
   </td>
  </tr>
  <tr>
   <td>pet_friendly
   </td>
   <td>Boolean, not null
   </td>
   <td>Whether or not the dog is suitable for a household with other pets
   </td>
  </tr>
  <tr>
   <td>elderly_friendly
   </td>
   <td>Boolean, not null
   </td>
   <td>Whether or not the dog is suitable for a household with elderly persons
   </td>
  </tr>
  <tr>
   <td>created_at
   </td>
   <td>Timestamp, not null, default now
   </td>
   <td>When the dog row was created
   </td>
  </tr>
  <tr>
   <td>shelter_id
   </td>
   <td>Integer, not null
   </td>
   <td>Foreign key references shelters(id)
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="3" >Milestones — <em>tracks tricks or achievements for a dog</em>
   </td>
  </tr>
  <tr>
   <td>id
   </td>
   <td>Integer, serial, not null
   </td>
   <td>Primary key
   </td>
  </tr>
  <tr>
   <td>name
   </td>
   <td>Text, not null 
   </td>
   <td>Name of milestone
   </td>
  </tr>
  <tr>
   <td>status
   </td>
   <td>Boolean, not null, default false
   </td>
   <td>Milestone incomplete or complete
   </td>
  </tr>
  <tr>
   <td>hours
   </td>
   <td>Integer, not null, default 0 
   </td>
   <td>Hours spent training dog
   </td>
  </tr>
  <tr>
   <td>notes
   </td>
   <td>Text
   </td>
   <td>Additional notes from dog training
   </td>
  </tr>
  <tr>
   <td>created_at
   </td>
   <td>Timestamp, not null, default now
   </td>
   <td>When the milestone was created
   </td>
  </tr>
  <tr>
   <td>updated_at
   </td>
   <td>Timestamp, not null, default now
   </td>
   <td>When the milestone was updated
   </td>
  </tr>
  <tr>
   <td>dog_id
   </td>
   <td>Integer, not null
   </td>
   <td>Foreign key references dogs(id)
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="3" >User_dog_pairings — <em>facilitates a M:M relationship between users and dogs</em>
   </td>
  </tr>
  <tr>
   <td>id
   </td>
   <td>Integer, serial, not null
   </td>
   <td>Primary key
   </td>
  </tr>
  <tr>
   <td>created_at
   </td>
   <td>Timestamp, not null, default now
   </td>
   <td>When the dog was starred
   </td>
  </tr>
  <tr>
   <td>dog_id
   </td>
   <td>Integer, not null
   </td>
   <td>Foreign key references dogs(id)
   </td>
  </tr>
  <tr>
   <td>user_id
   </td>
   <td>Integer, not null
   </td>
   <td>Foreign key references users(id)
   </td>
  </tr>
</table>


## Endpoints


<table>
  <tr>
   <td><strong>CRUD</strong>
   </td>
   <td><strong>HTTP Verb</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>User Stories</strong>
   </td>
   <td><strong>Router</strong>
   </td>
   <td><strong>Route</strong>
   </td>
  </tr>
  <tr>
   <td>Create
   </td>
   <td><code>POST</code>
   </td>
   <td>Log in user/admin into account
   </td>
   <td>1, 8
   </td>
   <td><code>auth</code>
   </td>
   <td><code>/login</code>
   </td>
  </tr>
  <tr>
   <td>Create
   </td>
   <td><code>POST</code>
   </td>
   <td>Create a user account
   </td>
   <td>1, 8
   </td>
   <td><code>auth</code>
   </td>
   <td><code>/register</code>
   </td>
  </tr>
  <tr>
   <td>Read
   </td>
   <td><code>GET</code>
   </td>
   <td>Fetch user with JWT token
   </td>
   <td>1, 8
   </td>
   <td><code>auth</code>
   </td>
   <td><code>/me</code>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Read
   </td>
   <td><code>GET</code>
   </td>
   <td>View dogs available for adoption
   </td>
   <td>8, 9
   </td>
   <td><code>dogs</code>
   </td>
   <td><code>/</code>
   </td>
  </tr>
  <tr>
   <td>Read
   </td>
   <td><code>GET</code>
   </td>
   <td>View profile for an individual dog
   </td>
   <td>12, 13
   </td>
   <td><code>dogs</code>
   </td>
   <td><code>/:dogId</code>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Read
   </td>
   <td><code>GET</code>
   </td>
   <td>View dogs under the user’s associated shelter
   </td>
   <td>2, 5
   </td>
   <td><code>dog-records</code>
   </td>
   <td><code>/</code>
   </td>
  </tr>
  <tr>
   <td>Create
   </td>
   <td><code>POST</code>
   </td>
   <td>Create a dog record
   </td>
   <td>2
   </td>
   <td><code>dog-records</code>
   </td>
   <td><code>/</code>
   </td>
  </tr>
  <tr>
   <td>Read
   </td>
   <td><code>GET</code>
   </td>
   <td>View a dog record
   </td>
   <td>4
   </td>
   <td><code>dog-records</code>
   </td>
   <td><code>/:dogId</code>
   </td>
  </tr>
  <tr>
   <td>Update
   </td>
   <td><code>PUT</code>
   </td>
   <td>Edit a dog record
   </td>
   <td>2, 7
   </td>
   <td><code>dog-records</code>
   </td>
   <td><code>/:dogId</code>
   </td>
  </tr>
  <tr>
   <td>Delete
   </td>
   <td><code>DELETE</code>
   </td>
   <td>Delete a dog record
   </td>
   <td>2, 6
   </td>
   <td><code>dog-records</code>
   </td>
   <td><code>/:dogId</code>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Create
   </td>
   <td><code>POST</code>
   </td>
   <td>Create a new milestone for dog
   </td>
   <td>3
   </td>
   <td><code>milestone</code>
   </td>
   <td><code>/</code>
   </td>
  </tr>
  <tr>
   <td>Read
   </td>
   <td><code>GET</code>
   </td>
   <td>View milestone for a dog
   </td>
   <td>3
   </td>
   <td><code>milestone</code>
   </td>
   <td><code>/:milestoneId</code>
   </td>
  </tr>
  <tr>
   <td>Update
   </td>
   <td><code>PUT</code>
   </td>
   <td>Update milestone for a dog
   </td>
   <td>4
   </td>
   <td><code>milestone</code>
   </td>
   <td><code>/:milestoneId</code>
   </td>
  </tr>
  <tr>
   <td>Delete
   </td>
   <td><code>DELETE</code>
   </td>
   <td>Delete a milestone for a dog
   </td>
   <td>4
   </td>
   <td><code>milestone</code>
   </td>
   <td><code>/:milestoneId</code>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Read
   </td>
   <td><code>GET</code>
   </td>
   <td>View user’s saved dogs
   </td>
   <td>10
   </td>
   <td><code>user</code>
   </td>
   <td><code>/starred</code>
   </td>
  </tr>
  <tr>
   <td>Create
   </td>
   <td><code>POST</code>
   </td>
   <td>Add dog to user’s starred list
   </td>
   <td>11
   </td>
   <td><code>user</code>
   </td>
   <td><code>/starred/:dogId</code>
   </td>
  </tr>
  <tr>
   <td>Delete
   </td>
   <td><code>DELETE</code>
   </td>
   <td>Remove dog from starred list
   </td>
   <td>11
   </td>
   <td><code>user</code>
   </td>
   <td><code>/starred/:dogId</code>
   </td>
  </tr>
</table>
