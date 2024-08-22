# Identity and Access Management (IAM)

To create an AWS account you must provide a unique email, account name and a credit card.You can use same credit card for different accounts.

When you create an account you get a Root user, The Root user has access to everything in the account and can perform any action on any resource within the account.


<tip>
But assuming You have a new employee in your organization and you want to provide access and also maybe restrict access to ceartain resources.
</tip>

![image_46.png](image_46.png)

This is where IAM comes in.

### Identity and Access Management (IAM)

IAM manages access to AWS resources. IAM handles who is authenticated and what are they authorized to do.

There are three types of Identities:
<ul>
<li>Users</li>
<li>Groups</li>
<li>Roles</li>
</ul>

IAM **policies** define what resources a user/group/role has access to and what actions they can perform on them.
![image_47.png](image_47.png)


## User
 IAM user is just an organization or user who wants to access a set of services within AWS .

But what do users have access to?
<tip>
Users have to be granted explicit permissions to access specific
services/resources.

Users are implicitly denied all permissions by default
</tip>
## Policies
To grant users access to resources, IAM policies need to be applied to the user, giving
them permissions.

Policies are documents that either grant or deny access to specific AWS
services/resources.
![image_48.png](image_48.png)

### Policy Example

![image_49.png](image_49.png)


This policy has a version which can change based on the recent AWS policy version.
Statement is what permissions you want to grant access to.
![image_50.png](image_50.png)

The above policy has a unique id and allows a user to access to all  EC2 resources.
![image_51.png](image_51.png)
The second permission allows a user to list and get all objects in a S3  bucket

<tip>
Now we have a user and policies
</tip>

### Users and Policies
We now attach a policy to a user since by default they don't have access to anything 
![image_52.png](image_52.png)

### Least Privilege Permission
Identities/ users should only be granted the minimum permissions necessary for the to perform their job.
<tip>
For every new user created you have to give them certain permissions and you have to remember to always give them permission.

If I have a bunch of users that require same permission we can create groups.
</tip>

## Groups

Groups are a collection of IAM users.
- Policies can be added to groups
- IAM users within a group automatically inherit all the policies from the
  group
- Example – having a separate group for each department

### Roles
Roles allow users, applications, or services to assume temporary permissions.
- Roles are assigned permissions/policies just like users and groups
- When someone assumes an IAM role, they inherit the permission of the
  role temporarily and return to their original permission when done

## Multi-Factor Authentication (MFA)

To login to an AWS root account you must provide an Email and a Password. If they leak or hacked then other people will have access to 
your account and might do malicious acts.
 
To prevent this we can create an Extra security , a code that will be generated on an MFA device/app which changes periodically. This code will then be sent to AWS to verify the user. 
So they can have the email and password but if they dont have a code then they cant access your account.



## Organizations
Organizations help manage multiple AWS accounts
Organizational units (OUs) allow you to group accounts with similar business or security
requirements 

Service Control Policies (SCPs) restrict what an account can do
- SCPs can be applied to individual accounts or OUs
- When applied to OUs, all AWS accounts within the OU inherit the policies