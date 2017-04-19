# join
Join to the private room

| Parameters 	| Required 	                | Description      	    |
|------------	|----------	                |------------------	    |
| invite    	| :white_check_mark:      	| Invite token          |
  	
# resolve
Resolve the username

| Parameters 	| Required 	                    | Description      	    |
|------------	|----------	                    |------------------	    |
| domain    	| :white_check_mark:      	    | Username              |
| post    	    | :negative_squared_cross_mark: | Room message id       |

# new_device
Verify the identity of new device 

| Parameters 	| Required 	                | Description      	    |
|------------	|----------	                |------------------	    |
| token      	| :white_check_mark:      	| Login token           |

# add_contact
Add contact (Just fill add contact form and let user to edit the form data)

| Parameters 	    | Required 	                            | Description      	                                                                                        |
|------------	    |----------	                            |------------------	                                                                                        |
| phone      	    | :white_check_mark:      	            | Phone number in E.164 number formatting [+][country code][subscriber number including area code]          |
| first_name      	| :negative_squared_cross_mark:      	| First name                                                                                                |
| last_name      	| :negative_squared_cross_mark:      	| Last name                                                                                                 |