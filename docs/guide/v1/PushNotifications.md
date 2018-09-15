# Possible Notifications

## ROOM_SEND_MESSAGE

| Type 	                    | Template Example 	                                    | Text Arguments      	                                        | Parameters          	|
|------------	            |----------	                                            |------------------	                                            |------------------	    |
| MESSAGE_TEXT    	        | {1}: {2}      	                                    | 1. Message author<br/>2. Message body                         | roomId<br/>messageId  |
| MESSAGE_NOTEXT  	        | {1} sent you a message                                | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_IMAGE    	        | {1} sent you a photo                                  | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_VIDEO    	        | {1} sent you a video                                  | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_AUDIO    	        | {1} sent you a audio                                  | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_VOICE    	        | {1} sent you a voice message                          | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_GIF    	        | {1} sent you a gif                                    | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_FILE    	        | {1} sent you a file                                   | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_LOCATION          | {1} sent you a location                               | 1. Message author                                             | roomId<br/>messageId  |
| MESSAGE_CONTACT           | {1} shared a contact with you                         | 1. Message author                                             | roomId<br/>messageId  |
| GROUP_MESSAGE_TEXT    	| {1}@{2}: {3}      	                                | 1. Message author<br/>2.Group title<br/>3. Message body       | roomId<br/>messageId  |
| GROUP_MESSAGE_NOTEXT    	| {1} sent a message to the group {2}                   | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_IMAGE    	| {1} sent a photo to the group {2}                     | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_VIDEO    	| {1} sent a video to the group {2}                     | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_AUDIO    	| {1} sent a audio to the group {2}                     | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_VOICE    	| {1} sent a voice message to the group {2}             | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_GIF    	    | {1} sent a gif to the group {2}                       | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_FILE    	| {1} sent a file to the group {2}                      | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_LOCATION    | {1} sent a location to the group {2}                  | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| GROUP_MESSAGE_CONTACT     | {1} shared a contact with you in the group {2}        | 1. Message author<br/>2.Group title                           | roomId<br/>messageId  |
| CHANNEL_MESSAGE_TEXT    	| {1}: {2}      	                                    | 1.Channel title<br/>2. Message body                           | roomId<br/>messageId  |
| CHANNEL_MESSAGE_NOTEXT  	| {1} posted a message     	                            | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_IMAGE    	| {1} posted a photo                                    | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_VIDEO    	| {1} posted a video                                    | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_AUDIO    	| {1} posted a audio                                    | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_VOICE    	| {1} posted a voice message                            | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_GIF    	| {1} posted a gif                                      | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_FILE    	| {1} posted a file                                     | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_LOCATION  | {1} posted a location                                 | 1.Channel title                                               | roomId<br/>messageId  |
| CHANNEL_MESSAGE_CONTACT   | {1} posted a contact                                  | 1.Channel title                                               | roomId<br/>messageId  |

## SIGNALING_OFFER

| Type 	                                    | Template Example 	                    | Text Arguments      	            | Parameters          	|
|------------	                            |----------	                            |------------------	                |------------------	    |
| SIGNALING_OFFER_VOICE_CALLING    	        | Incoming voice call from {1}	        | 1. Peer name                      |                       |
| SIGNALING_OFFER_VOICE_CALLING    	        | Incoming video call from {1}	        | 1. Peer name                      |                       |
| SIGNALING_OFFER_SCREEN_SHARING    	    | Screen sharing request from {1}	    | 1. Peer name                      |                       |
| SIGNALING_OFFER_SECRET_CHAT    	        | Secret chat request from {1}	        | 1. Peer name                      |                       |

