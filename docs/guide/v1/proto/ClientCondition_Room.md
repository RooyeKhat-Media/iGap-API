| Parameters      	| Required 	                            | Description                                       	                                        |
|-----------------	|----------	                            |---------------------------------------------------	                                        |
| room_id         	| :white_check_mark:      	            | Room id                                           	                                        |
| message_version 	| :white_check_mark:      	            | The biggest message version available in the room 	                                        |
| status_version  	| :white_check_mark:      	            | The biggest message status available in the room  	                                        |
| delete_version  	| :white_check_mark:      	            | The biggest delete version available in the room  	                                        |
| offline_deleted 	| :negative_squared_cross_mark:      	| Ids of messages deleted in offline mode           	                                        |
| offline_edited  	| :negative_squared_cross_mark:      	| Messages edited in offline mode ( [OfflineEdited](ClientCondition_Room_OfflineEdited.md) )    |
| offline_seen    	| :negative_squared_cross_mark:      	| Ids of messages which got seen in offline mode    	                                        |
| clear_id        	| :white_check_mark:      	            | Cleanup id                                        	                                        |
| cache_start_id  	| :white_check_mark:      	            | Id of the first message available in the cache    	                                        |
| cache_end_id    	| :white_check_mark:      	            | Id of the last message available in the cache     	                                        |
| offline_mute    	| :white_check_mark:      	            | Mute status in offline mode ( [OfflineMute](ClientCondition_Room_OfflineMute.md) )            |
