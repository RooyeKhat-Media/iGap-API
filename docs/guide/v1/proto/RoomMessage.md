
| Parameters      	| Required 	                        | Description                                     	                |
|-----------------	|----------	                        |-------------------------------------------------	                |
| message_id      	| :white_check_mark:      	        | Message id                                      	                |
| message_version 	| :white_check_mark:      	        | Message version                                 	                |
| status          	| :one:      	                    | Message status ([RoomMessageStatus](RoomMessageStatus.md))    	|
| status_version  	| :one:      	                    | Message status version                          	                |
| message_type    	| :one:      	                    | Message type ([RoomMessageType](RoomMessageType.md))  	        |
| message         	| :one: :two:      	                | Message text                                    	                |
| attachment      	| :one: :two:      	                | Attachments ([File](File.md))                                     |
| user_id         	| :one:      	                    | Message sender's user id                        	                |
| location        	| :one: :two:      	                | Location info ([RoomMessageLocation](RoomMessageLocation.md)) 	|
| log             	| :one: :two:      	                | Log ([RoomMessageLog](RoomMessageLog.md))                         |
| edited          	| :one:      	                    | Indicates whether or not the message is edited  	                |
| update_time     	| :one:      	                    | Message update time                             	                |
| deleted     	    | :white_check_mark:      	        | Set to true if message is deleted                	                |


:one: When message is not deleted

:two: Requirements depend on message_type according to following table

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