# Command References

## Conjur Variable set command
```
conjur variable set -i data/dev-upt/username -v uptadmin 
```
## Conjur variable get command
```
conjur variable get -i data/dev-upt/username
```

# Conjur fetch secrets
Curl Commands to fetch conjur secrets
1. Run the command using the api key
```
curl --header "Accept-Encoding: base64" --data 3h06wmq2ga2vfa3xypbcjnfsg911mpdz711wfzkev1jaxnzf1ysm2pn https://india.secretsmgr.cyberark.cloud/api/authn/conjur/host%2Fdata%2Fupt-tutorial-host
/authenticate
```
2. run the below command with the token from above command
```
curl -H 'Authorization: Token token="<Token>"' \https://india.secretsmgr.cyberark.cloud/api/secrets/conjur/variable/data/dev-upt/password
```

# Conjur load policy reference

## conjur load policy
```
conjur policy load -b data -f 3-permit-group.yml   
```
## Conjur update policy. Mostly for updating and deleting the existing configuration
```
conjur policy update -b data -f 5-host-delete.yml
```

