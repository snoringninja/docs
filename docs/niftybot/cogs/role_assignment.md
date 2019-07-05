# Role Assignment
### Purpose
This cog is designed to allow your users to add themselves to a group.  This can be useful for servers that are 
multi-purpose, so that people can join just the groups that are relevant to them. 
As always, the [code](https://github.com/snoringninja/niftybot-discord/blob/master/cogs/role_assignment.py "code") 
is internally documented and may be looked at for further understanding.

---

### Commands / Parameters
There are multiple different ways to use this module, which are documented below.

#### (prefix)guild ROLE_NAME
This command allows a user to request to join a group.  The group must exist within the role_list inside the 
RoleAssignment category of the server settings. If they are already in this group, they are informed of that. 
If the role does not exist, nothing happens.  
Example: &guild TestRole

#### (prefix)role add/remove ROLE_NAME
This command adds or removes a role from the role_list in the server settings.  You may ping the group you wish to add, 
or pass in the direct snowflake_id  
Example: &role add @TestRole

#### (prefix)rolechannel add/remove CHANNEL_ID
This command adds or removes a role from the assignment_channel_id in the server settings.  You must pass in the direct 
snowflake_id at this time.  
Example: &rolechannel add 234897237489273
