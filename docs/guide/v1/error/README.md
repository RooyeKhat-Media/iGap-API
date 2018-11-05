
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
The request is not valid

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 2 - LOGIN_REQUIRED
You have to log in first, then ask for performing this action

| Minor Code 	| Detail 	| Reaction 	                                                            |
|------------	|--------	|----------	                                                            |
| *          	| *      	| Send message message [#102](../proto/README.md#action_102)        	|


### Error 3 - NEW_CLIENT_IN_SESSION
New client just connected to this session, you are not allowed to continue

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 4 - FORBIDDEN
This operation is not permitted

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 5 - TIMEOUT
Getting response from the server has been timed out

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 6 - RELATION_ERROR
For related requests; if one gets error, RELATION_ERROR will be sent to the others

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 7 - INTERNAL_SERVER_ERROR
Internal server error is ocuured

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 8 - SESSION_IS_TERMINATED
Your session has been terminated by another device

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 9 - NICKNAME_REQUIRED
Nickname is required to be set before continue to do the action

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10 - FLOOD_REQUEST
You have exceeded the number of requests allowed

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# User Errors(1xx)
### Error 100 - USER_REGISTER_BAD_PAYLOAD
Bad payload for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail                  	        | Reaction 	|
|------------	|-------------------------	        |----------	|
| 1          	| Country code is invalid 	        | *        	|
| 2          	| Username is invalid     	        | *        	|
| 3          	| PreferenceMethod is invalid     	| *        	|

### Error 101 - USER_REGISTER_INTERNAL_SERVER_ERROR
Internal server error for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 135 - USER_REGISTER_BLOCKED_USER
Your user account is blocked for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 136 - USER_REGISTER_MAX_TRY_LOCK
The verification code was entered incorrectly too many times. Please try again later for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 137 - USER_REGISTER_MAX_SEND_LOCK
You have requested the verification code exceedingly for request [#100](../proto/README.md#action_100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 102 - USER_VERIFY_BAD_PAYLOAD
Bad payload for request [#101](../proto/README.md#action_101)

| Minor Code 	| Detail                       	| Reaction 	|
|------------	|------------------------------	|----------	|
| 1          	| Verification code is invalid 	| *        	|
| 2          	| Username is invalid          	| *        	|

### Error 103 - USER_VERIFY_INTERNAL_SERVER_ERROR
Internal server error for request [#101](../proto/README.md#action_101)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 104 - USER_VERIFY_USER_NOT_FOUND
There is no registered user with this given username

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 105 - USER_VERIFY_BLOCKED_USER
Your user account is blocked, you cannot verify the user

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 106 - USER_VERIFY_INVALID_CODE
Verification code is incorrect

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 107 - USER_VERIFY_EXPIRED_CODE
The Verification Code you entered has expired

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### :triangular_flag_on_post: :one: Error 108 - USER_VERIFY_MAX_TRY_LOCK
The Verification Code is locked now due to many tries

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 184 - USER_VERIFY_TWO_STEP_VERIFICATION_ENABLED
Two-step Verification is activated

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 109 - USER_LOGIN_BAD_PAYLOAD
Bad payload for request [#102](../proto/README.md#action_102)

| Minor Code 	| Detail                       	| Reaction 	|
|------------	|------------------------------	|----------	|
| 1          	| Token is invalid             	| *        	|
| 2          	| App Name is invalid          	| *        	|
| 3          	| App ID is invalid            	| *        	|
| 4          	| App Build Version is invalid 	| *        	|
| 5          	| App Version is invalid       	| *        	|
| 6          	| Platform is invalid          	| *        	|
| 7          	| Device is invalid            	| *        	|
| 8          	| Device Name is invalid       	| *        	|
| 9          	| Language is invalid          	| *        	|

### Error 110 - USER_LOGIN_INTERNAL_SERVER_ERROR
Internal server error for request [#102](../proto/README.md#action_102)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 111 - USER_LOGIN_FAILED
Login failed

| Minor Code 	| Detail                  	| Reaction 	                        |
|------------	|-------------------------	|----------	                        |
| *          	| *                       	| Go to registration page        	|
| 4          	| Your account is blocked 	| *        	                        |

### Error 10170 - USER_LOGIN_ALREADY_LOGGED_IN
You are forbidden to login again for request [#102](../proto/README.md#action_102)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 112 - USER_PROFILE_SET_NICKNAME_BAD_PAYLOAD
Bad payload for request [#105](../proto/README.md#action_105)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Nickname is not valid 	|          	|

### Error 113 - USER_PROFILE_SET_NICKNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#105](../proto/README.md#action_105)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 114 - USER_PROFILE_SET_EMAIL_BAD_PAYLOAD
Bad payload for request [#103](../proto/README.md#action_103)

| Minor Code 	| Detail                     	| Reaction 	|
|------------	|----------------------------	|----------	|
| 1          	| Email address in not valid 	| *        	|


### Error 115 - USER_PROFILE_SET_EMAIL_INTERNAL_SERVER_ERROR
Internal server error for request [#103](../proto/README.md#action_103)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 116 - USER_PROFILE_SET_GENDER_BAD_PAYLOAD
Bad payload for request [#104](../proto/README.md#action_104)

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| Gender is invalid 	| *        	|

### Error 117 - USER_PROFILE_SET_GENDER_INTERNAL_SERVER_ERROR
Internal server error for request [#104](../proto/README.md#action_104)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 118 - USER_CONTACTS_IMPORT_BAD_PAYLOAD
Bad payload for request [#106](../proto/README.md#action_106)

| Minor Code 	| Detail                    	| Reaction 	|
|------------	|---------------------------	|----------	|
| 1          	| Phone Number is not valid 	| *        	|
| 2          	| First Name is not valid   	| *        	|
| 3          	| Last Name is not valid    	| *        	|
| 4          	| Force is not valid        	| *        	|
| 5          	| Too many contacts         	| *        	|

### Error 119 - USER_CONTACTS_IMPORT_INTERNAL_SERVER_ERROR
Internal server error for request [#106](../proto/README.md#action_106)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10169 - USER_CONTACTS_IMPORT_FORBIDDEN
You are forbidden to do the action for request [#106](../proto/README.md#action_106)

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

| Minor Code 	| Detail                    	| Reaction 	|
|------------	|---------------------------	|----------	|
| 1          	| Phone Number is not valid 	| *        	|


### Error 123 - USER_CONTACTS_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#108](../proto/README.md#action_108)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 124 - USER_CONTACTS_EDIT_BAD_PAYLOAD
Bad payload for request [#109](../proto/README.md#action_109)

| Minor Code 	| Detail                             				| Reaction 	|
|------------	|------------------------------------				|----------	|
| 1          	| Phone Number is invalid            				| *       	|
| 2          	| First Name is invalid           				   	| *        	|
| 3          	| Last Name is invalid               				| *        	|
| 4          	| It's required to enter first name or last name 	| *        	|

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

### Error 138 - USER_AVATAR_ADD_BAD_PAYLOAD
Bad payload for request [#114](../proto/README.md#action_114)

| Minor Code 	| Detail                  	| Reaction 	|
|------------	|-------------------------	|----------	|
| 1          	| Attachment is not valid 	| *     	|

### Error 139 - USER_AVATAR_ADD_INTERNAL_SERVER_ERROR
Internal server error for request [#114](../proto/README.md#action_114)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 140 - USER_AVATAR_ADD_FORBIDDEN
You are forbidden to do the action for request [#114](../proto/README.md#action_114)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 141 - USER_AVATAR_DELETE_BAD_PAYLOAD
Bad payload for request [#115](../proto/README.md#action_115)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Avatar_ID is invalid 	| *        	|

### Error 142 - USER_AVATAR_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#115](../proto/README.md#action_115)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 143 - USER_AVATAR_DELETE_FORBIDDEN
You are forbidden to do the action for request [#115](../proto/README.md#action_115)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 144 - USER_AVATAR_GET_LIST_BAD_PAYLOAD
Bad payload for request [#116](../proto/README.md#action_116)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| User_ID is invalid 	| *        	|

### Error 145 - USER_AVATAR_GET_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#116](../proto/README.md#action_116)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 146 - USER_AVATAR_GET_LIST_FORBIDDEN
You are forbidden to do the action for request [#116](../proto/README.md#action_116)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 147 - USER_INFO_BAD_PAYLOAD
Bad payload for request [#117](../proto/README.md#action_117)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| User_ID is incorrect 	| *        	|

### Error 148 - USER_INFO_INTERNAL_SERVER_ERROR
Internal server error for request [#117](../proto/README.md#action_117)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 149 - USER_INFO_FORBIDDEN
You are forbidden to do the action for request [#117](../proto/README.md#action_117)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 150 - USER_GET_DELETE_TOKEN_BAD_PAYLOAD
Bad payload for request [#118](../proto/README.md#action_118)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 151 - USER_GET_DELETE_TOKEN_INTERNAL_SERVER_ERROR
Internal server error for request [#118](../proto/README.md#action_118)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 152 - USER_GET_DELETE_TOKEN_MAX_TRY_LOCK
Destruction Code for deleting user account has been entered incorrectly too many times for request [#118](../proto/README.md#action_118)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 153 - USER_GET_DELETE_TOKEN_MAX_SEND_LOCK
Destruction Code for deleting user account has been requested too many times

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 154 - USER_DELETE_BAD_PAYLOAD
Bad payload for request [#119](../proto/README.md#action_119)

| Minor Code 	| Detail                                  	| Reaction 	|
|------------	|-----------------------------------------	|----------	|
| 1          	| Account destruction token is incorrect  	| *        	|
| 2          	| Account destruction reason is not valid 	| *        	|

### Error 155 - USER_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#119](../proto/README.md#action_119)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 156 - USER_DELETE_INVALID_TOKEN
Account destruction token is incorrect for request [#119](../proto/README.md#action_119)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 157 - USER_DELETE_EXPIRED_TOKEN
Account destruction token you entered has expired for request [#119](../proto/README.md#action_119)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 158 - USER_DELETE_MAX_TRY_LOCK
Destruction Code for deleting user account has been entered incorrectly too many times for request [#119](../proto/README.md#action_119)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10171 - USER_DELETE_WALLET_RESTRICTION
You are forbidden to do the action due to wallet restriction for request [#119](../proto/README.md#action_119)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10172 - USER_DELETE_WALLET_BAD_GATEWAY
Server was not able to get a valid or any response from the Wallet server for request [#119](../proto/README.md#action_119)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 159 - USER_PROFILE_GET_SELF_REMOVE_BAD_PAYLOAD
Bad payload for request [#121](../proto/README.md#action_121)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 160 - USER_PROFILE_GET_SELF_REMOVE_INTERNAL_SERVER_ERROR
Internal server error for request [#121](../proto/README.md#action_121)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 161 - USER_PROFILE_SET_SELF_REMOVE_BAD_PAYLOAD
Bad payload for request [#120](../proto/README.md#action_120)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| Self_Remove is invalid 	| *        	|

### Error 162 - USER_PROFILE_SET_SELF_REMOVE_INTERNAL_SERVER_ERROR
Internal server error for request [#120](../proto/README.md#action_120)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 163 - USER_PROFILE_CHECK_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#122](../proto/README.md#action_122)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 164 - USER_PROFILE_UPDATE_USERNAME_BAD_PAYLOAD
Bad payload for request [#123](../proto/README.md#action_123)

| Minor Code 	| Detail                               	| Reaction 	|
|------------	|--------------------------------------	|----------	|
| 1          	| *                                    	| *        	|
| 2          	| Username is invalid                  	| *        	|
| 3          	| This username has already been taken 	| *        	|

### Error 165 - USER_PROFILE_UPDATE_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#123](../proto/README.md#action_123)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 175 - USER_PROFILE_UPDATE_USERNAME_UPDATE_LOCK
The username has been recently updated; please keep waiting until you can renew it or choose the latest one again for request [#123](../proto/README.md#action_123)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 166 - USER_UPDATE_STATUS_BAD_PAYLOAD
Bad payload for request [#124](../proto/README.md#action_124)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Status is incorrect 	| *        	|

### Error 167 - USER_UPDATE_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#124](../proto/README.md#action_124)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 168 - USER_SESSION_GET_ACTIVE_LIST_BAD_PAYLOAD
Bad payload for request [#125](../proto/README.md#action_125)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 169 - USER_SESSION_GET_ACTIVE_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#125](../proto/README.md#action_125)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 170 - USER_SESSION_TERMINATE_BAD_PAYLOAD
Bad payload for request [#126](../proto/README.md#action_126)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Session_ID is invalid 	| *        	|

### Error 171 - USER_SESSION_TERMINATE_INTERNAL_SERVER_ERROR
Internal server error for request [#126](../proto/README.md#action_126)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 172 - USER_SESSION_TERMINATE_FORBIDDEN
You are forbidden to do the action for request [#126](../proto/README.md#action_126)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 173 - USER_SESSION_LOGOUT_BAD_PAYLOAD
Bad payload for request [#127](../proto/README.md#action_127)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Session_ID is invalid 	| *        	|

### Error 174 - USER_SESSION_LOGOUT_INTERNAL_SERVER_ERROR
Internal server error for request [#127](../proto/README.md#action_127)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 176 - USER_CONTACTS_BLOCK_BAD_PAYLOAD
Bad payload for request [#128](../proto/README.md#action_128)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| User_ID is incorrect  	| *        	|

### Error 177 - USER_CONTACTS_BLOCK_INTERNAL_SERVER_ERROR
Internal server error for request [#128](../proto/README.md#action_128)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 178 - USER_CONTACTS_BLOCK_USER_NOT_FOUND
There is no user with this UserID for request [#128](../proto/README.md#action_128)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 179 - USER_CONTACTS_UNBLOCK_BAD_PAYLOAD
Bad payload for request [#129](../proto/README.md#action_129)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| User_ID is incorrect  	| *        	|

### Error 180 - USER_CONTACTS_UNBLOCK_INTERNAL_SERVER_ERROR
Internal server error for request [#129](../proto/README.md#action_129)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 181 - USER_CONTACTS_UNBLOCK_ALREADY_UNBLOCKED
This user has already been unblocked for request [#129](../proto/README.md#action_129)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 182 - USER_CONTACTS_GET_BLOCKED_LIST_BAD_PAYLOAD
Bad payload for request [#130](../proto/README.md#action_130)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 183 - USER_CONTACTS_GET_BLOCKED_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#130](../proto/README.md#action_130)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 185 - USER_TWO_STEP_VERIFICATION_GET_PASSWORD_DETAIL_BAD_PAYLOAD
Bad payload for request [#131](../proto/README.md#action_131)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 186 - USER_TWO_STEP_VERIFICATION_GET_PASSWORD_DETAIL_INTERNAL_SERVER_ERROR
Internal server error for request [#131](../proto/README.md#action_131)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 187 - USER_TWO_STEP_VERIFICATION_GET_PASSWORD_DETAIL_FORBIDDEN
You are forbidden to do the action for request [#131](../proto/README.md#action_131)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 188 - USER_TWO_STEP_VERIFICATION_GET_PASSWORD_DETAIL_NO_PASSWORD
You have not activated Two-step Verification yet for request [#131](../proto/README.md#action_131)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 189 - USER_TWO_STEP_VERIFICATION_VERIFY_PASSWORD_BAD_PAYLOAD
Bad payload for request [#132](../proto/README.md#action_132)

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| Password is wrong 	| *        	|

### Error 190 - USER_TWO_STEP_VERIFICATION_VERIFY_PASSWORD_INTERNAL_SERVER_ERROR
Internal server error for request [#132](../proto/README.md#action_132)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 191 - USER_TWO_STEP_VERIFICATION_VERIFY_PASSWORD_MAX_TRY_LOCK
Password has been entered incorrectly too many times for request [#132](../proto/README.md#action_132)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 192 - USER_TWO_STEP_VERIFICATION_VERIFY_PASSWORD_FORBIDDEN
You are forbidden to do the action for request [#132](../proto/README.md#action_132)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 193 - USER_TWO_STEP_VERIFICATION_VERIFY_PASSWORD_NO_PASSWORD
Password has not been set yet for request [#132](../proto/README.md#action_132)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 194 - USER_TWO_STEP_VERIFICATION_VERIFY_PASSWORD_INVALID_PASSWORD
Password is incorrect for request [#132](../proto/README.md#action_132)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 195 - USER_TWO_STEP_VERIFICATION_SET_PASSWORD_BAD_PAYLOAD
Bad payload for request [#133](../proto/README.md#action_133)

| Minor Code 	| Detail                                            	| Reaction 	|
|------------	|---------------------------------------------------	|----------	|
| 1          	| Old Password is wrong                             	| *        	|
| 2          	| New Password is invalid                           	| *        	|
| 3          	| Recovery E-mail is not valid                      	| *        	|
| 4          	| Recovery E-mail is not valid                      	| *        	|
| 5          	| The first recovery question is invalid            	| *        	|
| 6          	| Answer of the first recovery question is invalid  	| *        	|
| 7          	| The second recovery question is invalid           	| *        	|
| 8          	| Answer of the second recovery question is invalid 	| *        	|
| 9          	| Password hint is not valid                        	| *        	|

### Error 196 - USER_TWO_STEP_VERIFICATION_SET_PASSWORD_INTERNAL_SERVER_ERROR
Internal server error for request [#133](../proto/README.md#action_133)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 197 - USER_TWO_STEP_VERIFICATION_SET_PASSWORD_MAX_TRY_LOCK
Password has been entered incorrectly too many times for request [#133](../proto/README.md#action_133)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 198 - USER_TWO_STEP_VERIFICATION_SET_PASSWORD_INVALID_OLD_PASSWORD
The old password in not correct for request [#133](../proto/README.md#action_133)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 199 - USER_TWO_STEP_VERIFICATION_UNSET_PASSWORD_BAD_PAYLOAD
Bad payload for request [#134](../proto/README.md#action_134)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Password is invalid 	| *        	|

### Error 10100 - USER_TWO_STEP_VERIFICATION_UNSET_PASSWORD_INTERNAL_SERVER_ERROR
Internal server error for request [#134](../proto/README.md#action_134)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10101 - USER_TWO_STEP_VERIFICATION_UNSET_PASSWORD_MAX_TRY_LOCK
Password has been entered incorrectly too many times for request [#134](../proto/README.md#action_134)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10102 - USER_TWO_STEP_VERIFICATION_UNSET_PASSWORD_INVALID_PASSWORD
Password is not valid for request [#134](../proto/README.md#action_134)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| 1          	| *      	| *        	|

### Error 10103 - USER_TWO_STEP_VERIFICATION_CHECK_PASSWORD_BAD_PAYLOAD
Bad payload for request [#135](../proto/README.md#action_135)

| Minor Code 	| Detail                  	| Reaction 	|
|------------	|-------------------------	|----------	|
| 1          	| Password is not correct 	| *        	|

### Error 10104 - USER_TWO_STEP_VERIFICATION_CHECK_PASSWORD_INTERNAL_SERVER_ERROR
Internal server error for request [#135](../proto/README.md#action_135)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10105 - USER_TWO_STEP_VERIFICATION_CHECK_PASSWORD_INVALID_PASSWORD
Password is not correct for request [#135](../proto/README.md#action_135)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10106 - USER_TWO_STEP_VERIFICATION_CHECK_PASSWORD_MAX_TRY_LOCK
Password has been entered incorrectly too many times for request [#135](../proto/README.md#action_135)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10107 - USER_TWO_STEP_VERIFICATION_CHECK_PASSWORD_NO_PASSWORD
Password has not been set yet for request [#135](../proto/README.md#action_135)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| 1          	| *      	| *        	|

### Error 10108 - USER_TWO_STEP_VERIFICATION_VERIFY_RECOVERY_EMAIL_BAD_PAYLOAD
Bad payload for request [#136](../proto/README.md#action_136)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Token is incorrect 	| *        	|

### Error 10109 - USER_TWO_STEP_VERIFICATION_VERIFY_RECOVERY_EMAIL_INTERNAL_SERVER_ERROR
Internal server error for request [#136](../proto/README.md#action_136)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10110 - USER_TWO_STEP_VERIFICATION_VERIFY_RECOVERY_EMAIL_MAX_TRY_LOCK
The code to verify the recovery E-mail has been entered incorrectly too many times for request [#136](../proto/README.md#action_136)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10111 - USER_TWO_STEP_VERIFICATION_VERIFY_RECOVERY_EMAIL_EXPIRED_TOKEN
The code to verify and authenticate recovery E-mail has expired for request [#136](../proto/README.md#action_136)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10112 - USER_TWO_STEP_VERIFICATION_VERIFY_RECOVERY_EMAIL_NO_PASSWORD
Password has not been set yet for request [#136](../proto/README.md#action_136)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10113 - USER_TWO_STEP_VERIFICATION_VERIFY_RECOVERY_EMAIL_INVALID_TOKEN
The verification code you entered for E-mail recovery is incorrect for request [#136](../proto/README.md#action_136)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10114 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_EMAIL_BAD_PAYLOAD
Bad payload for request [#137](../proto/README.md#action_137)

| Minor Code 	| Detail                       	| Reaction 	|
|------------	|------------------------------	|----------	|
| 1          	| Password is incorrect        	| *        	|
| 2          	| Recovery E-mail is incorrect 	| *        	|
| 3          	| Recovery E-mail is incorrect 	| *        	|

### Error 10115 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_EMAIL_INTERNAL_SERVER_ERROR
Internal server error for request [#137](../proto/README.md#action_137)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10116 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_EMAIL_MAX_TRY_LOCK
The code to verify the recovery E-mail has been entered incorrectly too many times for request [#137](../proto/README.md#action_137)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10117 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_EMAIL_NO_PASSWORD
Password has not been set yet for request [#137](../proto/README.md#action_137)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10118 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_EMAIL_INVALID_PASSWORD
Password is incorrect for request [#137](../proto/README.md#action_137)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10119 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_EMAIL_CONFIRMED_BEFORE
Recovery E-mail has already been confirmed for request [#137](../proto/README.md#action_137)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10120 - USER_TWO_STEP_VERIFICATION_REQUEST_RECOVERY_TOKEN_BAD_PAYLOAD
Bad payload for request [#138](../proto/README.md#action_138)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10121 - USER_TWO_STEP_VERIFICATION_REQUEST_RECOVERY_TOKEN_INTERNAL_SERVER_ERROR
Internal server error for request [#138](../proto/README.md#action_138)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10122 - USER_TWO_STEP_VERIFICATION_REQUEST_RECOVERY_TOKEN_NO_PASSWORD
Password has not been set yet for request [#138](../proto/README.md#action_138)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10123 - USER_TWO_STEP_VERIFICATION_REQUEST_RECOVERY_TOKEN_NO_RECOVERY_EMAIL
No E-mail has been set to recover password for request [#138](../proto/README.md#action_138)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10124 - USER_TWO_STEP_VERIFICATION_REQUEST_RECOVERY_TOKEN_MAX_TRY_LOCK
Password recovery token has been entered incorrectly too many times for request [#138](../proto/README.md#action_138)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10154 - USER_TWO_STEP_VERIFICATION_REQUEST_RECOVERY_TOKEN_FORBIDDEN
You are forbidden to do the action for request [#138](../proto/README.md#action_138)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10125 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_TOKEN_BAD_PAYLOAD
Bad payload for request [#139](../proto/README.md#action_139)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Token is incorrect 	| *        	|

### Error 10126 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_TOKEN_INTERNAL_SERVER_ERROR
Internal server error for request [#139](../proto/README.md#action_139)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10127 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_TOKEN_MAX_TRY_LOCK
Password recovery token has been entered incorrectly too many times for request [#139](../proto/README.md#action_139)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10128 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_TOKEN_EXPIRED_TOKEN
Password recovery token has expired for request [#139](../proto/README.md#action_139)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10129 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_TOKEN_INVALID_TOKEN
Password recovery token is invalid for request [#139](../proto/README.md#action_139)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10130 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_TOKEN_NO_PASSWORD
Password has not been set yet for request [#139](../proto/README.md#action_139)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10155 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_TOKEN_FORBIDDEN
You are forbidden to do the action for request [#139](../proto/README.md#action_139)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10131 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_ANSWERS_BAD_PAYLOAD
Bad payload for request [#140](../proto/README.md#action_140)

| Minor Code 	| Detail                         	| Reaction 	|
|------------	|--------------------------------	|----------	|
| 1          	| The first answer is incorrect  	| *        	|
| 2          	| The second answer is incorrect 	| *        	|

### Error 10132 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_ANSWERS_INTERNAL_SERVER_ERROR
Internal server error for request [#140](../proto/README.md#action_140)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10133 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_ANSWERS_MAX_TRY_LOCK
Password has been entered incorrectly too many times for request [#140](../proto/README.md#action_140)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10134 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_ANSWERS_INVALID_ANSWERS
At least one of the answers is not valid for the request [#140](../proto/README.md#action_140)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10135 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_ANSWERS_NO_PASSWORD
Password has not been set yet for request [#140](../proto/README.md#action_140)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10156 - USER_TWO_STEP_VERIFICATION_RECOVER_PASSWORD_BY_ANSWERS_FORBIDDEN
You are forbidden to do the action for request [#140](../proto/README.md#action_140)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10136 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_QUESTION_BAD_PAYLOAD
Bad payload for request [#141](../proto/README.md#action_141)

| Minor Code 	| Detail                                     	| Reaction 	|
|------------	|--------------------------------------------	|----------	|
| 1          	| Password is incorrect                      	| *        	|
| 2          	| The first question is invalid              	| *        	|
| 3          	| Answer of the first question is incorrect  	| *        	|
| 4          	| The second question is invalid             	| *        	|
| 5          	| Answer of the second question is incorrect 	| *        	|

### Error 10137 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_QUESTION_INTERNAL_SERVER_ERROR
Internal server error for request [#141](../proto/README.md#action_141)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10138 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_QUESTION_MAX_TRY_LOCK
Password has been entered incorrectly too many times for request [#141](../proto/README.md#action_141)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10139 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_QUESTION_NO_PASSWORD
Password has not been set yet for request [#141](../proto/README.md#action_141)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10140 - USER_TWO_STEP_VERIFICATION_CHANGE_RECOVERY_QUESTION_INVALID_PASSWORD
Password is incorrect for request [#141](../proto/README.md#action_141)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10141 - USER_TWO_STEP_VERIFICATION_CHANGE_HINT_BAD_PAYLOAD
Bad payload for request [#142](../proto/README.md#action_142)

| Minor Code 	| Detail                   	| Reaction 	|
|------------	|--------------------------	|----------	|
| 1          	| Password is incorrect    	| *        	|
| 2          	| Password hint is invalid 	| *        	|

### Error 10142 - USER_TWO_STEP_VERIFICATION_CHANGE_HINT_INTERNAL_SERVER_ERROR
Internal server error for request [#142](../proto/README.md#action_142)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### :triangular_flag_on_post: :one: Error 10143 - USER_TWO_STEP_VERIFICATION_CHANGE_HINT_MAX_TRY_LOCK
Password has been entered incorrectly too many times for request [#142](../proto/README.md#action_142)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10144 - USER_TWO_STEP_VERIFICATION_CHANGE_HINT_NO_PASSWORD
Password has not been set yet for request [#142](../proto/README.md#action_142)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10145 - USER_TWO_STEP_VERIFICATION_CHANGE_HINT_INVALID_PASSWORD
Password is incorrect for request [#142](../proto/README.md#action_142)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10157 - USER_TWO_STEP_VERIFICATION_RESEND_VERIFY_EMAIL_BAD_PAYLOAD
Bad payload for request [#146](../proto/README.md#action_146)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10158 - USER_TWO_STEP_VERIFICATION_RESEND_VERIFY_EMAIL_INTERNAL_SERVER_ERROR
Internal server error for request [#146](../proto/README.md#action_146)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10159 - USER_TWO_STEP_VERIFICATION_RESEND_VERIFY_EMAIL_NO_PASSWORD
Password has not been set yet for request [#146](../proto/README.md#action_146)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10160 - USER_TWO_STEP_VERIFICATION_RESEND_VERIFY_EMAIL_NO_UNCONFIRMED_RECOVERY_EMAIL
There is no confirmed E-mail to be sent the verification token for request [#146](../proto/README.md#action_146)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10146 - USER_PRIVACY_GET_RULE_BAD_PAYLOAD
Bad payload for request [#143](../proto/README.md#action_143)

| Minor Code 	| Detail        	| Reaction 	|
|------------	|---------------	|----------	|
| 1          	| Type is wrong 	| *        	|

### Error 10147 - USER_PRIVACY_GET_RULE_INTERNAL_SERVER_ERROR
Internal server error for request [#143](../proto/README.md#action_143)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10148 - USER_PRIVACY_SET_RULE_BAD_PAYLOAD
Bad payload for request [#144](../proto/README.md#action_144)

| Minor Code 	| Detail         	| Reaction 	|
|------------	|----------------	|----------	|
| 1          	| Type is wrong  	| *        	|
| 2          	| Level is wrong 	| *        	|

### Error 10149 - USER_PRIVACY_SET_RULE_INTERNAL_SERVER_ERROR
Internal server error for request [#144](../proto/README.md#action_144)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10150 - USER_VERIFY_NEW_DEVICE_BAD_PAYLOAD
Bad payload for request [#145](../proto/README.md#action_145)

| Minor Code 	| Detail           	| Reaction 	|
|------------	|------------------	|----------	|
| 1          	| Token is invalid 	| *        	|

### Error 10151 - USER_VERIFY_NEW_DEVICE_INTERNAL_SERVER_ERROR
Internal server error for request [#145](../proto/README.md#action_145)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10152 - USER_VERIFY_NEW_DEVICE_INVALID_TOKEN
Token is invalid for request [#145](../proto/README.md#action_145)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 10153 - USER_VERIFY_NEW_DEVICE_EXPIRED_TOKEN
Token has expired for request [#145](../proto/README.md#action_145)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 10161 - USER_PROFILE_SET_BIO_BAD_PAYLOAD
Bad payload for request [#147](../proto/README.md#action_147)

| Minor Code 	| Detail         	| Reaction 	|
|------------	|----------------	|----------	|
| 1          	| Bio is invalid 	| *        	|


### Error 10162 - USER_PROFILE_SET_BIO_INTERNAL_SERVER_ERROR
Internal server error for request [#147](../proto/README.md#action_147)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 10163 - USER_PROFILE_GET_BIO_BAD_PAYLOAD
Bad payload for request [#148](../proto/README.md#action_148)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 10164 - USER_PROFILE_GET_BIO_INTERNAL_SERVER_ERROR
Internal server error for request [#148](../proto/README.md#action_148)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 10165 - USER_REPORT_BAD_PAYLOAD
Bad payload for request [#149](../proto/README.md#action_149)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| User_ID is invalid     	| *        	|
| 2          	| Reason is invalid      	| *        	|
| 3          	| Description is invalid 	| *        	|


### Error 10166 - USER_REPORT_INTERNAL_SERVER_ERROR
Internal server error for request [#149](../proto/README.md#action_149)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 10167 - USER_REPORT_REPORTED_BEFORE
You have already reported this user for request [#149](../proto/README.md#action_149)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 10168 - USER_REPORT_FORBIDDEN
You are forbidden to do the action for request [#149](../proto/README.md#action_149)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 10173 - USER_SET_BOT_BAD_PAYLOAD
Bad payload for request [#150](../proto/README.md#action_150)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| status is invalid     	| *        	|


### Error 10174 - USER_SET_BOT_INTERNAL_SERVER_ERROR
Internal server error for request [#150](../proto/README.md#action_150)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# Chat Errors(2xx)
### Error 200 - CHAT_GET_ROOM_BAD_PAYLOAD
Bad payload for request [#200](../proto/README.md#action_200)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Peer_ID is invalid 	| *        	|


### Error 201 - CHAT_GET_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#200](../proto/README.md#action_200)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 202 - CHAT_GET_ROOM_PEER_NOT_FOUND
There is no active user with the given peer_ID for request [#200](../proto/README.md#action_200)

| Minor Code 	| Detail                         	| Reaction 	|
|------------	|--------------------------------	|----------	|
| 1          	| *                              	| *        	|
| 2          	| *                              	| *        	|
| 3          	| Peer's account has got blocked 	| *        	|


### Error 203 - CHAT_SEND_MESSAGE_BAD_PAYLOAD
Bad payload for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail                                	| Reaction 	|
|------------	|---------------------------------------	|----------	|
| 1          	| Room_ID is invalid                    	| *        	|
| 2          	| Message is invalid                    	| *        	|
| 3          	| Attachment is invalid                 	| *        	|
| 4          	| Attachment is invalid                 	| *        	|
| 5          	| Attachment is invalid                 	| *        	|
| 6          	| Attachment is invalid                 	| *        	|
| 7          	| Attachment is invalid                 	| *        	|
| 8          	| Attachment is invalid                 	| *        	|
| 9          	| Message is invalid                    	| *        	|
| 10         	| Attachment is invalid                 	| *        	|
| 11         	| Message is invalid                    	| *        	|
| 12         	| Attachment is invalid                 	| *        	|
| 13         	| Message is invalid                    	| *        	|
| 14         	| Attachment is invalid                 	| *        	|
| 15         	| Message is invalid                    	| *        	|
| 16         	| Attachment is invalid                 	| *        	|
| 17         	| Location is invalid                   	| *        	|
| 18         	| Location.lat is invalid               	| *        	|
| 19         	| Location.lon is invalid               	| *        	|
| 22         	| Contact is invalid                    	| *        	|
| 23         	| Message_Type is invalid               	| *        	|
| 24         	| No such file is found                 	| *        	|
| 25         	| ReplyTo is invalid                    	| *        	|
| 26         	| ForwardFrom.Room_ID is invalid        	| *        	|
| 27         	| ForwardFrom.Message_ID is invalid     	| *        	|
| 28         	| ForwardFrom is invalid                	| *        	|
| 29         	| ReplyTo and ForwardFrom have been set 	| *        	|
| 30         	| Message is invalid                    	| *        	|
| 31         	| Attachment is invalid                 	| *        	|
| 32         	| **Message is too long**               	| *        	|
| 33         	| Random id is invalid                    	| *        	|

### Error 204 - CHAT_SEND_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 205 - CHAT_SEND_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 233 - CHAT_SEND_MESSAGE_BLOCKED_BY_PEER
You have got blocked by the peer for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### :triangular_flag_on_post: :one: Error 234 - CHAT_SEND_MESSAGE_LIMIT_REACHED
You are not currently allowed to send message to the required recipient for the restriction made; ask her/him to add you in the contact list first or keep waiting to remove restriction for request [#201](../proto/README.md#action_201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 206 - CHAT_UPDATE_STATUS_BAD_PAYLOAD
Bad payload for request [#202](../proto/README.md#action_202)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|


### Error 207 - CHAT_UPDATE_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#202](../proto/README.md#action_202)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 208 - CHAT_UPDATE_STATUS_FORBIDDEN
You are forbidden to do the action for request [#202](../proto/README.md#action_202)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 209 - CHAT_EDIT_MESSAGE_BAD_PAYLOAD
Bad payload for request [#203](../proto/README.md#action_203)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| Message is invalid    	| *        	|


### Error 210 - CHAT_EDIT_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#203](../proto/README.md#action_203)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 211 - CHAT_EDIT_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#203](../proto/README.md#action_203)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 212 - CHAT_DELETE_MESSAGE_BAD_PAYLOAD
Bad payload for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| Both are invalid 			| *        	|


### Error 213 - CHAT_DELETE_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 214 - CHAT_DELETE_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#204](../proto/README.md#action_204)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 215 - CHAT_CLEAR_MESSAGE_BAD_PAYLOAD
Bad payload for request [#205](../proto/README.md#action_205)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Room_ID is invalid  	| *        	|
| 2          	| Clear_ID is invalid 	| *        	|



### Error 216 - CHAT_CLEAR_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#205](../proto/README.md#action_205)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 217 - CHAT_CLEAR_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#205](../proto/README.md#action_205)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 218 - CHAT_DELETE_BAD_PAYLOAD
Bad payload for request [#206](../proto/README.md#action_206)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Room_ID is invalid  	| *        	|


### Error 219 - CHAT_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#206](../proto/README.md#action_206)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 220 - CHAT_DELETE_FORBIDDEN
You are forbidden to do the action for request [#206](../proto/README.md#action_206)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 221 - CHAT_UPDATE_DRAFT_BAD_PAYLOAD
Bad payload for request [#207](../proto/README.md#action_207)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| ReplyTo is invalid    	| *        	|


### Error 222 - CHAT_UPDATE_DRAFT_INTERNAL_SERVER_ERROR
Internal server error for request [#207](../proto/README.md#action_207)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 223 - CHAT_UPDATE_DRAFT_FORBIDDEN
You are forbidden to do the action for request [#207](../proto/README.md#action_207)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 224 - CHAT_GET_DRAFT_BAD_PAYLOAD
Bad payload for request [#208](../proto/README.md#action_208)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 225 - CHAT_GET_DRAFT_INTERNAL_SERVER_ERROR
Internal server error for request [#208](../proto/README.md#action_208)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 226 - CHAT_GET_DRAFT_FORBIDDEN
You are forbidden to do the action for request [#208](../proto/README.md#action_208)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 227 - CHAT_CONVERT_TO_GROUP_BAD_PAYLOAD
Bad payload for request [#209](../proto/README.md#action_209)

| Minor Code 	| Detail                         	| Reaction 	|
|------------	|--------------------------------	|----------	|
| 1          	| Room_ID is invalid             	| *        	|
| 2          	| Group Name is not valid        	| *        	|
| 3          	| Group Description is not valid 	| *        	|


### Error 228 - CHAT_CONVERT_TO_GROUP_INTERNAL_SERVER_ERROR
Internal server error for request [#209](../proto/README.md#action_209)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 229 - CHAT_CONVERT_TO_GROUP_FORBIDDEN
You are forbidden to do the action for request [#209](../proto/README.md#action_209)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 230 - CHAT_SET_ACTION_BAD_PAYLOAD
Bad payload for request [#210](../proto/README.md#action_210)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| Room_ID is invalid     	| *        	|
| 2          	| Action is wrong        	| *        	|
| 3          	| Action_ID is not valid 	| *        	|


### Error 231 - CHAT_SET_ACTION_INTERNAL_SERVER_ERROR
Internal server error for request [#210](../proto/README.md#action_210)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 232 - CHAT_SET_ACTION_FORBIDDEN
You are forbidden to do the action for request [#210](../proto/README.md#action_210)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# Group Errors(3xx)
### Error 300 - GROUP_CREATE_BAD_PAYLOAD
Bad payload for request [#300](../proto/README.md#action_300)

| Minor Code 	| Detail                         	| Reaction 	|
|------------	|--------------------------------	|----------	|
| 1          	| Room_Name for Group is invalid 	| *        	|
| 2          	| Group Description is invalid   	| *        	|


### Error 301 - GROUP_CREATE_INTERNAL_SERVER_ERROR
Internal server error for request [#300](../proto/README.md#action_300)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 380 - GROUP_CREATE_LIMIT_REACHED
You are restricted to create more rooms for the request [#300](../proto/README.md#action_300)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 302 - GROUP_ADD_MEMBER_BAD_PAYLOAD
Bad payload for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail                     	| Reaction 	|
|------------	|----------------------------	|----------	|
| 1          	| Room_ID is invalid         	| *        	|
| 2          	| User_ID is invalid         	| *        	|
| 3          	| StartMessage_ID is invalid 	| *        	|


### Error 303 - GROUP_ADD_MEMBER_INTERNAL_SERVER_ERROR
Internal server error for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 304 - GROUP_ADD_MEMBER_EXISTS
This user has already joined this room for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 305 - GROUP_ADD_MEMBER_FORBIDDEN
You are forbidden to do the action for request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 362 - GROUP_ADD_MEMBER_PARTICIPANTS_COUNT_LIMIT_EXCEEDED
No more member can join this room for the request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 379 - GROUP_ADD_MEMBER_PRIVACY_PROTECTION
You cannot invite this user to groups because of the protected privacy for the request [#301](../proto/README.md#action_301)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 306 - GROUP_SEND_MESSAGE_BAD_PAYLOAD
Bad payload for request [#310](../proto/README.md#action_310)

| Minor Code 	| Detail                                	| Reaction 	|
|------------	|---------------------------------------	|----------	|
| 1          	| Room_ID is invalid                    	| *        	|
| 2          	| Message is invalid                    	| *        	|
| 3          	| Attachment is invalid                 	| *        	|
| 4          	| Attachment is invalid                 	| *        	|
| 5          	| Attachment is invalid                 	| *        	|
| 6          	| Attachment is invalid                 	| *        	|
| 7          	| Attachment is invalid                 	| *        	|
| 8          	| Attachment is invalid                 	| *        	|
| 9          	| Message is invalid                    	| *        	|
| 10         	| Attachment is invalid                 	| *        	|
| 11         	| Message is invalid                    	| *        	|
| 12         	| Attachment is invalid                 	| *        	|
| 13         	| Message is invalid                    	| *        	|
| 14         	| Attachment is invalid                 	| *        	|
| 15         	| Message is invalid                    	| *        	|
| 16         	| Attachment is invalid                 	| *        	|
| 17         	| Location is invalid                   	| *        	|
| 18         	| Location.lat is invalid               	| *        	|
| 19         	| Location.lon is invalid               	| *        	|
| 22         	| Contact is invalid                    	| *        	|
| 23         	| Message_Type is invalid               	| *        	|
| 24         	| No such file is found                 	| *        	|
| 25         	| ReplyTo is invalid                    	| *        	|
| 26         	| ForwardFrom.Room_ID is invalid        	| *        	|
| 27         	| ForwardFrom.Message_ID is invalid     	| *        	|
| 28         	| ForwardFrom is invalid                	| *        	|
| 29         	| ReplyTo and ForwardFrom have been set 	| *        	|
| 30         	| Message is invalid                    	| *        	|
| 31         	| Attachment is invalid                 	| *        	|
| 32         	| **Message is too long**               	| *        	|
| 33         	| Random id is invalid                    	| *        	|


### Error 307 - GROUP_SEND_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#310](../proto/README.md#action_310)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 308 - GROUP_SEND_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#310](../proto/README.md#action_310)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 309 - GROUP_UPDATE_STATUS_BAD_PAYLOAD
Bad payload for request [#311](../proto/README.md#action_311)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| Status is invalid     	| *        	|


### Error 310 - GROUP_UPDATE_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#311](../proto/README.md#action_311)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 311 - GROUP_UPDATE_STATUS_FORBIDDEN
You are forbidden to do the action for request [#311](../proto/README.md#action_311)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 312 - GROUP_DELETE_MESSAGE_BAD_PAYLOAD
Bad payload for request [#320](../proto/README.md#action_320)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|


### Error 313 - GROUP_DELETE_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#320](../proto/README.md#action_320)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 314 - GROUP_DELETE_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#320](../proto/README.md#action_320)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 315 - GROUP_CLEAR_MESSAGE_BAD_PAYLOAD
Bad payload for request [#304](../proto/README.md#action_304)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Room_ID is invalid  	| *        	|
| 2          	| Clear_ID is invalid 	| *        	|


### Error 316 - GROUP_CLEAR_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#304](../proto/README.md#action_304)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 317 - GROUP_CLEAR_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#304](../proto/README.md#action_304)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 318 - GROUP_ADD_MODERATOR_BAD_PAYLOAD
Bad payload for request [#303](../proto/README.md#action_303)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 319 - GROUP_ADD_MODERATOR_INTERNAL_SERVER_ERROR
Internal server error for request [#303](../proto/README.md#action_303)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 320 - GROUP_ADD_MODERATOR_FORBIDDEN
You are forbidden to do the action for request [#303](../proto/README.md#action_303)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 321 - GROUP_ADD_ADMIN_BAD_PAYLOAD
Bad payload in for request [#302](../proto/README.md#action_302)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 322 - GROUP_ADD_ADMIN_INTERNAL_SERVER_ERROR
Internal server error for request [#302](../proto/README.md#action_302)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 323 - GROUP_ADD_ADMIN_FORBIDDEN
You are forbidden to do the action for request [#302](../proto/README.md#action_302)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 324 - GROUP_KICK_MODERATOR_BAD_PAYLOAD
Bad payload for request [#308](../proto/README.md#action_308)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 325 - GROUP_KICK_MODERATOR_INTERNAL_SERVER_ERROR
Internal server error for request [#308](../proto/README.md#action_308)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 326 - GROUP_KICK_MODERATOR_FORBIDDEN
You are forbidden to do the action for request [#308](../proto/README.md#action_308)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 327 - GROUP_KICK_ADMIN_BAD_PAYLOAD
Bad payload for request [#306](../proto/README.md#action_306)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 328 - GROUP_KICK_ADMIN_INTERNAL_SERVER_ERROR
Internal server error for request [#306](../proto/README.md#action_306)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 329 - GROUP_KICK_ADMIN_FORBIDDEN
You are forbidden to do the action for request [#306](../proto/README.md#action_306)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 330 - GROUP_EDIT_BAD_PAYLOAD
Bad payload for request [#305](../proto/README.md#action_305)

| Minor Code 	| Detail                       	| Reaction 	|
|------------	|------------------------------	|----------	|
| 1          	| Room_ID is invalid           	| *        	|
| 2          	| Group Name is invalid        	| *        	|
| 3          	| Group Description is invalid 	| *        	|


### Error 331 - GROUP_EDIT_INTERNAL_SERVER_ERROR
Internal server error for request [#305](../proto/README.md#action_305)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 363 - GROUP_EDIT_FORBIDDEN
You are forbidden to do the action for request [#305](../proto/README.md#action_305)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 332 - GROUP_KICK_MEMBER_BAD_PAYLOAD
Bad payload for request [#307](../proto/README.md#action_307)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 333 - GROUP_KICK_MEMBER_INTERNAL_SERVER_ERROR
Internal server error for request [#307](../proto/README.md#action_307)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 334 - GROUP_KICK_MEMBER_FORBIDDEN
You are forbidden to do the action for request [#307](../proto/README.md#action_307)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 335 - GROUP_LEFT_BAD_PAYLOAD
Bad payload for request [#309](../proto/README.md#action_309)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Room_ID is invalid 	| *        	|


### Error 336 - GROUP_LEFT_INTERNAL_SERVER_ERROR
Internal server error for request [#309](../proto/README.md#action_309)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 337 - GROUP_LEFT_FORBIDDEN
You are forbidden to do the action for request [#309](../proto/README.md#action_309)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 338 - GROUP_AVATAR_ADD_BAD_PAYLOAD
Bad payload for request [#312](../proto/README.md#action_312)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Attachment is invalid 	| *        	|
| 2          	| Room_ID is invalid    	| *        	|


### Error 339 - GROUP_AVATAR_ADD_INTERNAL_SERVER_ERROR
Internal server error for request [#312](../proto/README.md#action_312)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 340 - GROUP_AVATAR_ADD_FORBIDDEN
You are forbidden to do the action for request [#312](../proto/README.md#action_312)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 341 - GROUP_AVATAR_DELETE_BAD_PAYLOAD
Bad payload for request [#313](../proto/README.md#action_313)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Avatar_ID is invalid 	| *        	|
| 2          	| Room_ID is invalid   	| *        	|


### Error 342 - GROUP_AVATAR_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#313](../proto/README.md#action_313)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 343 - GROUP_AVATAR_DELETE_FORBIDDEN
You are forbidden to do the action for request [#313](../proto/README.md#action_313)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 344 - GROUP_AVATAR_GET_LIST_BAD_PAYLOAD
Bad payload for request [#314](../proto/README.md#action_314)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 345 - GROUP_AVATAR_GET_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#314](../proto/README.md#action_314)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 346 - GROUP_AVATAR_GET_LIST_FORBIDDEN
You are forbidden to do the action for request [#314](../proto/README.md#action_314)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 347 - GROUP_UPDATE_DRAFT_BAD_PAYLOAD
Bad payload for request [#315](../proto/README.md#action_315)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| ReplyTo is invalid    	| *        	|


### Error 348 - GROUP_UPDATE_DRAFT_INTERNAL_SERVER_ERROR
Internal server error for request [#315](../proto/README.md#action_315)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 349 - GROUP_UPDATE_DRAFT_FORBIDDEN
You are forbidden to do the action for request [#315](../proto/README.md#action_315)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 350 - GROUP_GET_DRAFT_BAD_PAYLOAD
Bad payload for request [#316](../proto/README.md#action_316)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 351 - GROUP_GET_DRAFT_INTERNAL_SERVER_ERROR
Internal server error for request [#316](../proto/README.md#action_316)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 352 - GROUP_GET_DRAFT_FORBIDDEN
You are forbidden to do the action for request [#316](../proto/README.md#action_316)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 353 - GROUP_GET_MEMBER_LIST_BAD_PAYLOAD
Bad payload for request [#317](../proto/README.md#action_317)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| FilterRole is invalid 	| *        	|
| 3          	| OffSet is invalid     	| *        	|
| 4          	| Limit is invalid      	|          	|


### Error 354 - GROUP_GET_MEMBER_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#317](../proto/README.md#action_317)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 355 - GROUP_GET_MEMBER_LIST_FORBIDDEN
You are forbidden to do the action for request [#317](../proto/README.md#action_317)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 356 - GROUP_DELETE_BAD_PAYLOAD
Bad payload for request [#318](../proto/README.md#action_318)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 357 - GROUP_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#318](../proto/README.md#action_318)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 358 - GROUP_DELETE_FORBIDDEN
You are forbidden to do the action for request [#318](../proto/README.md#action_318)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 359 - GROUP_SET_ACTION_BAD_PAYLOAD
Bad payload for request [#319](../proto/README.md#action_319)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| Room_ID is invalid     	| *        	|
| 2          	| Action is wrong        	| *        	|
| 3          	| Action_ID is not valid 	| *        	|


### Error 360 - GROUP_SET_ACTION_INTERNAL_SERVER_ERROR
Internal server error for request [#319](../proto/README.md#action_319)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 361 - GROUP_SET_ACTION_FORBIDDEN
You are forbidden to do the action for request [#319](../proto/README.md#action_319)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 364 - GROUP_CHECK_USERNAME_BAD_PAYLOAD
Bad payload for request [#321](../proto/README.md#action_321)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 365 - GROUP_CHECK_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#321](../proto/README.md#action_321)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 366 - GROUP_UPDATE_USERNAME_BAD_PAYLOAD
Bad payload for request [#322](../proto/README.md#action_322)

| Minor Code 	| Detail                                                 	    | Reaction 	|
|------------	|--------------------------------------------------------	    |----------	|
| 1          	| Room_ID is invalid                                     	    | *        	|
| 2          	| Username is invalid                                    	    | *        	|
| 3          	| This username has already been taken by another user   	    | *        	|
| 4          	| More than the allowed usernames have been selected by you  	| *        	|


### Error 367 - GROUP_UPDATE_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#322](../proto/README.md#action_322)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### :triangular_flag_on_post: :one: Error 368 - GROUP_UPDATE_USERNAME_UPDATE_LOCK
Username has been changed recently, to renew it wait until the allowed time or choose the last one again for the request [#322](../proto/README.md#action_322)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 369 - GROUP_UPDATE_USERNAME_FORBIDDEN
You are forbidden to do the action for request [#322](../proto/README.md#action_322)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 370 - GROUP_REMOVE_USERNAME_BAD_PAYLOAD
Bad payload for request [#323](../proto/README.md#action_323)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 371 - GROUP_REMOVE_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#323](../proto/README.md#action_323)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 372 - GROUP_REMOVE_USERNAME_FORBIDDEN
You are forbidden to do the action for request [#323](../proto/README.md#action_323)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 373 - GROUP_REVOKE_LINK_BAD_PAYLOAD
Bad payload for request [#324](../proto/README.md#action_324)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 374 - GROUP_REVOKE_LINK_INTERNAL_SERVER_ERROR
Internal server error for request [#324](../proto/README.md#action_324)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 375 - GROUP_REVOKE_LINK_FORBIDDEN
You are forbidden to do the action for request [#324](../proto/README.md#action_324)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 376 - GROUP_EDIT_MESSAGE_BAD_PAYLOAD
Bad payload for request [#325](../proto/README.md#action_325)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| Message is invalid    	| *        	|


### Error 377 - GROUP_EDIT_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#325](../proto/README.md#action_325)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 378 - GROUP_EDIT_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#325](../proto/README.md#action_325)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 381 - GROUP_PIN_MESSAGE_BAD_PAYLOAD
Bad payload for request [#326](../proto/README.md#action_326)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|


### Error 382 - GROUP_PIN_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#326](../proto/README.md#action_326)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 383 - GROUP_PIN_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#326](../proto/README.md#action_326)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# Channel Errors(4xx)

### Error 400 - CHANNEL_CREATE_BAD_PAYLOAD
Bad payload for request [#400](../proto/README.md#action_400)

| Minor Code 	| Detail                         	| Reaction 	|
|------------	|--------------------------------	|----------	|
| 1          	| Room_Name for Channel is invalid 	| *        	|
| 2          	| Channel Description is invalid   	| *        	|


### Error 401 - CHANNEL_CREATE_INTERNAL_SERVER_ERROR
Internal server error for request [#400](../proto/README.md#action_400)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 479 - CHANNEL_CREATE_LIMIT_REACHED
You are restricted to create more rooms for the request [#400](../proto/README.md#action_400)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 402 - CHANNEL_ADD_MEMBER_BAD_PAYLOAD
Bad payload for request [#401](../proto/README.md#action_401)

| Minor Code 	| Detail                    	| Reaction 	|
|------------	|---------------------------	|----------	|
| 1          	| Room_ID is invalid        	| *        	|
| 2          	| User_ID_Member is invalid 	| *        	|


### Error 403 - CHANNEL_ADD_MEMBER_INTERNAL_SERVER_ERROR
Internal server error for request [#401](../proto/README.md#action_401)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 404 - CHANNEL_ADD_MEMBER_EXISTS
This user has already joined this room for request [#401](../proto/README.md#action_401)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 405 - CHANNEL_ADD_MEMBER_FORBIDDEN
You are forbidden to do the action for request [#401](../proto/README.md#action_401)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 478 - CHANNEL_ADD_MEMBER_PRIVACY_PROTECTION
You cannot invite this user to groups because of the protected privacy for the request [#401](../proto/README.md#action_401)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 406 - CHANNEL_SEND_MESSAGE_BAD_PAYLOAD
Bad payload for request [#410](../proto/README.md#action_410)

| Minor Code 	| Detail                                	| Reaction 	|
|------------	|---------------------------------------	|----------	|
| 1          	| Room_ID is invalid                    	| *        	|
| 2          	| Message is invalid                    	| *        	|
| 3          	| Attachment is invalid                 	| *        	|
| 4          	| Attachment is invalid                 	| *        	|
| 5          	| Attachment is invalid                 	| *        	|
| 6          	| Attachment is invalid                 	| *        	|
| 7          	| Attachment is invalid                 	| *        	|
| 8          	| Attachment is invalid                 	| *        	|
| 9          	| Message is invalid                    	| *        	|
| 10         	| Attachment is invalid                 	| *        	|
| 11         	| Message is invalid                    	| *        	|
| 12         	| Attachment is invalid                 	| *        	|
| 13         	| Message is invalid                    	| *        	|
| 14         	| Attachment is invalid                 	| *        	|
| 15         	| Message is invalid                    	| *        	|
| 16         	| Attachment is invalid                 	| *        	|
| 17         	| Location is invalid                   	| *        	|
| 18         	| Location.lat is invalid               	| *        	|
| 19         	| Location.lon is invalid               	| *        	|
| 22         	| Contact is invalid                    	| *        	|
| 23         	| Message_Type is invalid               	| *        	|
| 24         	| No such file is found                 	| *        	|
| 25         	| ReplyTo is invalid                    	| *        	|
| 26         	| ForwardFrom.Room_ID is invalid        	| *        	|
| 27         	| ForwardFrom.Message_ID is invalid     	| *        	|
| 28         	| ForwardFrom is invalid                	| *        	|
| 29         	| ReplyTo and ForwardFrom have been set 	| *        	|
| 30         	| Message is invalid                    	| *        	|
| 31         	| Attachment is invalid                 	| *        	|
| 32         	| **Message is too long**               	| *        	|
| 33         	| Random id is invalid                    	| *        	|


### Error 407 - CHANNEL_SEND_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#410](../proto/README.md#action_410)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 408 - CHANNEL_SEND_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#410](../proto/README.md#action_410)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 409 - CHANNEL_DELETE_BAD_PAYLOAD
Bad payload for request [#404](../proto/README.md#action_404)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 410 - CHANNEL_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#404](../proto/README.md#action_404)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 411 - CHANNEL_DELETE_FORBIDDEN
You are forbidden to do the action for request [#404](../proto/README.md#action_404)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 412 - CHANNEL_DELETE_MESSAGE_BAD_PAYLOAD
Bad payload for request [#411](../proto/README.md#action_411)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|


### Error 413 - CHANNEL_DELETE_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#411](../proto/README.md#action_411)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 414 - CHANNEL_DELETE_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#411](../proto/README.md#action_411)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 415 - CHANNEL_GET_MEMBER_LIST_BAD_PAYLOAD
Bad payload for request [#417](../proto/README.md#action_417)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| FilterRole is invalid 	| *        	|
| 3          	| OffSet is invalid     	| *        	|
| 4          	| Limit is invalid      	|          	|


### Error 416 - CHANNEL_GET_MEMBER_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#417](../proto/README.md#action_417)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 417 - CHANNEL_GET_MEMBER_LIST_FORBIDDEN
You are forbidden to do the action for request [#417](../proto/README.md#action_417)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 418 - CHANNEL_ADD_MODERATOR_BAD_PAYLOAD
Bad payload for request [#403](../proto/README.md#action_403)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 419 - CHANNEL_ADD_MODERATOR_INTERNAL_SERVER_ERROR
Internal server error for request [#403](../proto/README.md#action_403)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 420 - CHANNEL_ADD_MODERATOR_FORBIDDEN
You are forbidden to do the action for request [#403](../proto/README.md#action_403)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 421 - CHANNEL_ADD_ADMIN_BAD_PAYLOAD
Bad payload in for request [#402](../proto/README.md#action_402)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 422 - CHANNEL_ADD_ADMIN_INTERNAL_SERVER_ERROR
Internal server error for request [#402](../proto/README.md#action_402)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 423 - CHANNEL_ADD_ADMIN_FORBIDDEN
You are forbidden to do the action for request [#402](../proto/README.md#action_402)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 424 - CHANNEL_KICK_MODERATOR_BAD_PAYLOAD
Bad payload for request [#408](../proto/README.md#action_408)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 425 - CHANNEL_KICK_MODERATOR_INTERNAL_SERVER_ERROR
Internal server error for request [#408](../proto/README.md#action_408)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 426 - CHANNEL_KICK_MODERATOR_FORBIDDEN
You are forbidden to do the action for request [#408](../proto/README.md#action_408)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 427 - CHANNEL_KICK_ADMIN_BAD_PAYLOAD
Bad payload for request [#406](../proto/README.md#action_406)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 428 - CHANNEL_KICK_ADMIN_INTERNAL_SERVER_ERROR
Internal server error for request [#406](../proto/README.md#action_406)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 429 - CHANNEL_KICK_ADMIN_FORBIDDEN
You are forbidden to do the action for request [#406](../proto/README.md#action_406)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 430 - CHANNEL_EDIT_BAD_PAYLOAD
Bad payload for request [#405](../proto/README.md#action_405)

| Minor Code 	| Detail                      	 		| Reaction 	|
|------------	|------------------------------			|----------	|
| 1          	| Room_ID is invalid       	    		| *        	|
| 2          	| Channel Name is invalid     	   		| *        	|
| 3          	| Channel Description is invalid 		| *        	|


### Error 431 - CHANNEL_EDIT_INTERNAL_SERVER_ERROR
Internal server error for request [#405](../proto/README.md#action_405)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 459 - CHANNEL_EDIT_FORBIDDEN
You are forbidden to do the action for request [#405](../proto/README.md#action_405)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 432 - CHANNEL_KICK_MEMBER_BAD_PAYLOAD
Bad payload for request [#407](../proto/README.md#action_407)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Member_ID is invalid 	| *        	|


### Error 433 - CHANNEL_KICK_MEMBER_INTERNAL_SERVER_ERROR
Internal server error for request [#407](../proto/README.md#action_407)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 434 - CHANNEL_KICK_MEMBER_FORBIDDEN
You are forbidden to do the action for request [#407](../proto/README.md#action_407)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 435 - CHANNEL_LEFT_BAD_PAYLOAD
Bad payload for request [#409](../proto/README.md#action_409)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Room_ID is invalid 	| *        	|


### Error 436 - CHANNEL_LEFT_INTERNAL_SERVER_ERROR
Internal server error for request [#409](../proto/README.md#action_409)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 437 - CHANNEL_LEFT_FORBIDDEN
You are forbidden to do the action for request [#409](../proto/README.md#action_409)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 438 - CHANNEL_AVATAR_ADD_BAD_PAYLOAD
Bad payload for request [#412](../proto/README.md#action_412)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Attachment is invalid 	| *        	|
| 2          	| Room_ID is invalid    	| *        	|


### Error 439 - CHANNEL_AVATAR_ADD_INTERNAL_SERVER_ERROR
Internal server error for request [#412](../proto/README.md#action_412)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 440 - CHANNEL_AVATAR_ADD_FORBIDDEN
You are forbidden to do the action for request [#412](../proto/README.md#action_412)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 441 - CHANNEL_AVATAR_DELETE_BAD_PAYLOAD
Bad payload for request [#413](../proto/README.md#action_413)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Avatar_ID is invalid 	| *        	|
| 2          	| Room_ID is invalid   	| *        	|


### Error 442 - CHANNEL_AVATAR_DELETE_INTERNAL_SERVER_ERROR
Internal server error for request [#413](../proto/README.md#action_413)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 443 - CHANNEL_AVATAR_DELETE_FORBIDDEN
You are forbidden to do the action for request [#413](../proto/README.md#action_413)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 444 - CHANNEL_AVATAR_GET_LIST_BAD_PAYLOAD
Bad payload for request [#414](../proto/README.md#action_414)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 445 - CHANNEL_AVATAR_GET_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#414](../proto/README.md#action_414)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 446 - CHANNEL_AVATAR_GET_LIST_FORBIDDEN
You are forbidden to do the action for request [#414](../proto/README.md#action_414)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 447 - CHANNEL_UPDATE_DRAFT_BAD_PAYLOAD
Bad payload for request [#415](../proto/README.md#action_415)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| ReplyTo is invalid    	| *        	|


### Error 448 - CHANNEL_UPDATE_DRAFT_INTERNAL_SERVER_ERROR
Internal server error for request [#415](../proto/README.md#action_415)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 449 - CHANNEL_UPDATE_DRAFT_FORBIDDEN
You are forbidden to do the action for request [#415](../proto/README.md#action_415)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 450 - CHANNEL_GET_DRAFT_BAD_PAYLOAD
Bad payload for request [#416](../proto/README.md#action_416)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 451 - CHANNEL_GET_DRAFT_INTERNAL_SERVER_ERROR
Internal server error for request [#416](../proto/README.md#action_416)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 452 - CHANNEL_GET_DRAFT_FORBIDDEN
You are forbidden to do the action for request [#416](../proto/README.md#action_416)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 453 - CHANNEL_CHECK_USERNAME_BAD_PAYLOAD
Bad payload for request [#418](../proto/README.md#action_418)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 454 - CHANNEL_CHECK_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#418](../proto/README.md#action_418)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 455 - CHANNEL_UPDATE_USERNAME_BAD_PAYLOAD
Bad payload for request [#419](../proto/README.md#action_419)

| Minor Code 	| Detail                                                 	    | Reaction 	|
|------------	|--------------------------------------------------------	    |----------	|
| 1          	| Room_ID is invalid                                     	    | *        	|
| 2          	| Username is invalid                                    	    | *        	|
| 3          	| This username has already been taken by another user   	    | *        	|
| 4          	| More than the allowed usernames have been selected by you  	| *        	|


### Error 456 - CHANNEL_UPDATE_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#419](../proto/README.md#action_419)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### :triangular_flag_on_post: :one: Error 457 - CHANNEL_UPDATE_USERNAME_UPDATE_LOCK
Username has been changed recently, to renew it wait until the allowed time or choose the last one again for the request [#419](../proto/README.md#action_419)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 458 - CHANNEL_UPDATE_USERNAME_FORBIDDEN
You are forbidden to do the action for request [#419](../proto/README.md#action_419)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 460 - CHANNEL_REMOVE_USERNAME_BAD_PAYLOAD
Bad payload for request [#420](../proto/README.md#action_420)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 461 - CHANNEL_REMOVE_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#420](../proto/README.md#action_420)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 462 - CHANNEL_REMOVE_USERNAME_FORBIDDEN
You are forbidden to do the action for request [#420](../proto/README.md#action_420)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 463 - CHANNEL_REVOKE_LINK_BAD_PAYLOAD
Bad payload for request [#421](../proto/README.md#action_421)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|


### Error 464 - CHANNEL_REVOKE_LINK_INTERNAL_SERVER_ERROR
Internal server error for request [#421](../proto/README.md#action_421)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 465 - CHANNEL_REVOKE_LINK_FORBIDDEN
You are forbidden to do the action for request [#421](../proto/README.md#action_421)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 466 - CHANNEL_UPDATE_SIGNATURE_BAD_PAYLOAD
Bad payload for request [#422](../proto/README.md#action_422)

| Minor Code 	| Detail               	| Reaction 	|
|------------	|----------------------	|----------	|
| 1          	| Room_ID is invalid   	| *        	|
| 2          	| Signature is invalid 	| *        	|


### Error 467 - CHANNEL_UPDATE_SIGNATURE_INTERNAL_SERVER_ERROR
Internal server error for request [#422](../proto/README.md#action_422)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 468 - CHANNEL_UPDATE_SIGNATURE_FORBIDDEN
You are forbidden to do the action for request [#422](../proto/README.md#action_422)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 469 - CHANNEL_GET_MESSAGES_STATS_BAD_PAYLOAD
Bad payload for request [#423](../proto/README.md#action_423)

| Minor Code 	| Detail                                      	| Reaction 	|
|------------	|---------------------------------------------	|----------	|
| 1          	| Room_ID is invalid                          	| *        	|
| 2          	| At least one message is required            	| *        	|
| 3          	| Number of messages is more than the allowed 	| *        	|
| 4          	| Message_ID is invalid                       	| *        	|


### Error 470 - CHANNEL_GET_MESSAGES_STATS_INTERNAL_SERVER_ERROR
Internal server error for request [#423](../proto/README.md#action_423)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 471 - CHANNEL_GET_MESSAGES_STATS_FORBIDDEN
You are forbidden to do the action for request [#423](../proto/README.md#action_423)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 472 - CHANNEL_ADD_MESSAGE_REACTION_BAD_PAYLOAD
Bad payload for request [#424](../proto/README.md#action_424)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| Reaction is invalid   	| *        	|


### Error 473 - CHANNEL_ADD_MESSAGE_REACTION_INTERNAL_SERVER_ERROR
Internal server error for request [#424](../proto/README.md#action_424)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 474 - CHANNEL_ADD_MESSAGE_REACTION_FORBIDDEN
You are forbidden to do the action for request [#424](../proto/README.md#action_424)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 475 - CHANNEL_EDIT_MESSAGE_BAD_PAYLOAD
Bad payload for request [#425](../proto/README.md#action_425)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|
| 3          	| Message is invalid    	| *        	|


### Error 476 - CHANNEL_EDIT_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#425](../proto/README.md#action_425)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 477 - CHANNEL_EDIT_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#425](../proto/README.md#action_425)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 480 - CHANNEL_UPDATE_REACTION_STATUS_BAD_PAYLOAD
Bad payload for request [#426](../proto/README.md#action_426)

| Minor Code 	| Detail               	        | Reaction 	|
|------------	|----------------------	        |----------	|
| 1          	| Room_ID is invalid   	        | *        	|
| 2          	| reaction_status is invalid 	| *        	|


### Error 481 - CHANNEL_UPDATE_REACTION_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#426](../proto/README.md#action_426)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 482 - CHANNEL_UPDATE_REACTION_STATUS_FORBIDDEN
You are forbidden to do the action for request [#426](../proto/README.md#action_426)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 483 - CHANNEL_PIN_MESSAGE_BAD_PAYLOAD
Bad payload for request [#427](../proto/README.md#action_427)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|


### Error 484 - CHANNEL_PIN_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#427](../proto/README.md#action_427)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 485 - CHANNEL_PIN_MESSAGE_FORBIDDEN
You are forbidden to do the action for request [#427](../proto/README.md#action_427)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# Info Errors(5xx)
### Error 500 - INFO_LOCATION_NOT_FOUND
Location could not be found for the request [#500](../proto/README.md#action_500)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 501 - INFO_COUNTRY_BAD_PAYLOAD
Bad payload for request [#501](../proto/README.md#action_501)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| IsoCode is invalid 	| *        	|


### Error 502 - INFO_PAGE_BAD_PAYLOAD
Bad payload for request [#503](../proto/README.md#action_503)

| Minor Code 	| Detail      	| Reaction 	|
|------------	|-------------	|----------	|
| 1          	| ID is Wrong 	| *        	|


### Error 503 - INFO_PAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#503](../proto/README.md#action_503)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 504 - INFO_WALLPAPER_BAD_PAYLOAD
Bad payload for request [#504](../proto/README.md#action_504)

| Minor Code 	| Detail         	| Reaction 	|
|------------	|----------------	|----------	|
| 1          	| Fit is invalid 	| *        	|


### Error 505 - INFO_WALLPAPER_INTERNAL_SERVER_ERROR
Internal server error for request [#504](../proto/README.md#action_504)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# Client Errors(6xx)
### Error 600 - CLIENT_CONDITION_BAD_PAYLOAD
Bad payload for request [#600](../proto/README.md#action_600)

| Minor Code 	| Detail                              							| Reaction 	|
|------------	|-------------------------------------							|----------	|
| 1          	| Room_ID is invalid             						     	| *        	|
| 2          	| MessageVersion is invalid      						     	| *        	|
| 3          	| StatusVersion is invalid          						  	| *        	|
| 4          	| DeleteVersion is invalid          						  	| *        	|
| 5          	| OfflineDeleted is invalid           							| *        	|
| 6          	| OfflineEdited.Message_ID is invalid 							| *        	|
| 7          	| OfflineEdited.Message is invalid    							| *        	|
| 8          	| OfflineSeen is invalid          						    	| *        	|
| 9          	| Clear_ID is invalid             						    	| *        	|
| 10         	| CacheStart_ID is invalid       						     	| *        	|
| 11         	| CacheEnd_ID is invalid          						    	| *        	|
| 12         	| OfflineMute is invalid            						  	| *        	|
| 13         	| Your request is totally wrong       							| *        	|
| 14         	| OfflineListened is invalid          							| *        	|
| 15         	| Your request is totally wrong       							| *        	|
| 16         	| OfflineDeletedDeprecated & OfflineDeleted have been set both 	| *        	|
| 17         	| OfflineDeleted.Message_ID is invalid                         	| *        	|
| 18         	| OfflineDeleted.both is invalid                               	| *        	|


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

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| OffSet is invalid 	| *        	|
| 2          	| Limit is invalid  	| *        	|


### Error 611 - CLIENT_GET_ROOM_LIST_INTERNAL_SERVER_ERROR
Internal server error for request [#601](../proto/README.md#action_601)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 612 - CLIENT_GET_ROOM_BAD_PAYLOAD
Bad payload for request [#602](../proto/README.md#action_602)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Room_ID is invalid 	| *        	|


### Error 613 - CLIENT_GET_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#602](../proto/README.md#action_602)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 614 - CLIENT_GET_ROOM_NOT_FOUND
No Such room with the requested ID was found for request [#602](../proto/README.md#action_602)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 615 - CLIENT_GET_ROOM_HISTORY_BAD_PAYLOAD
Bad payload for request [#603](../proto/README.md#action_603)

| Minor Code 	| Detail                     	| Reaction 	|
|------------	|----------------------------	|----------	|
| 1          	| Room_ID is invalid         	| *        	|
| 2          	| FirstMessage_ID is invalid 	| *        	|
| 3          	| Direction is wrong         	| *        	|
| 4          	| Limit is invalid           	| *        	|


### Error 616 - CLIENT_GET_ROOM_HISTORY_INTERNAL_SERVER_ERROR
Internal server error for request [#603](../proto/README.md#action_603)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 617 - CLIENT_GET_ROOM_HISTORY_NOT_FOUND
There is no other massage to view for request [#603](../proto/README.md#action_603)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 618 - CLIENT_SEARCH_ROOM_HISTORY_BAD_PAYLOAD
Bad payload for request [#605](../proto/README.md#action_605)

| Minor Code 	| Detail                       	| Reaction 	|
|------------	|------------------------------	|----------	|
| 1          	| Room_ID is invalid           	| *        	|
| 2          	| OffSet is invalid            	| *        	|
| 3          	| Filter is invalid            	| *        	|
| 4          	| OffSet.Message_ID is invalid 	| *        	|


### Error 619 - CLIENT_SEARCH_ROOM_HISTORY_INTERNAL_SERVER_ERROR
Internal server error for request [#605](../proto/README.md#action_605)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 620 - CLIENT_SEARCH_ROOM_HISTORY_NOT_FOUND
There is no other massage to view for request [#605](../proto/README.md#action_605)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 621 - CLIENT_RESOLVE_USERNAME_BAD_PAYLOAD
Bad payload for request [#606](../proto/README.md#action_606)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Username is incorrect 	| *        	|


### Error 622 - CLIENT_RESOLVE_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#606](../proto/README.md#action_606)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 623 - CLIENT_RESOLVE_USERNAME_NOT_FOUND
There is no user with the requested username for the request [#606](../proto/README.md#action_606)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 624 - CLIENT_GET_ROOM_MESSAGE_BAD_PAYLOAD
Bad payload for request [#604](../proto/README.md#action_604)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Room_ID is invalid    	| *        	|
| 2          	| Message_ID is invalid 	| *        	|


### Error 625 - CLIENT_GET_ROOM_MESSAGE_INTERNAL_SERVER_ERROR
Internal server error for request [#604](../proto/README.md#action_604)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 626 - CLIENT_GET_ROOM_MESSAGE_NOT_FOUND
The requested message could not be found for request [#604](../proto/README.md#action_604)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 627 - CLIENT_CHECK_INVITE_LINK_BAD_PAYLOAD
Bad payload for request [#607](../proto/README.md#action_607)

| Minor Code 	| Detail                    	| Reaction 	|
|------------	|---------------------------	|----------	|
| 1          	| Invite Token is not valid 	| *        	|


### Error 628 - CLIENT_CHECK_INVITE_LINK_INTERNAL_SERVER_ERROR
Internal server error for request [#607](../proto/README.md#action_607)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 629 - CLIENT_CHECK_INVITE_LINK_NOT_FOUND
Invite Link of the room is invalid for request [#607](../proto/README.md#action_607)
| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 630 - CLIENT_JOIN_BY_INVITE_LINK_BAD_PAYLOAD
Bad payload for request [#608](../proto/README.md#action_608)

| Minor Code 	| Detail                    	| Reaction 	|
|------------	|---------------------------	|----------	|
| 1          	| Invite Token is not valid 	| *        	|


### Error 631 - CLIENT_JOIN_BY_INVITE_LINK_INTERNAL_SERVER_ERROR
Internal server error for request [#608](../proto/README.md#action_608)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 632 - CLIENT_JOIN_BY_INVITE_LINK_FORBIDDEN
You are forbidden to do the action for request [#608](../proto/README.md#action_608)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 633 - CLIENT_JOIN_BY_INVITE_LINK_ALREADY_JOINED
The user has already joined this room for request [#608](../proto/README.md#action_608)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|



### Error 634 - CLIENT_JOIN_BY_INVITE_LINK_PARTICIPANTS_COUNT_LIMIT_EXCEEDED
No other user is accepted to join this room because of the allowed number reached for request [#608](../proto/README.md#action_608)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 635 - CLIENT_JOIN_BY_USERNAME_BAD_PAYLOAD
Bad payload for request [#609](../proto/README.md#action_609)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Username is invalid 	| *        	|


### Error 636 - CLIENT_JOIN_BY_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#609](../proto/README.md#action_609)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 637 - CLIENT_JOIN_BY_USERNAME_FORBIDDEN
You are forbidden to do the action for request [#609](../proto/README.md#action_609)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 638 - CLIENT_JOIN_BY_USERNAME_ALREADY_JOINED
The user has already joined this room for request [#609](../proto/README.md#action_609)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 639 - CLIENT_JOIN_BY_USERNAME_PARTICIPANTS_COUNT_LIMIT_EXCEEDED
No other user is accepted to join this room because of the allowed number reached for request [#609](../proto/README.md#action_609)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 640 - CLIENT_SUBSCRIBE_TO_ROOM_BAD_PAYLOAD
Bad payload for request [#610](../proto/README.md#action_610)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Room_ID is invalid 	| *        	|


### Error 641 - CLIENT_SUBSCRIBE_TO_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#610](../proto/README.md#action_610)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 642 - CLIENT_SUBSCRIBE_TO_ROOM_FORBIDDEN
You are forbidden to do the action for request [#610](../proto/README.md#action_610)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 643 - CLIENT_UNSUBSCRIBE_FROM_ROOM_BAD_PAYLOAD
Bad payload for request [#611](../proto/README.md#action_611)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Room_ID is invalid 	| *        	|


### Error 644 - CLIENT_UNSUBSCRIBE_FROM_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#611](../proto/README.md#action_611)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 645 - CLIENT_SEARCH_USERNAME_BAD_PAYLOAD
Bad payload for request [#612](../proto/README.md#action_612)

| Minor Code 	| Detail           	| Reaction 	|
|------------	|------------------	|----------	|
| 1          	| Query is invalid 	| *        	|


### Error 646 - CLIENT_SEARCH_USERNAME_INTERNAL_SERVER_ERROR
Internal server error for request [#612](../proto/README.md#action_612)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 647 - CLIENT_COUNT_ROOM_HISTORY_BAD_PAYLOAD
Bad payload for request [#613](../proto/README.md#action_613)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Room_ID is invalid 	| *        	|


### Error 648 - CLIENT_COUNT_ROOM_HISTORY_INTERNAL_SERVER_ERROR
Internal server error for request [#613](../proto/README.md#action_613)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 649 - CLIENT_COUNT_ROOM_HISTORY_NOT_FOUND
No such room was found for request [#613](../proto/README.md#action_613)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 650 - CLIENT_MUTE_ROOM_BAD_PAYLOAD
Bad payload for request [#614](../proto/README.md#action_614)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Room_ID is invalid  	| *        	|
| 2          	| RoomMute is invalid 	| *        	|


### Error 651 - CLIENT_MUTE_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#614](../proto/README.md#action_614)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 652 - CLIENT_MUTE_ROOM_FORBIDDEN
You are forbidden to do the action for request [#614](../proto/README.md#action_614)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 653 - CLIENT_PIN_ROOM_BAD_PAYLOAD
Bad payload for request [#615](../proto/README.md#action_615)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Room_ID is invalid 	| *        	|
| 2          	| PIN is invalid     	| *        	|


### Error 654 - CLIENT_PIN_ROOM_INTERNAL_SERVER_ERROR
Internal server error for request [#615](../proto/README.md#action_615)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 655 - CLIENT_PIN_ROOM_FORBIDDEN
You are forbidden to do the action for request [#615](../proto/README.md#action_615)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 656 - CLIENT_ROOM_REPORT_BAD_PAYLOAD
Bad payload for request [#616](../proto/README.md#action_616)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| Room_ID is invalid     	| *        	|
| 2          	| Message_ID is invalid  	| *        	|
| 3          	| Reason is invalid      	| *        	|
| 4          	| Description is invalid 	|          	|


### Error 657 - CLIENT_ROOM_REPORT_INTERNAL_SERVER_ERROR
Internal server error for request [#616](../proto/README.md#action_616)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 658 - CLIENT_ROOM_REPORT_REPORTED_BEFORE
You have already reported this message/room for the request [#616](../proto/README.md#action_616)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 659 - CLIENT_ROOM_REPORT_FORBIDDEN
You are forbidden to do the action for request [#616](../proto/README.md#action_616)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 660 - CLIENT_REGISTER_DEVICE_BAD_PAYLOAD
Bad payload for request [#617](../proto/README.md#action_617)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| token is invalid 	    | *        	|
| 2          	| type is invalid 	    | *        	|


### Error 661 - CLIENT_REGISTER_DEVICE_INTERNAL_SERVER_ERROR
You are forbidden to do the action for request [#617](../proto/README.md#action_617)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 662 - CLIENT_REGISTER_DEVICE_FORBIDDEN
Internal server error for request [#617](../proto/README.md#action_617)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# File Errors(7xx)

### Error 700 - FILE_UPLOAD_OPTION_BAD_PAYLOAD.
Bad payload for request [#700](../proto/README.md#action_700)

| Minor Code 	| Detail          	| Reaction 	|
|------------	|-----------------	|----------	|
| 1          	| Size is invalid 	| *        	|


### Error 701 - FILE_UPLOAD_OPTION_INTERNAL_SERVER_ERROR
Internal server error for request [#700](../proto/README.md#action_700)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 702 - FILE_UPLOAD_INIT_BAD_PAYLOAD
Bad payload for for request [#701](../proto/README.md#action_701)

| Minor Code 	| Detail                  	| Reaction 	|
|------------	|-------------------------	|----------	|
| 1          	| Size is invalid         	| *        	|
| 2          	| First bytes are invalid 	| *        	|
| 3          	| Last bytes are invalid  	| *        	|
| 4          	| FileHash is invalid     	| *        	|
| 5          	| FileName is invalid     	| *        	|


### Error 703 - FILE_UPLOAD_INIT_INTERNAL_SERVER_ERROR
Internal server error for request [#701](../proto/README.md#action_701)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 704 - FILE_UPLOAD_BAD_PAYLOAD
Bad payload for request [#702](../proto/README.md#action_702)

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| Token is invalid  	| *        	|
| 2          	| OffSet is invalid 	| *        	|
| 3          	| OffSet is invalid 	| *        	|
| 4          	| Bytes are invalid 	| *        	|


### Error 705 - FILE_UPLOAD_INTERNAL_SERVER_ERROR
Internal server error for request [#702](../proto/README.md#action_702)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 706 - FILE_UPLOAD_FORBIDDEN
You are forbidden to do the action for request [#702](../proto/README.md#action_702)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 707 - FILE_UPLOAD_STATUS_BAD_PAYLOAD
Bad payload for request [#703](../proto/README.md#action_703)

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| Token is invalid  	| *        	|


### Error 708 - FILE_UPLOAD_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#703](../proto/README.md#action_703)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 709 - FILE_UPLOAD_STATUS_NOT_FOUND
No such file was found for request [#703](../proto/README.md#action_703)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 710 - FILE_INFO_BAD_PAYLOAD
Bad payload for request [#704](../proto/README.md#action_704)

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| Token is invalid  	| *        	|


### Error 711 - FILE_INFO_INTERNAL_SERVER_ERROR
Internal server error for request [#704](../proto/README.md#action_704)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 712 - FILE_INFO_NOT_FOUND
No such file was found for request [#704](../proto/README.md#action_704)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 713 - FILE_DOWNLOAD_BAD_PAYLOAD
Bad payload for request [#705](../proto/README.md#action_705)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Token is invalid    	| *        	|
| 2          	| OffSet is invalid   	| *        	|
| 3          	| MaxLimit is invalid 	| *        	|
| 4          	| Selector is invalid 	| *        	|


### Error 714 - FILE_DOWNLOAD_INTERNAL_SERVER_ERROR
Internal server error for request [#705](../proto/README.md#action_705)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 715 - FILE_DOWNLOAD_NOT_FOUND
No such file was found for request [#705](../proto/README.md#action_705)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


# QR code errors 7xx

### Error 800 - QR_CODE_JOIN_BAD_PAYLOAD
Bad payload for request [#800](../proto/README.md#action_800)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| InviteToken is invalid 	| *        	|


### Error 801 - QR_CODE_JOIN_INTERNAL_SERVER_ERROR
Internal server error for request [#800](../proto/README.md#action_800)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 802 - QR_CODE_RESOLVE_BAD_PAYLOAD
Bad payload for request [#801](../proto/README.md#action_801)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Username is invalid   	| *        	|
| 2          	| Message_ID is invalid 	| *        	|


### Error 803 - QR_CODE_RESOLVE_INTERNAL_SERVER_ERROR
Internal server error for request [#801](../proto/README.md#action_801)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 804 - QR_CODE_NEW_DEVICE_BAD_PAYLOAD
Bad payload for request [#802](../proto/README.md#action_802)

| Minor Code 	| Detail                     	| Reaction 	|
|------------	|----------------------------	|----------	|
| 1          	| AppName is invalid         	| *        	|
| 2          	| App_ID is invalid          	| *        	|
| 3          	| AppBuildVersion is invalid 	| *        	|
| 4          	| AppVersion is invalid      	| *        	|
| 5          	| Platform is invalid        	| *        	|
| 6          	| PlatformVersion is invalid 	| *        	|
| 7          	| Device is invalid          	| *        	|
| 8          	| DeviceName is invalid      	| *        	|


### Error 805 - QR_CODE_NEW_DEVICE_INTERNAL_SERVER_ERROR
Internal server error for request [#802](../proto/README.md#action_802)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 806 - QR_CODE_ADD_CONTACT_BAD_PAYLOAD
Bad payload for request [#803](../proto/README.md#action_803)

| Minor Code 	| Detail                 	| Reaction 	|
|------------	|------------------------	|----------	|
| 1          	| Phone is invalid       	| *        	|
| 2          	| First name is invalid  	| *        	|
| 3          	| Last name is invalid   	| *        	|


### Error 807 - QR_CODE_ADD_CONTACT_INTERNAL_SERVER_ERROR
Internal server error for request [#803](../proto/README.md#action_803)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 808 - QR_CODE_ADD_ME_BAD_PAYLOAD
Bad payload for request [#804](../proto/README.md#action_804)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 809 - QR_CODE_ADD_ME_INTERNAL_SERVER_ERROR
Internal server error for request [#804](../proto/README.md#action_804)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|



# Signaling errors 9xx

### Error 900 - SIGNALING_GET_CONFIGURATION_BAD_PAYLOAD
Bad payload for request [#900](../proto/README.md#action_900)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 901 - SIGNALING_GET_CONFIGURATION_INTERNAL_SERVER_ERROR
Internal server error for request [#900](../proto/README.md#action_900)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 902 - SIGNALING_OFFER_BAD_PAYLOAD
Bad payload for request [#901](../proto/README.md#action_901)

| Minor Code 	| Detail                   	| Reaction 	|
|------------	|--------------------------	|----------	|
| 1          	| CalledUser_ID is invalid 	| *        	|
| 2          	| Type is invalid          	| *        	|
| 3          	| Caller_SDP is invalid    	| *        	|


### Error 903 - SIGNALING_OFFER_INTERNAL_SERVER_ERROR
Internal server error for request [#901](../proto/README.md#action_901)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 904 - SIGNALING_OFFER_FORBIDDEN
You are forbidden to do the action for request [#901](../proto/README.md#action_901)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 905 - SIGNALING_OFFER_BLOCKED_BY_PEER
You have got blocked by the peer for request [#901](../proto/README.md#action_901)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 906 - SIGNALING_OFFER_PRIVACY_PROTECTION
You cannot call this user because of the protected privacy for the request [#901](../proto/README.md#action_901)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 907 - SIGNALING_RINGING_BAD_PAYLOAD
Bad payload for request [#902](../proto/README.md#action_902)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 908 - SIGNALING_RINGING_INTERNAL_SERVER_ERROR
Internal server error for request [#902](../proto/README.md#action_902)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 909 - SIGNALING_RINGING_FORBIDDEN
You are forbidden to do the action for request [#902](../proto/README.md#action_902)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 910 - SIGNALING_ACCEPT_BAD_PAYLOAD
Bad payload for request [#903](../proto/README.md#action_903)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Called_SDP is invalid 	| *        	|


### Error 911 - SIGNALING_ACCEPT_INTERNAL_SERVER_ERROR
Internal server error for request [#903](../proto/README.md#action_903)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 912 - SIGNALING_ACCEPT_FORBIDDEN
You are forbidden to do the action for request [#903](../proto/README.md#action_903)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 913 - SIGNALING_CANDIDATE_BAD_PAYLOAD
Bad payload for request [#904](../proto/README.md#action_904)

| Minor Code 	| Detail                     	| Reaction 	|
|------------	|----------------------------	|----------	|
| 1          	| Candidate is invalid       	| *        	|
| 2          	| SDP_MID is invalid         	| *        	|
| 3          	| SDP_M_Line_Index is invalid 	| *        	|



### Error 914 - SIGNALING_CANDIDATE_INTERNAL_SERVER_ERROR
Internal server error for request [#904](../proto/README.md#action_904)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 915 - SIGNALING_CANDIDATE_FORBIDDEN
You are forbidden to do the action for request [#904](../proto/README.md#action_904)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 916 - SIGNALING_LEAVE_BAD_PAYLOAD
Bad payload for request [#905](../proto/README.md#action_905)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 917 - SIGNALING_LEAVE_INTERNAL_SERVER_ERROR
Internal server error for request [#905](../proto/README.md#action_905)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 918 - SIGNALING_LEAVE_FORBIDDEN
You are forbidden to do the action for request [#905](../proto/README.md#action_905)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### error 919 - SIGNALING_SESSION_HOLD_BAD_PAYLOAD
Bad payload for request [#906](../proto/README.md#action_906)

| Minor Code 	| Detail          	| Reaction 	|
|------------	|-----------------	|----------	|
| 1          	| Hold is invalid 	| *        	|


### Error 920 - SIGNALING_SESSION_HOLD_INTERNAL_SERVER_ERROR
Internal server error for request [#906](../proto/README.md#action_906)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 921 - SIGNALING_SESSION_HOLD_FORBIDDEN
You are forbidden to do the action for request [#906](../proto/README.md#action_906)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 922 - SIGNALING_GET_LOG_BAD_PAYLOAD
Bad payload for request [#907](../proto/README.md#action_907)

| Minor Code 	| Detail                	| Reaction 	|
|------------	|-----------------------	|----------	|
| 1          	| Pagination is invalid 	| *        	|
| 2          	| OffSet is invalid     	| *        	|
| 3          	| Limit is invalid      	| *        	|


### Error 923 - SIGNALING_GET_LOG_INTERNAL_SERVER_ERROR
Internal server error for request [#907](../proto/README.md#action_907)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### error 924 - SIGNALING_CLEAR_LOG_BAD_PAYLOAD
Bad payload for request [#908](../proto/README.md#action_908)

| Minor Code 	| Detail              	| Reaction 	|
|------------	|---------------------	|----------	|
| 1          	| Clear_ID is invalid 	| *        	|


### Error 925 - SIGNALING_CLEAR_LOG_INTERNAL_SERVER_ERROR
Internal server error for request [#908](../proto/README.md#action_908)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 926 - SIGNALING_RATE_BAD_PAYLOAD
Bad payload for request [#909](../proto/README.md#action_909)

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| ID is invalid     	| *        	|
| 2          	| Rate is invalid   	| *        	|
| 3          	| Reason is invalid 	| *        	|


### Error 927 - SIGNALING_RATE_INTERNAL_SERVER_ERROR
Internal server error for request [#909](../proto/README.md#action_909)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 928 - SIGNALING_RATE_FORBIDDEN
You are forbidden to do the action for request [#909](../proto/README.md#action_909)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|



# Geo errors 10xx

### Error 1000 - GEO_GET_REGISTER_STATUS_BAD_PAYLOAD
Bad payload for request [#1000](../proto/README.md#action_1000)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1001 - GEO_GET_REGISTER_STATUS_INTERNAL_SERVER_ERROR
Internal server error for request [#1000](../proto/README.md#action_1000)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1002 - GEO_REGISTER_BAD_PAYLOAD
Bad payload for request [#1001](../proto/README.md#action_1001)

| Minor Code 	| Detail            	| Reaction 	|
|------------	|-------------------	|----------	|
| 1          	| Enable is invalid 	| *        	|


### Error 1003 - GEO_REGISTER_INTERNAL_SERVER_ERROR
Internal server error for request [#1001](../proto/README.md#action_1001)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1004 - GEO_UPDATE_POSITION_BAD_PAYLOAD
Bad payload for request [#1002](../proto/README.md#action_1002)

| Minor Code 	| Detail         	| Reaction 	|
|------------	|----------------	|----------	|
| 1          	| Lat is invalid 	| *        	|
| 2          	| Lon is invalid 	| *        	|


### Error 1005 - GEO_UPDATE_POSITION_INTERNAL_SERVER_ERROR
Internal server error for request [#1002](../proto/README.md#action_1002)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1006 - GEO_UPDATE_POSITION_FORBIDDEN
You are forbidden to do the action for request [#1002](../proto/README.md#action_1002)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1007 - GEO_GET_COMMENT_BAD_PAYLOAD
Bad payload for request [#1003](../proto/README.md#action_1003)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| User_ID is invalid 	| *        	|


### Error 1008 - GEO_GET_COMMENT_INTERNAL_SERVER_ERROR
Internal server error for request [#1003](../proto/README.md#action_1003)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1009 - GEO_GET_COMMENT_FORBIDDEN
You are forbidden to do the action for request [#1003](../proto/README.md#action_1003)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1010 - GEO_UPDATE_COMMENT_BAD_PAYLOAD
Bad payload for request [#1004](../proto/README.md#action_1004)

| Minor Code 	| Detail             	| Reaction 	|
|------------	|--------------------	|----------	|
| 1          	| Comment is invalid 	| *        	|


### error 1011 - GEO_UPDATE_COMMENT_INTERNAL_SERVER_ERROR
Internal server error for request [#1004](../proto/README.md#action_1004)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1012 - GEO_UPDATE_COMMENT_FORBIDDEN
You are forbidden to do the action for request [#1004](../proto/README.md#action_1004)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1013 - GEO_GET_NEARBY_DISTANCE_BAD_PAYLOAD
Bad payload for request [#1005](../proto/README.md#action_1005)

| Minor Code 	| Detail         	| Reaction 	|
|------------	|----------------	|----------	|
| 1          	| Lat is invalid 	| *        	|
| 2          	| Lon is invalid 	| *        	|


### Error 1014 - GEO_GET_NEARBY_DISTANCE_INTERNAL_SERVER_ERROR
Internal server error for request [#1005](../proto/README.md#action_1005)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1015 - GEO_GET_NEARBY_DISTANCE_FORBIDDEN
You are forbidden to do the action for request [#1005](../proto/README.md#action_1005)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1016 - GEO_GET_NEARBY_COORDINATE_BAD_PAYLOAD
Bad payload for request [#1006](../proto/README.md#action_1006)

| Minor Code 	| Detail         	| Reaction 	|
|------------	|----------------	|----------	|
| 1          	| Lat is invalid 	| *        	|
| 2          	| Lon is invalid 	| *        	|


### Error 1017 - GEO_GET_NEARBY_COORDINATE_INTERNAL_SERVER_ERROR
Internal server error for request [#1006](../proto/README.md#action_1006)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1018 - GEO_GET_NEARBY_COORDINATE_FORBIDDEN
You are forbidden to do the action for request [#1006](../proto/README.md#action_1006)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


###  Error 1019 - GEO_GET_CONFIGURATION_BAD_PAYLOAD
Bad payload for request [#1007](../proto/README.md#action_1007)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 1020 - GEO_GET_CONFIGURATION_INTERNAL_SERVER_ERROR
Internal server error for request [#1007](../proto/README.md#action_1007)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# Wallet errors 90xx

### Error 9000 - WALLET_GET_ACCESS_TOKEN_BAD_PAYLOAD
Bad payload for request [#9000](../proto/README.md#action_9000)

| Minor Code 	| Detail         	| Reaction 	|
|------------	|----------------	|----------	|
| *          	| *      	        | *        	|


### Error 9001 - WALLET_GET_ACCESS_TOKEN_INTERNAL_SERVER_ERROR
Internal server error for request [#9000](../proto/README.md#action_9000)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9002 - WALLET_GET_ACCESS_TOKEN_BAD_GATEWAY
Server was not able to get a valid or any response from the Wallet server for request [#9000](../proto/README.md#action_9000)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9003 - WALLET_GET_ACCESS_TOKEN_FORBIDDEN
You are forbidden to do the action for request [#9000](../proto/README.md#action_9000)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 9004 - WALLET_PAYMENT_INIT_BAD_PAYLOAD
Bad payload for request [#9001](../proto/README.md#action_9001)

| Minor Code 	| Detail         	        | Reaction 	|
|------------	|----------------	        |----------	|
| 1          	| language is invalid      	| *        	|
| 2          	| jwt is invalid      	    | *        	|
| 3          	| to_user_id is invalid     | *        	|
| 4          	| amount is invalid      	| *        	|
| 5          	| description is invalid    | *        	|


### Error 9005 - WALLET_PAYMENT_INIT_INTERNAL_SERVER_ERROR
Internal server error for request [#9001](../proto/README.md#action_9001)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9006 - WALLET_PAYMENT_INIT_BAD_GATEWAY
Server was not able to get a valid or any response from the Wallet server for request [#9001](../proto/README.md#action_9001)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9007 - WALLET_PAYMENT_INIT_FORBIDDEN
You are forbidden to do the action for request [#9001](../proto/README.md#action_9001)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9008 - WALLET_PAYMENT_INIT_RECIPIENT_FORBIDDEN
Recipient are forbidden for request [#9001](../proto/README.md#action_9001)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9009 - WALLET_PAYMENT_INIT_GATEWAY_ERROR
Error from Wallet server for request [#9001](../proto/README.md#action_9001)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9010 - WALLET_PAYMENT_INIT_RECIPIENT_NOT_REGISTERED
Recipient is not registered in wallet for request [#9001](../proto/README.md#action_9001)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 9011 - WALLET_REGISTER_BAD_PAYLOAD
Bad payload for request [#9002](../proto/README.md#action_9002)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9012 - WALLET_REGISTER_INTERNAL_SERVER_ERROR
Internal server error for request [#9002](../proto/README.md#action_9002)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9013 - WALLET_REGISTER_FORBIDDEN
You are forbidden to do the action for request [#9002](../proto/README.md#action_9002)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 9014 - WALLET_ID_MAPPING_BAD_PAYLOAD
Bad payload for request [#9003](../proto/README.md#action_9003)

| Minor Code 	| Detail 	                    | Reaction 	|
|------------	|--------	                    |----------	|
| 1          	| wallet_id is invalid      	| *        	|


### Error 9015 - WALLET_ID_MAPPING_INTERNAL_SERVER_ERROR
Internal server error for request [#9003](../proto/README.md#action_9003)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9016 - WALLET_ID_MAPPING_NOT_FOUND
No such user was found for request [#9003](../proto/README.md#action_9003)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# Mpl errors 90xx

### Error 9100 - MPL_GET_BILL_TOKEN_BAD_PAYLOAD
Bad payload for request [#9100](../proto/README.md#action_9100)

| Minor Code 	| Detail         	        | Reaction 	|
|------------	|----------------	        |----------	|
| 1          	| bill_id is invalid        | *        	|
| 2          	| pay_id is invalid         | *        	|


### Error 9101 - MPL_GET_BILL_TOKEN_INTERNAL_SERVER_ERROR
Internal server error for request [#9100](../proto/README.md#action_9100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9102 - MPL_GET_BILL_TOKEN_BAD_GATEWAY
Server was not able to get a valid or any response from the Mpl server for request [#9100](../proto/README.md#action_9100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9103 - MPL_GET_BILL_TOKEN_FORBIDDEN
You are forbidden to do the action for request [#9100](../proto/README.md#action_9100)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 9104 - MPL_GET_TOPUP_TOKEN_BAD_PAYLOAD
Bad payload for request [#9101](../proto/README.md#action_9101)

| Minor Code 	| Detail         	                    | Reaction 	|
|------------	|----------------	                    |----------	|
| 1          	| charge_mobile_number is invalid       | *        	|
| 2          	| amount is invalid                     | *        	|
| 2          	| type is invalid                       | *        	|


### Error 9105 - MPL_GET_TOPUP_TOKEN_INTERNAL_SERVER_ERROR
Internal server error for request [#9101](../proto/README.md#action_9101)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9106 - MPL_GET_TOPUP_TOKEN_BAD_GATEWAY
Server was not able to get a valid or any response from the Mpl server for request [#9101](../proto/README.md#action_9101)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9107 - MPL_GET_TOPUP_TOKEN_FORBIDDEN
You are forbidden to do the action for request [#9101](../proto/README.md#action_9101)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

# BillInquiry errors 92xx

### Error 9200 - BILL_INQUIRY_MCI_BAD_PAYLOAD
Bad payload for request [#9200](../proto/README.md#action_9200)

| Minor Code 	| Detail         	              | Reaction 	|
|------------	|----------------	              |----------	|
| 1          	| mobile_number is invalid        | *        	|


### Error 9201 - BILL_INQUIRY_MCI_INTERNAL_SERVER_ERROR
Internal server error for request [#9200](../proto/README.md#action_9200)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9202 - BILL_INQUIRY_MCI_BAD_GATEWAY
Server was not able to get a valid or any response from the bill inquiry server for request [#9200](../proto/README.md#action_9200)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9203 - BILL_INQUIRY_MCI_FORBIDDEN
You are forbidden to do the action for request [#9200](../proto/README.md#action_9200)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|

### Error 9204 - BILL_INQUIRY_TELECOM_BAD_PAYLOAD
Bad payload for request [#9201](../proto/README.md#action_9201)

| Minor Code 	| Detail         	                    | Reaction 	|
|------------	|----------------	                    |----------	|
| 1          	| province_code is invalid              | *        	|
| 2          	| telephone_number is invalid           | *        	|


### Error 9205 - BILL_INQUIRY_TELECOM_INTERNAL_SERVER_ERROR
Internal server error for request [#9201](../proto/README.md#action_9201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9206 - BILL_INQUIRY_TELECOM_BAD_GATEWAY
Server was not able to get a valid or any response from the bill inquiry server for request [#9201](../proto/README.md#action_9201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|


### Error 9207 - BILL_INQUIRY_TELECOM_FORBIDDEN
You are forbidden to do the action for request [#9201](../proto/README.md#action_9201)

| Minor Code 	| Detail 	| Reaction 	|
|------------	|--------	|----------	|
| *          	| *      	| *        	|