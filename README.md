# Instagram_Clone_Schema_MySQL 
DDL COMMANDS
In this Instagram clone schema I have focused on the basics and store entities / information as to  USERS, PHOTOS, COMMENTS ON PHOTOS, LIKES FOR PHOTOS as well, HASHTAGS WHICH ONLY APPLY TO PHOTOS. I did not worry about hashtags inside of comments which users can do on a real Instagram. In addition I stored FOLLOWERS and FOLLOWINGS / FOLLOWEES.
To help me guide the database structure design I have used the project-attached schema designer dbdiagram.io.
The schema is composed of the Users, Photos, Comments, Likes tables which are referenced each other with One-To-Many relationship the most common relationship in relational Schemas. 
The table USERS has a unique ID column with a PRIMARY KEY constraint which links foreign keys columns in the Comments and Photos tables. As any users are allowed to post as many photos as they like, the Users and Photos table are then linked one another through PK ID column and FK user_id column.
The table Comments which is going to rely on both Users and Photos tables contains the PK ID column and two FK columns as User_id and Photo_id that are referenced to the PK of the column ID in the USERS table and to the PK of the column ID in the PHOTOS table, respectively.
In Regards to Likes for Photos, I have opted to build on the first Junction table of the schema with the FK columns USER_ID and PHOTO_ID. The combination of these FOREIGN KEYS forms
the PRIMARY KEY of the table (COMPOSITE KEY), so that we ensure that there is only one like per user. Within this table a MANY-TO-MANY relationship is defined. 
Another example of a junction table within this schema is concerned with the Follows table where both the FK columns Follower_id and Followee_id links the PRIMARY KEY
column ID of the USERS table. Imagining that I have an Instagram account, the followers are the users following me, on the contrary the followees or following are the users that I follow. 
Finally, in order to try to obtain the most effective approach for Hashtags I created two tables, TAGS showing ID as the PK column with the relevant tag name and the other table called PHOTO_TAGS which is the third Junction table of the schema composed of the Photo_id and tag_id FK columns which references on a many-to-many relationship the ID PK column of the Photos table and the ID PK column of the Tags table.
There could have been other constraints in the schema which instead I did not include at all such as ON DELETE CASCADE for foreign key columns with which rows from any child table are deleted automatically, when the rows from the related parent table are deleted.

DML & DQL COMMANDS

After inserting a bunch of data in each table of the schema I answered some questions to help me get better data insights.









