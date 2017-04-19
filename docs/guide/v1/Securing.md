# Encryption
## Step 1
After websocket connection is established , You will receive message [#30001](proto/README.md#action_30001)

You must generate random string called **symmetricKey** with length equal to _symmetricKeyLength_ and encrypt it with _publicKey_ using OpenSSL library (Padding mode is PKCS #1)


## Step 2
Send message [#2](proto/README.md#action_2) with encrypted **symmetricKey** to server , depending on your request there are three cases of response

1. You send plaintext symmetricKey and we cannot accept this key so you will go back to step 1 (After 3 times , your request will be ignored)
2. Your encrypted symmetricKey length is not equal to _symmetricKeyLength_ , You will receive message [#30002](proto/README.md#action_30002) with **REJECTED** status . Websocket connection shall get closed permanently in this case.
3. Your symmetricKey is accepted successfully , You will receive message [#30002](proto/README.md#action_30002) with **ACCEPTED** status

## Step 3
For each request , you must encrypt your request using **symmetricKey** with _symmetricMethod_ (Padding mode is PKCS #5) and **cryptographically strong pseudo-random bytes** IV with size equal to _symmetricIvSize_

See [RAND_bytes](https://www.openssl.org/docs/manmaster/crypto/RAND_bytes.html) for more details

## Step 4
Send your request in the flowing format:
```
"IV" + "Encrypted Request"
```


# Decryption
# Step 1
Server responses must be decrypted after securing connection. In this case, response format is:
```
"IV" + "Encrypted Response"
```

Split response using _symmetricIvSize_ , 0 to _symmetricIvSize_ is IV and _symmetricIvSize_ to end is encrypted response

# Step 2
For each response , you must decrypt it using **symmetricKey** with _symmetricMethod_ and IV
