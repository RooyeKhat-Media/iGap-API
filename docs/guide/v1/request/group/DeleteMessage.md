Delete a message from a group room

# Request
message [#320](../../proto/README.md#action_320)

# Response
message [#30320](../../proto/README.md#action_30320)

# List of access rule
* OWNER
* ADMIN
* MODERATOR
* MEMBER

| User role 	| Own message            | MEMBER message                  	| MODERATOR message                 | ADMIN message                     | OWNER message                     |
|--------------	|----------------------- |-------------------------------	|-------------------------------	|-------------------------------	|-------------------------------    |
| OWNER         | :white_check_mark:     | :white_check_mark: 	            | :white_check_mark: 	            | :white_check_mark: 	            | :white_check_mark: 	            |
| ADMIN        	| :white_check_mark: 	 | :white_check_mark: 	            | :white_check_mark: 	            | :negative_squared_cross_mark: 	| :negative_squared_cross_mark:     |
| MODERATOR     | :white_check_mark: 	 | :white_check_mark: 	            | :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark:     |
| MEMBER        | :white_check_mark: 	 | :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark:     |
