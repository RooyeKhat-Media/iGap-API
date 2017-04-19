
[TOC]
# Errors
**Error types**
* Real Error : Both server and client receive these errors and must do reaction
* Virtual Error : Only server receive these errors

## Error message
When a real error occurred , message [#0](../proto/README.md#action_0) will be sent to the client

## Symbols
| Symbol 	                                | Detail 	                        |
|------------	                            |--------	                        |
| :triangular_flag_on_post: :one:          	| wait parameter is required      	|


# System Errors (xx)
### Error 1 - BAD_REQUEST
Request format is invalid

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 2 - LOGIN_REQUIRED
Login is required to perform this action

| Minor Code 	| Detail 	| Reaction 	                                                            |
|------------	|--------	|----------	                                                            |
| *          	| *      	| Send message message [#102](../proto/README.md#action_102)        	|


### Error 3 - NEW_CLIENT_IN_SESSION
New client connected in this session , so you will be kicked out

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 4 - FORBIDDEN
This operation is not permitted

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 5 - TIMEOUT
The client timed out waiting for the response

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 6 - RELATION_ERROR
For related requests , if once get error , RELATION_ERROR will be sent to others

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 7 - INTERNAL_SERVER_ERROR
Internal server error is ocuured

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# User Errors(1xx)
### Error 100 - USER_REGISTER_BAD_PAYLOAD
Bad payload for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid countryCode      	| *        	|
| 2          	| Invalid phoneNumber      	| *        	|


### Error 101 - USER_REGISTER_INTERNAL_SERVER_ERROR
Internal server error for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 135 - USER_REGISTER_BLOCKED_USER
User is blocked for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 136 - USER_REGISTER_MAX_TRY_LOCK
The code is entered incorrectly too much for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 137 - USER_REGISTER_MAX_SEND_LOCK
Verify code has been forwarded exceedingly. for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 102 - USER_VERIFY_BAD_PAYLOAD
Bad payload for request [#101](../proto/README.md#action_101)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid code      	| *        	|
| 2          	| Invalid username      | *        	|


### Error 103 - USER_VERIFY_INTERNAL_SERVER_ERROR
Internal server error for request [#101](../proto/README.md#action_101)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 104 - USER_VERIFY_USER_NOT_FOUND
There is no registered user with given username

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 105 - USER_VERIFY_BLOCKED_USER
User is blocked , You cannot verify the user

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 106 - USER_VERIFY_INVALID_CODE
Verification code is invalid

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 107 - USER_VERIFY_EXPIRED_CODE
Verification code is expired

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### :triangular_flag_on_post: :one: Error 108 - USER_VERIFY_MAX_TRY_LOCK
Verification code is locked for a while due to too many tries

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 109 - USER_LOGIN_BAD_PAYLOAD
Bad payload for request [#102](../proto/README.md#action_102)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid token      	| *        	|


### Error 110 - USER_LOGIN_INTERNAL_SERVER_ERROR
Internal server error for request [#102](../proto/README.md#action_102)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 111 - USER_LOGIN_FAILED
Login failed

| Minor Code 	| Detail 	            | Reaction 	                        |
|------------	|--------	            |----------	                        |
| *          	| *      	            | Go to registration page        	|
| 4          	| User is blocked      	| *        	                        |

### Error 112 - USER_PROFILE_SET_NICKNAME_BAD_PAYLOAD
Bad payload for request [#105](../proto/README.md#action_105)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid nickname      	| *        	|


### Error 113 - USER_PROFILE_SET_NICKNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#105](../proto/README.md#action_105)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 114 - USER_PROFILE_SET_EMAIL_BAD_PAYLOAD
Bad payload for request [#103](../proto/README.md#action_103)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid email      	| *        	|


### Error 115 - USER_PROFILE_SET_EMAIL_INTERNAL_SERVER_ERROR
Internal server error for request [#103](../proto/README.md#action_103)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 116 - USER_PROFILE_SET_GENDER_BAD_PAYLOAD
Bad payload for request [#104](../proto/README.md#action_104)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid gender      	| *        	|


### Error 117 - USER_PROFILE_SET_GENDER_INTERNAL_SERVER_ERROR
Internal server error for request [#104](../proto/README.md#action_104)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 118 - USER_CONTACTS_IMPORT_BAD_PAYLOAD
Bad payload for request [#106](../proto/README.md#action_106)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid phone      	    | *        	|
| 2          	| Invalid first_name      	| *        	|
| 3          	| Invalid last_name      	| *        	|
| 4          	| Invalid force      	    | *        	|

### Error 119 - USER_CONTACTS_IMPORT_INTERNAL_SERVER_ERROR
Internal server error for request [#106](../proto/README.md#action_106)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 120 - USER_CONTACTS_GET_LIST_BAD_PAYLOAD
Bad payload for request [#107](../proto/README.md#action_107)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 121 - USER_CONTACTS_GET_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#107](../proto/README.md#action_107)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 122 - USER_CONTACTS_DELETE_BAD_PAYLOAD
Bad payload for request [#108](../proto/README.md#action_108)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid phone      	    | *        	|

### Error 123 - USER_CONTACTS_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#108](../proto/README.md#action_108)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 124 - USER_CONTACTS_EDIT_BAD_PAYLOAD
Bad payload for request [#109](../proto/README.md#action_109)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid phone      	                    | *        	|
| 2          	| Invalid first_name      	                | *        	|
| 3          	| Invalid last_name      	                | *        	|
| 4          	| first_name or last_name is required      	| *        	|

### Error 125 - USER_CONTACTS_EDIT_INTERNAL_SERVER_ERROR
Internal server error for request [#109](../proto/README.md#action_109)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 126 - USER_PROFILE_GET_NICKNAME_BAD_PAYLOAD
Bad payload for request [#112](../proto/README.md#action_112)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 127 - USER_PROFILE_GET_NICKNAME_INTERNAL_SERVER_ERROR 
Internal server error for request [#112](../proto/README.md#action_112)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 128 - USER_PROFILE_GET_EMAIL_BAD_PAYLOAD
Bad payload for request [#110](../proto/README.md#action_110)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 129 - USER_PROFILE_GET_EMAIL_INTERNAL_SERVER_ERROR
Internal server error for request [#110](../proto/README.md#action_110)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 130 - USER_PROFILE_GET_GENDER_BAD_PAYLOAD
Bad payload for request [#111](../proto/README.md#action_111)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 131 - USER_PROFILE_GET_GENDER_INTERNAL_SERVER_ERROR
Internal server error for request [#111](../proto/README.md#action_111)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 132 - USER_USERNAME_TO_ID_BAD_PAYLOAD 
Bad payload for request [#113](../proto/README.md#action_113)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| 1          	| *      	| *        	|

### Error 133 - USER_USERNAME_TO_ID_INTERNAL_SERVER_ERROR
Internal server error for request [#113](../proto/README.md#action_113)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 134 - USER_USERNAME_TO_ID_NOT_FOUND
No such user is found for request [#113](../proto/README.md#action_113)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid username      	| *        	|

# Chat Errors(2xx)
### Error 200 - CHAT_GET_ROOM_BAD_PAYLOAD
Bad payload for request [#200](../proto/README.md#action_200)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid peerId      	| *        	|


### Error 201 - CHAT_GET_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#200](../proto/README.md#action_200)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 202 - CHAT_GET_ROOM_PEER_NOT_FOUND
There is no active user with given peerId

| Minor Code 	| Detail 	                                        | Reaction 	|
|------------	|--------	                                        |----------	|
| *          	| *      	                                        | *        	|

### Error 203 - CHAT_SEND_MESSAGE_BAD_PAYLOAD
Bad payload for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail 	                            | Reaction 	|
|------------	|--------	                            |----------	|
| 1          	| Invalid roomId      	                | *        	|
| 2          	| Invalid message      	                | *        	|
| 3          	| Invalid attachment      	            | *        	|
| 4          	| Invalid attachment      	            | *        	|
| 5          	| Invalid attachment      	            | *        	|
| 6          	| Invalid attachment      	            | *        	|
| 7          	| Invalid attachment      	            | *        	|
| 8          	| Invalid attachment      	            | *        	|
| 9          	| Invalid message      	                | *        	|
| 10          	| Invalid attachment      	            | *        	|
| 11          	| Invalid message      	                | *        	|
| 12          	| Invalid attachment      	            | *        	|
| 13          	| Invalid message      	                | *        	|
| 14          	| Invalid attachment      	            | *        	|
| 15          	| Invalid message      	                | *        	|
| 16          	| Invalid attachment      	            | *        	|
| 17          	| Invalid location 	                    | *        	|
| 18          	| Invalid location.lat                  | *        	|
| 19          	| Invalid location.lon                  | *        	|
| 20          	| Invalid log            	            | *        	|
| 21          	| Invalid log.type      	            | *        	|
| 22          	| Invalid contact      	                | *        	|
| 23          	| Invalid messageType      	            | *        	|
| 24          	| No such file is found      	        | *        	|
| 25          	| Invalid replyTo      	                | *        	|
| 26          	| Invalid forwardFrom.roomId            | *        	|
| 27          	| Invalid forwardFrom.messageId         | *        	|
| 28          	| Invalid forwardFrom                   | *        	|
| 29          	| Both replyTo and forwardFrom are set  | *        	|
| 30          	| Invalid message      	                | *        	|
| 31          	| Invalid attachment      	            | *        	|
| 32          	|  **Message is too long**      	    | *        	|

### Error 204 - CHAT_SEND_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 205 - CHAT_SEND_MESSAGE_FORBIDDEN
This operation is not permitted for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 206 - CHAT_UPDATE_STATUS_BAD_PAYLOAD
Bad payload for request [#202](../proto/README.md#action_202)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid roomId      	    | *        	|
| 2          	| Invalid messageId      	| *        	|
| 3          	| Invalid status      	    | *        	|

### Error 207 - CHAT_UPDATE_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#202](../proto/README.md#action_202)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 208 - CHAT_UPDATE_STATUS_FORBIDDEN
This operation is not permitted for request [#202](../proto/README.md#action_202)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 209 - CHAT_EDIT_MESSAGE_BAD_PAYLOAD
Bad payload for request [#203](../proto/README.md#action_203)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid roomId      	    | *        	|
| 2          	| Invalid messageId      	| *        	|
| 3         	| Invalid message      	    | *        	|

### Error 210 - CHAT_EDIT_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#203](../proto/README.md#action_203)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 211 - CHAT_EDIT_MESSAGE_FORBIDDEN
This operation is not permitted for request [#203](../proto/README.md#action_203)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 212 - CHAT_DELETE_MESSAGE_BAD_PAYLOAD
Bad payload for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid roomId      	    | *        	|
| 2         	| Invalid messageId      	| *        	|

### Error 213 - CHAT_DELETE_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 214 - CHAT_DELETE_MESSAGE_FORBIDDEN
This operation is not permitted for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 215 - CHAT_CLEAR_MESSAGE_BAD_PAYLOAD
Bad payload for request [#205](../proto/README.md#action_205)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid roomId      	| *        	|
| 2          	| Invalid clearId      	| *        	|


### Error 216 - CHAT_CLEAR_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#205](../proto/README.md#action_205)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 217 - CHAT_CLEAR_MESSAGE_FORBIDDEN
This operation is not permitted for request [#205](../proto/README.md#action_205)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 218 - CHAT_DELETE_BAD_PAYLOAD 
Bad payload for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid roomId      	| *        	|

### Error 219 - CHAT_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 220 - CHAT_DELETE_FORBIDDEN
This operation is not permitted for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# Group Errors(3xx)
### Error 300 - GROUP_CREATE_BAD_PAYLOAD
Bad payload for request [#300](../proto/README.md#action_300)

| Minor Code 	| Detail 	            | Reaction 	    |
|------------	|--------	            |----------	    |
| 1          	| Invalid name          | *             |
| 2        	    | Invalid description   | *             |

### Error 301 - GROUP_CREATE_INTERNAL_SERVER_ERROR
Internal server error for request [#300](../proto/README.md#action_300)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 302 - GROUP_ADD_MEMBER_BAD_PAYLOAD
Bad payload for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	                        | Reaction 	   |
|------------	|--------	                        |----------    |
| 1          	| Invalid roomId                    | *            |
| 2             | Invalid userId                    | *            |
| 3             | Invalid startMessageId            | *            |
| 4             | Invalid role                      | *            |

### Error 303 - GROUP_ADD_MEMBER_INTERNAL_SERVER_ERROR
Internal server error for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 304 - GROUP_ADD_MEMBER_EXISTS 
User is already in this room for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 305 - GROUP_ADD_MEMBER_FORBIDDEN 
This operation is not permitted for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 306 - GROUP_SEND_MESSAGE_BAD_PAYLOAD
Bad payload for request [#310](../proto/README.md#action_310)

| Minor Code 	| Detail 	                            | Reaction 	|
|------------	|--------	                            |----------	|
| 1          	| Invalid roomId      	                | *        	|
| 2          	| Invalid message      	                | *        	|
| 3          	| Invalid attachment      	            | *        	|
| 4          	| Invalid attachment      	            | *        	|
| 5          	| Invalid attachment      	            | *        	|
| 6          	| Invalid attachment      	            | *        	|
| 7          	| Invalid attachment      	            | *        	|
| 8          	| Invalid attachment      	            | *        	|
| 9          	| Invalid message      	                | *        	|
| 10          	| Invalid attachment      	            | *        	|
| 11          	| Invalid message      	                | *        	|
| 12          	| Invalid attachment      	            | *        	|
| 13          	| Invalid message      	                | *        	|
| 14          	| Invalid attachment      	            | *        	|
| 15          	| Invalid message      	                | *        	|
| 16          	| Invalid attachment      	            | *        	|
| 17          	| Invalid location 	                    | *        	|
| 18          	| Invalid location.lat                  | *        	|
| 19          	| Invalid location.lon                  | *        	|
| 20          	| Invalid log            	            | *        	|
| 21          	| Invalid log.type      	            | *        	|
| 22          	| Invalid contact      	                | *        	|
| 23          	| Invalid messageType      	            | *        	|
| 24          	| No such file is found      	        | *        	|
| 25          	| Invalid replyTo      	                | *        	|
| 26          	| Invalid forwardFrom.roomId            | *        	|
| 27          	| Invalid forwardFrom.messageId         | *        	|
| 28          	| Invalid forwardFrom                   | *        	|
| 29          	| Both replyTo and forwardFrom are set  | *        	|
| 30          	| Invalid message      	                | *        	|
| 31          	| Invalid attachment      	            | *        	|
| 32          	|  **Message is too long**      	    | *        	|

### Error 307 - GROUP_SEND_MESSAGE_INTERNAL_SERVER_ERROR 
Internal server error for request [#310](../proto/README.md#action_310)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 308 - GROUP_SEND_MESSAGE_FORBIDDEN 
This operation is not permitted for request [#310](../proto/README.md#action_310)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 309 - GROUP_UPDATE_STATUS_BAD_PAYLOAD
Bad payload for request [#311](../proto/README.md#action_311)

| Minor Code 	| Detail 	                | Reaction  |
|------------	|--------	                |---------  |
| 1             | Invalid roomId            |           |
| 2             | Invalid massageId         |           |
| 3       	    | Invalid massageStatus     |           |

### Error 310 - GROUP_UPDATE_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#311](../proto/README.md#action_311)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 311 - GROUP_UPDATE_STATUS_FORBIDDEN
This operation is not permitted for request [#311](../proto/README.md#action_311)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 315 - GROUP_CLEAR_MESSAGE_BAD_PAYLOAD
Bad payload for request [#304](../proto/README.md#action_304)

| Minor Code 	| Detail 	             | Reaction  |
|------------	|--------	             |---------  |
| 1             | Invalid roomId         |           |
| 2             | Invalid clearId        |           |

### Error 316 - GROUP_CLEAR_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#311](../proto/README.md#action_304)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 317 - GROUP_CLEAR_MESSAGE_FORBIDDEN
This operation is not permitted for request [#304](../proto/README.md#action_304)

| Minor Code 	| Detail 	                                                | Reaction  |
|------------	|--------	                                                |---------  |
| 1             | clear id can not be fewer than the first massage id       |           |


### Error 318 - GROUP_ADD_MODERATOR_BAD_PAYLOAD
Bad payload for request [#303](../proto/README.md#action_303)

| Minor Code 	| Detail 	              | Reaction  |
|------------	|--------	              |---------  |
| *             | *                       |           |
| 1             | Invalid roomId          |           |
| 2             | Invalid memberId        |           |

### Error 319 - GROUP_ADD_MODERATOR_INTERNAL_SERVER_ERROR
Internal server error for request [#303](../proto/README.md#action_303)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 320 - GROUP_ADD_MODERATOR_FORBIDDEN
This operation is not permitted for request [#303](../proto/README.md#action_303)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 321 - GROUP_ADD_ADMIN_BAD_PAYLOAD
Bad payload in for request [#302](../proto/README.md#action_302)

### Error 322 - GROUP_ADD_ADMIN_INTERNAL_SERVER_ERROR
Internal server error for request [#302](../proto/README.md#action_302)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 323 - GROUP_ADD_ADMIN_FORBIDDEN  
This operation is not permitted for request [#302](../proto/README.md#action_302)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 324 - GROUP_KICK_MODERATOR_BAD_PAYLOAD
Bad payload for request [#308](../proto/README.md#action_308)

| Minor Code 	| Detail 	                | Reaction  |
|------------	|--------	                |---------- |
| *             | *                         |           |
| 1             | Invalid roomId            |           |
| 2             | Invalid memberId          |           |

### Error 325 - GROUP_KICK_MODERATOR_INTERNAL_SERVER_ERROR 
Internal server error for request [#308](../proto/README.md#action_308)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 326 - GROUP_KICK_MODERATOR_FORBIDDEN 
This operation is not permitted for request [#308](../proto/README.md#action_308)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 327 - GROUP_KICK_ADMIN_BAD_PAYLOAD 
Bad payload for request [#306](../proto/README.md#action_306)

| Minor Code 	| Detail 	                | Reaction  |
|------------	|--------	                |---------- |
| *             | *                         |           |
| 1             | Invalid roomId            |           |
| 2             | Invalid memberId          |           |

### Error 328 - GROUP_KICK_ADMIN_INTERNAL_SERVER_ERROR  
Internal server error for request [#306](../proto/README.md#action_306)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	| 

### Error 329 - GROUP_KICK_ADMIN_FORBIDDEN
This operation is not permitted for request [#306](../proto/README.md#action_306)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	| 

### Error 330 - GROUP_EDIT_BAD_PAYLOAD
Bad payload for request [#305](../proto/README.md#action_305)

| Minor Code 	| Detail 	             | Reaction  |
|------------	|--------	             |---------  |
| 1             | Invalid roomid         |           |
| 2             | Invalid username       |           |
| 3       	    | Invalid description    |           |

### Error 331 - GROUP_EDIT_INTERNAL_SERVER_ERROR 
Internal server error for request [#305](../proto/README.md#action_305)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 332 - GROUP_KICK_MEMBER_BAD_PAYLOAD 
Bad payload for request [#307](../proto/README.md#action_307)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid roomId      	                    | *        	|
| 2          	| Invalid memberId      	                | *        	|


### Error 333 - GROUP_KICK_MEMBER_INTERNAL_SERVER_ERROR
Internal server error for request [#307](../proto/README.md#action_307)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 334 - GROUP_KICK_MEMBER_FORBIDDEN
This operation is not permitted for request [#307](../proto/README.md#action_307)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 335 - GROUP_LEFT_BAD_PAYLOAD
Bad payload for request [#309](../proto/README.md#action_309)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 336 - GROUP_LEFT_INTERNAL_SERVER_ERROR
Internal server error for request [#309](../proto/README.md#action_309)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	| 

### Error 337 - GROUP_LEFT_FORBIDDEN 
This operation is not permitted for request [#309](../proto/README.md#action_309)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# Channel Errors(4xx)
### Error 406 - CHANNEL_SEND_MESSAGE_BAD_PAYLOAD
Bad payload for request [#410](../proto/README.md#action_410)

| Minor Code 	| Detail 	                            | Reaction 	|
|------------	|--------	                            |----------	|
| 1          	| Invalid roomId      	                | *        	|
| 2          	| Invalid message      	                | *        	|
| 3          	| Invalid attachment      	            | *        	|
| 4          	| Invalid attachment      	            | *        	|
| 5          	| Invalid attachment      	            | *        	|
| 6          	| Invalid attachment      	            | *        	|
| 7          	| Invalid attachment      	            | *        	|
| 8          	| Invalid attachment      	            | *        	|
| 9          	| Invalid message      	                | *        	|
| 10          	| Invalid attachment      	            | *        	|
| 11          	| Invalid message      	                | *        	|
| 12          	| Invalid attachment      	            | *        	|
| 13          	| Invalid message      	                | *        	|
| 14          	| Invalid attachment      	            | *        	|
| 15          	| Invalid message      	                | *        	|
| 16          	| Invalid attachment      	            | *        	|
| 17          	| Invalid location 	                    | *        	|
| 18          	| Invalid location.lat                  | *        	|
| 19          	| Invalid location.lon                  | *        	|
| 20          	| Invalid log            	            | *        	|
| 21          	| Invalid log.type      	            | *        	|
| 22          	| Invalid contact      	                | *        	|
| 23          	| Invalid messageType      	            | *        	|
| 24          	| No such file is found      	        | *        	|
| 25          	| Invalid replyTo      	                | *        	|
| 26          	| Invalid forwardFrom.roomId            | *        	|
| 27          	| Invalid forwardFrom.messageId         | *        	|
| 28          	| Invalid forwardFrom                   | *        	|
| 29          	| Both replyTo and forwardFrom are set  | *        	|
| 30          	| Invalid message      	                | *        	|
| 31          	| Invalid attachment      	            | *        	|
| 32          	|  **Message is too long**      	    | *        	|

# Info Errors(5xx)
### Error 500 - INFO_LOCATION_NOT_FOUND
Cannot detect your location

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 501 - INFO_COUNTRY_BAD_PAYLOAD
Bad payload for request [#501](../proto/README.md#action_501)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid isoCode      	| *        	|

### Error 502 - INFO_PAGE_BAD_PAYLOAD
Bad payload for request [#503](../proto/README.md#action_503)

| Minor Code 	| Detail 	            | Reaction 	|
|------------	|--------	            |----------	|
| 1          	| Invalid id      	    | *        	|

### Error 503 - INFO_PAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#503](../proto/README.md#action_503)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# Client Errors(6xx)
### Error 600 - CLIENT_CONDITION_BAD_PAYLOAD
Bad payload for request [#600](../proto/README.md#action_600)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid roomId      	                    | *        	|
| 2          	| Invalid messageVersion      	            | *        	|
| 3          	| Invalid statusVersion      	            | *        	|
| 4          	| Invalid deleteVersion      	            | *        	|
| 5          	| Invalid offlineDeleted      	            | *        	|
| 6          	| Invalid offline_edited.message_id      	| *        	|
| 7          	| Invalid offline_edited.message      	    | *        	|
| 8          	| Invalid offlineSeen      	                | *        	|
| 9          	| Invalid clearId      	                    | *        	|
| 10          	| Invalid cacheStartId      	            | *        	|
| 11          	| Invalid cacheEndId      	                | *        	|
| 12          	| Invalid offlineMute      	                | *        	|
| 13          	| Duplicated room in payload                | *        	|

### Error 601 - CLIENT_CONDITION_INTERNAL_SERVER_ERROR
Internal server error for request [#600](../proto/README.md#action_600)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 602 - CLIENT_UPDATE_MESSAGE_BAD_PAYLOAD
Virtual Error

### Error 603 - CLIENT_UPDATE_MESSAGE_INTERNAL_SERVER_ERROR
Virtual Error

### Error 604 - CLIENT_UPDATE_MESSAGE_FORBIDDEN
Virtual Error

### Error 605 - CLIENT_UPDATE_DELETE_MESSAGE_BAD_PAYLOAD
Virtual Error

### Error 606 - CLIENT_UPDATE_DELETE_MESSAGE_INTERNAL_SERVER_ERROR
Virtual Error

### Error 607 - CLIENT_UPDATE_MESSAGE_STATUS_BAD_PAYLOAD
Virtual Error

### Error 608 - CLIENT_UPDATE_MESSAGE_STATUS_INTERNAL_SERVER_ERROR
Virtual Error

### Error 609 - CLIENT_UPDATE_MESSAGE_STATUS_FORBIDDEN
Virtual Error

### Error 610 - CLIENT_GET_ROOM_LIST_BAD_PAYLOAD
Bad payload for request [#601](../proto/README.md#action_601)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 611 - CLIENT_GET_ROOM_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#601](../proto/README.md#action_601)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 612 - CLIENT_GET_ROOM_BAD_PAYLOAD
Bad payload for request [#](../proto/README.md#action_)

| Minor Code 	| Detail 	                | Reaction 	|
|------------	|--------	                |----------	|
| 1          	| Invalid room_id      	    | *        	|

### Error 613 - CLIENT_GET_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#](../proto/README.md#action_)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 614 - CLIENT_GET_ROOM_NOT_FOUND 
No such room is found for request [#602](../proto/README.md#action_602)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 615 - CLIENT_GET_ROOM_HISTORY_BAD_PAYLOAD
Bad payload for request [#603](../proto/README.md#action_603)

| Minor Code 	| Detail 	                     | Reaction  |
|------------	|--------	                     |---------  |
| 1             | Invalid roomId                 |           |
| 2             | Invalid firstMessageId         |           |

### Error 616 - CLIENT_GET_ROOM_HISTORY_INTERNAL_SERVER_ERROR
Internal server error for request [#603](../proto/README.md#action_603)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 617 - CLIENT_GET_ROOM_HISTORY_NOT_FOUND
There is no other massage for viewing. for request [#603](../proto/README.md#action_603)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# File Errors(7xx)

### Error 700 - FILE_UPLOAD_OPTION_BAD_PAYLOAD.
Bad payload for request [#700](../proto/README.md#action_700)

| Minor Code 	| Detail 	    | Reaction 	|
|------------	|--------	    |----------	|
| 1          	| Invalid size  | *        	|

### Error 701 - FILE_UPLOAD_OPTION_INTERNAL_SERVER_ERROR
Internal server error for request [#700](../proto/README.md#action_700)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 702 - FILE_UPLOAD_INIT_BAD_PAYLOAD
Bad payload for for request [#701](../proto/README.md#action_701)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid size    	                        | *        	|
| 2          	| Invalid firstBytes   	                    | *        	|
| 3             | Invalid lastBytes      	                | *        	|
| 4             | Invalid fileHash      	                | *        	|
| 5             | Invalid fileName      	                | *        	|

### Error 703 - FILE_UPLOAD_INIT_INTERNAL_SERVER_ERROR
Internal server error for request [#701](../proto/README.md#action_701)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 704 - FILE_UPLOAD_BAD_PAYLOAD
Bad payload for request [#702](../proto/README.md#action_702)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid token     	                    | *        	|
| 2          	| Invalid offset      	                    | *        	|
| 3          	| Invalid offset     	                    | *        	|
| 4          	| Invalid bytes     	                    | *        	|

### Error 705 - FILE_UPLOAD_INTERNAL_SERVER_ERROR
Internal server error for request [#702](../proto/README.md#action_702)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 706 - FILE_UPLOAD_FORBIDDEN
This operation is not permitted for request [#702](../proto/README.md#action_702)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 707 - FILE_UPLOAD_STATUS_BAD_PAYLOAD
Bad payload for request [#703](../proto/README.md#action_703)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid token     	                    | *        	|

### Error 708 - FILE_UPLOAD_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#703](../proto/README.md#action_703)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 709 - FILE_UPLOAD_STATUS_NOT_FOUND
No such file is found for request [#703](../proto/README.md#action_703)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 710 - FILE_INFO_BAD_PAYLOAD
Bad payload for request [#704](../proto/README.md#action_704)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid token     	                    | *        	|

### Error 711 - FILE_INFO_INTERNAL_SERVER_ERROR
Internal server error for request [#704](../proto/README.md#action_704)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 712 - FILE_INFO_NOT_FOUND
No such file is found for request [#704](../proto/README.md#action_704)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 713 - FILE_DOWNLOAD_BAD_PAYLOAD
Bad payload for request [#705](../proto/README.md#action_705)

| Minor Code 	| Detail 	                                | Reaction 	|
|------------	|--------	                                |----------	|
| 1          	| Invalid token     	                    | *        	|
| 2          	| Invalid offset     	                    | *        	|
| 3          	| Invalid maxLimit     	                    | *        	|
| 4          	| Invalid selector     	                    | *        	|
| 5          	| Invalid offset     	                    | *        	|

### Error 714 - FILE_DOWNLOAD_INTERNAL_SERVER_ERROR
Internal server error for request [#705](../proto/README.md#action_705)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 715 - FILE_DOWNLOAD_NOT_FOUND
No such file is found for request [#705](../proto/README.md#action_705)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|