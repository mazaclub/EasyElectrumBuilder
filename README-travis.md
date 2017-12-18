# Notes on Travis-CI automated builds

## Branches

## PRs

## Weekly Builds

## Siging & uploading distribution files

one method of deployment is to 
 - generate an ssh key for this use
 - add as a deploy key to the repo
 - encrypt the private key 
 ```
 travis encrypt-file ./id_rsa --add
 ```
 - 
