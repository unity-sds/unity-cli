# Unity-SDS CLI

 
 A CLI for the Unity Platform

 This github repository and archive is now archived. Please see https://github.com/unity-sds/unity-py for more up-to-date tooling for interacting with the Unity system.

## Setup / env

We need to have the unity login for authorization, so set the following environment variables:
```
export UNITY_USER=$UNITY_COGNITO_USERNAME
export UNITY_PASSWORD=$UNITY_COGNITO_PASSWORD
```

# Examples

List collections in the Unity System:
```
 python unity/main.py data get-collections | jq  '.features[].id'

"SNDR_SNPP_ATMS_L1A___1"
"L0_SNPP_EphAtt___1"
"L0_SNPP_ATMS_SCIENCE___1"
```

List the items (data files) in a collection:
```
(base) MT-212570:unity-cli gangl$ python unity/main.py data get-collection L0_SNPP_EphAtt___1 | jq  '.features[].assets.data | .title,.href'

"P1570011AAAAAAAAAAAAAT16015034636900.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16015034636900.PDS"
"P1570011AAAAAAAAAAAAAT16014190248700.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014190248700.PDS"
"P1570011AAAAAAAAAAAAAT16014225007600.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014225007600.PDS"
"P1570011AAAAAAAAAAAAAT16015022900600.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16015022900600.PDS"
"P1570011AAAAAAAAAAAAAT16014220241900.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014220241900.PDS"
"P1570011AAAAAAAAAAAAAT16014233550900.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014233550900.PDS"
"P1570011AAAAAAAAAAAAAT16014230057500.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014230057500.PDS"
"P1570011AAAAAAAAAAAAAT16014184934800.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014184934800.PDS"
"P1570011AAAAAAAAAAAAAT16014223957700.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014223957700.PDS"
"P1570011AAAAAAAAAAAAAT16014214620700.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014214620700.PDS"
"P1570011AAAAAAAAAAAAAT16014201831600.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014201831600.PDS"
"P1570011AAAAAAAAAAAAAT16014210755400.PDS"
"s3://uds-dev-cumulus-protected/SNPP_EphAtt___1/P1570011AAAAAAAAAAAAAT16014210755400.PDS"
```
