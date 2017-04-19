| Parameters                    	| Required 	                | Description                                                               |
|-------------------------------	|----------	                |---------------------------------	       			                        |
| request     			          	| :white_check_mark:      	| [Request](Request.md)              		                                |
| message_type                  	| :white_check_mark:      	| Message type ([RoomMessageType](message_type.md))		                    |
| room_id 		                	| :white_check_mark:      	| Chatroom id                         	    	                            |
| message                       	| :one:      	            | Message text                        	    	    	                    |
| attachment                    	| :one:      	            | Attachments                     	    	   			                    |
| location 	   					    | :one:      	            | User's location info ([RoomMessageLocation](RoomMessageLocation.md))      |
| log           				 	| :one:      	            | Log ([RoomMessageLog](RoomMessageLog.md))							        |
| contact         				 	| :one:      	            | Contact ([RoomMessageContact](RoomMessageContact.md))					    |



:one: Requirements depends on message_type according to following table

| message_type 	| message                       	| attachment                    	| location                      	| log                           	| contact                        	|
|--------------	|-------------------------------	|-------------------------------	|-------------------------------	|-------------------------------	|-------------------------------	|
| TEXT         	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| IMAGE        	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| IMAGE_TEXT   	| :white_check_mark:            	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| VIDEO        	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| VIDEO_TEXT   	| :white_check_mark:            	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| AUDIO        	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| AUDIO_TEXT   	| :white_check_mark:            	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| VOICE        	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| GIF         	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| FILE         	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| FILE_TEXT    	| :white_check_mark:            	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| LOCATION     	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	|
| LOG          	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :white_check_mark:            	| :negative_squared_cross_mark: 	|
| CONTACT     	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark: 	| :negative_squared_cross_mark:    	| :white_check_mark:             	|