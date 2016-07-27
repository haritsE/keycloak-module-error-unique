# Keycloak Custom Authenticator Module

## Description
A custom authenticator for keycloak, that rejects login if a user is unique. Modified from `IdpCreateUserIfUniqueAuthenticator` and `IdpCreateUserIfUniqueAuthenticatorFactory` class from keycloak default authenticator.

## Use case
Login is only allowed if user exist in keycloak DB, if not, rejects them. Replace the original "Create user if unique" in first broker login with this execution.

## How to build & deploy
- `mvn package`
- Copy .jar from `/target` and copy it to the `/providers` directory
