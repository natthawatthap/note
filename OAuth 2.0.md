OAuth 2.0 (Open Authorization 2.0) is an industry-standard authorization protocol that enables secure authorization flows between different services, particularly in the context of web and mobile applications interacting with APIs. OAuth 2.0 is designed to provide a straightforward way for users to grant limited access to their resources without sharing their credentials (such as username and password).

Key features and concepts of OAuth 2.0 include:

1. **Roles:**
   - **Resource Owner (User):** The entity that owns the resource and can grant access to it. This is typically the end-user.
   - **Client:** The application making requests on behalf of the resource owner. This can be a web application, mobile app, or server.
   - **Authorization Server:** The server responsible for authenticating the resource owner and obtaining authorization. It issues access tokens to the client after successful authentication.
   - **Resource Server:** The server hosting the protected resources. It validates access tokens and serves the protected resources.

2. **Authorization Grant Types:**
   - **Authorization Code Grant:** Used by web applications. The client redirects the resource owner to the authorization server, which returns an authorization code. The client exchanges this code for an access token.
   - **Implicit Grant:** Used by mobile and browser-based applications. The access token is obtained directly without an intermediate authorization code.
   - **Client Credentials Grant:** Used by clients to authenticate with the authorization server using their credentials. Typically used for machine-to-machine communication.
   - **Resource Owner Password Credentials Grant:** The resource owner's credentials are used directly by the client to obtain an access token.

3. **Access Token:**
   - The access token is a credential that represents the authorization granted to the client by the resource owner. It is used by the client to access protected resources on behalf of the resource owner.

4. **Scope:**
   - Scopes define the permissions granted to the client. The resource owner may be asked to approve different scopes during the authorization process.

5. **Refresh Token:**
   - Some grant types (e.g., Authorization Code Grant) may return a refresh token, allowing the client to obtain a new access token without involving the resource owner.

OAuth 2.0 is widely adopted and used for securing APIs, enabling Single Sign-On (SSO), and supporting various application scenarios where controlled access to resources is required. It is important to note that OAuth 2.0 focuses on authorization and delegation, not on authentication. In scenarios where authentication is needed, OpenID Connect (OIDC) is often used in conjunction with OAuth 2.0.