# Response Masking Policy for Mule 4

In certain scenarios, the response is required to be masked to comply with regulations. 
This policy will help Mule developers implement solutions to achieve the same.

This custom policy will do the following:
- Mask fields
- Skip masking for exempted users


## Deploying to Exchange
Clone the project to your local, change the groupId to point your orgId. Issue `mvn deploy`.

Ensure that there is an entry in your settings.xml pertaining to exchange-server

Check if the policy is being deployed to https://maven.anypoint.mulesoft.com/api/v1 or https://maven.anypoint.mulesoft.com/api/v2

## Configuration

The field name in `()` is the corresponding yaml field name.

### Fields to be masked (maskingSelectorsList)

These fields will be provided in the form of comma separated values.
Example: `ssn,dob`

### Users to be exempted (exemptedUsers)

Certain users can be exempted from any kind of data masking. Userid/names are to be provided in a comma separated format.
Example: `biswa,usera`

**User is currently being consumed from `authentication.properties.claims.uid` or `attributes.headers.uid`. Modify as required.**