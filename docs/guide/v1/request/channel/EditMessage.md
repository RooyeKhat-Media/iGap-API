Edit a channel room message

# Request
message [#425](../../proto/README.md#action_425)

# Response
message [#30425](../../proto/README.md#action_30425)

# List of access rule
* OWNER
* ADMIN
* MODERATOR

| User role 	| Own message            | MODERATOR message                 | ADMIN message                     | OWNER message                     |
|--------------	|----------------------- |-------------------------------	|-------------------------------	|-------------------------------    |
| OWNER         | :white_check_mark:     | :white_check_mark: 	            | :white_check_mark: 	            | :white_check_mark: 	            |
| ADMIN        	| :white_check_mark: 	 | :white_check_mark: 	            | :negative_squared_cross_mark: 	| :negative_squared_cross_mark:     |
| MODERATOR     | :white_check_mark: 	 | :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark:     |
