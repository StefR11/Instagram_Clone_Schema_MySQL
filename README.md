# Instagram_Clone_Schema_MySQL
In this Instagram clone schema I have focused on the basics and store entities / information as to  USERS, PHOTOS, COMMENTS ON PHOTOS, LIKES FOR PHOTOS as well, HASHTAGS WHICH ONLY APPLY TO PHOTOS. I did not worry about hashtags inside of comments which users can do on a real Instagram. In addition stored FOLLOWERS and FOLLOWINGS / FOLLOWEES.
To help me guide the database structure design I have used the project-attached schema designer dbdiagram.io.
The schema is composed of the Users, Photos, Comments, Likes tables which are referenced each other with One-To-Many relationship the most common relationship in relational Schemas. 
The table USERS has a unique ID column with a PRIMARY KEY constraint which links foreign keys columns in the Comments and Photos tables. As any users are allowed to post as many photos as they like, the Users and Photos table are then linked one another through PK ID column and FK user_id column.
The table Comments which is going to rely on both Users and Photos tables contains the PK ID column and two FK columns as User_id and Photo_id that are referenced to the PK of the column ID in the USERS table and to the PK of the column ID in the PHOTOS table, respectively.
In Regards to Likes for Photos, I have opted to build on the first Junction table of the schema with the FK columns USER_ID and PHOTO_ID. The combination of these FOREIGN KEYS forms
the PRIMARY KEY of the table (COMPOSITE KEY), so that we ensure that there is only one like per user. Within this table a MANY-TO-MANY relationship is defined. 
The other junction table of the schema is concerned with


there are also many more other things to store, I did not store stuff about advertising
