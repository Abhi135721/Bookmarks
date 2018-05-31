# Bookmarks

## Resources:

### User :
	
    ID	: Integer		Primary Key
    Name	: Varchar(100)	
    Mail_id	: Varchar(150)
    
### Bookmark:
	
    ID		: Integer		Primary Key
    Title		: Varchar(100)
    URL		: Varchar(200)
    SLUG		: Varchar(100)
    CreateTime	: Date
    UpdateTime	: Date
    Privacy		: Boolean(to store public or private)
    User_id		: Integer foreign key references User(ID)
    
### Tag:
	
    ID		: Integer		Primary Key
    Name		: Varchar(100)
    
###	Bookmark_Tags:

    ID		:	Integer		Primary Key
    Bookmark_id	:	Integer foreign key references Bookmark(ID)
    Tag_id		:	Integer	foreign key references Tag(ID)
    
    
# Functions:

### User functions:

    GET    /User          List of Users
    POST   /User          Create new User
    PUT    /User/<id>     Update a User
    DELETE /User/<id>     Delete User having the given id
    GET    /User/<id>     Retrieving data of the User with given id

### Bookmark functions:

    GET    /Bookmark          List of Bookmarks
    POST   /Bookmark          Create new Bookmark
    PUT    /Bookmark/<id>     Update a Bookmark
    DELETE /Bookmark/<id>     Delete Bookmark with the given id
    GET    /Bookmark/<id>     Retrieving data of the Bookmark with given id

### Tag functions:

    GET    /Tag          List of tags
    POST   /Tag          Create new tag
    PUT    /Tag/<id>     Update a tag
    DELETE /Tag/<id>     Delete tag with the given id
    GET    /Tag/<id>     Retrieving data of the tag with given id
    
### User_Bookmarks:

    GET    /User/Bookmark	List of all Bookmarks for every User
    GET    /User/<id>/Bookmark	List of Bookmarks of User having the given id.
    
### Bookmarks_Tags:

    GET    /Bookmark/Tag	List of all tags for every Bookmark
    GET    /Tag/Bookmark	List of all Bookmarks for every Tag
    GET    /Bookmark/<id>/Tag	List of tags for a particular Bookmark
    GET    /Tag/<id>/Bookmark	List of all bookmarks for a particular tag
    
    
    
    
