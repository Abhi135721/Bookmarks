# Bookmarks

## Resources:

### User :
	
    ID		: Integer		Primary Key
    Name	: Varchar(100)	
    Mail_id : Varchar(150)
    
### Bookmark:
	
    ID			: Integer		Primary Key
    Title		: Varchar(100)
    URL			: Varchar(200)
    SLUG		: Varchar(100)
    CreateTime	: Date
    UpdateTime	: Date
    Privacy		: Boolean(to store public or private)
    User_id		: Integer foreign key references User(ID)
    
### Tag:
	
    ID		: Integer		Primary Key
    Name	: Varchar(100)
    
###	Bookmark_Tags:

	ID			:	Integer		Primary Key
    Bookmark_id	:	Integer foreign key references Bookmark(ID)
    Tag_id		:	Integer	foreign key references Tag(ID)
    
    
