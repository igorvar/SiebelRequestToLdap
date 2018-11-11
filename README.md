# SiebelRequestToLdap
Get data about user from LDAP
The solution for cases when user authentication in Sibel is configured via LDAP, and users log in from a domain other than the organization's domain.

In the case of the expiration date of the password, such users cannot log in to Sibel. As a solution, it is proposed X days before the expiration date of the password to show it a warning every time the user logs on.

The expiration date for the password is stored in LDAP. For their extraction and written the this service.

Input parameters:
- UserName (required)
- Domain (current domain by default)

Output:
- PasswordRequired - Y if need password for identification, N - user log in w/o password
- PasswordNeverExpires - some users do not need to change the password.
- Fields about password expiraion date.
