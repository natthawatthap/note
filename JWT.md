JWT stands for JSON Web Token. It is a compact, URL-safe means of representing claims to be transferred between two parties. These claims can be verified and are often used for authentication and information exchange in a compact and self-contained manner. JWTs are commonly used in web development for authentication purposes.

A JWT typically consists of three parts:

1. **Header:** The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

2. **Payload:** The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.

3. **Signature:** To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

The resulting JWT is a string that can be sent in an HTTP header and verified on the server to ensure the integrity of the data it contains.

Here's an example of a JWT:

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```

It consists of three parts separated by dots (`.`). The first part is the header, the second part is the payload, and the third part is the signature. Each part is base64-encoded.