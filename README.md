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

    Get:/user         list of user id
    post:/user        create new user
    put:/user/id      update an user
    Delete:/user/id   delete user with that id
    Get:/user/id      retrieving data of that user

### Bookmark functions:

    Get:/Bookmark          list of Bookmark id
    post:/Bookmark         create new Bookmark
    put:/Bookmark/id       update an Bookmark
    Delete:/Bookmark/id    delete Bookmark with that id
    Get:/Bookmark/id       retrieving data of that Bookmark

### Tag functions:

    Get:/tag          list of tag id
    post:/tag         create new tag
    put:/tag/id       update an tag
    Delete:/tag/id    delete tag with that id
    Get:/tag/id       retrieving data of that tag
