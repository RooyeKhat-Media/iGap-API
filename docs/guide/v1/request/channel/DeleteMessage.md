Delete a message from a channel room

# Request
message [#411](../../proto/README.md#action_411)

# Response
message [#30411](../../proto/README.md#action_30411)

# List of access rule
* OWNER
* ADMIN
* MODERATOR

| User role 	| Own message            | MODERATOR message                | ADMIN message                     | OWNER message                     |
|--------------	|----------------------- |-------------------------------	|-------------------------------	|-------------------------------    |
| OWNER         | :white_check_mark:     | :white_check_mark: 	            | :white_check_mark: 	            | :white_check_mark: 	            |
| ADMIN        	| :white_check_mark: 	 | :white_check_mark: 	            | :negative_squared_cross_mark: 	| :negative_squared_cross_mark:     |
| MODERATOR     | :white_check_mark: 	 | :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark:     |
