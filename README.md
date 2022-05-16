
User Flow => The flow of actions a user can perform

Login =>
	As a [ current user ],
	I want [ to login in to my SM account ]
	so that [ I can see my feed ]
		Tasks:
			> Create fxn to retreive data
				> True: able to see pg
				> False: cannot access feed pg
			> Display posts in feed
	
	As a [ new user ],
	I want [ to register to use the new SM account ]
	so that [ I can see other people's posts ]
	
Feed => 
	As a [ current user ],
	I want [ to see user feeds ]
	so that [ I can interact with my own posts ]
		Tasks;
			> Fxn to display all posts
			> edit/delete btn on user's own posts
	
	As a [ current user ].
	I want [ to see and intereact with a "new post" section ]
	so that { I can create new posts ]
		Tasks:
			> Create input section
			> Post btn
				> post to db and display in feed
					> fxn to send to db
					> fxn to add to feed
					> (fxn) reset form
			> Reset btn
				> reset form
				
	As a [ current user ]
	I want [ to edit and delete my own posts ]
	so that [ I can edit and delete my own posts ]
		Tasks:
			> Read-only on non-user posts
			> if isUser, show btn, else don't 
			> onclick [editBtn] 
				=> readonly is removed
				=> user can change content
				=> user updates record
			> onclick [deleteBtn]
				=> removes post from both db and local dom.
				=> verification: alert and confirm before deleting file
	
	As a [ developer ].
	I want [ all posts to have a unique ID ]
	so that [ each post can be differentiated from the others ]
		Tasks:
			> GUID fxn


JSON
	users: [{userObj},
	posts: [{UUID: {UUID, userName, content}, 
	
	
MVPs:
> GUID fxn

user flow => login

1. user wants to log in. => input userName and PW
	> fxn to get UN and PW => store as currentUser
		currentUser = { userNmae: unFromForm, password: pwFromForm }
	
	> getUsers() {
		// ajax methods to get users only
	  }		
	> checkAuth(currentUser) {
		// check if the current user exists in an array of current users
		// check if pw matches pw for existing user
		// if user exists and pw matches, 
		return true
	  }	
	  isAuth = checkAuth();	// default to false, return true only if fxn completes. 
	  

JSON file structure { "users": [ array of users ], "posts": [ array of posts ]