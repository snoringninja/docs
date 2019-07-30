# Role Assignment
!!! important
    Remember all commands must be prefixed by whatever prefix is set in the niftybot.ini file.
---

## RoleAssignor
*class* cogs.role_assignment.RoleAssignor(*bot*)
>Handles commands for adding or removing a role, adding or removing a channel, or adding a user to a configured role

!!! warning "**TODO**"
    Allow owners to add roles/channels simply by passing in the name of the role or channel instead of requiring 
    them to use the snowflake ID; if there happens to be more than one of either, then require the owner to use the 
    specific ID

---

### assign_role
*command* **assign_role**(*ctx, guild, member*)
> Assign users to a configured role if requested.  Command is executed via the `guild` command.

* **Parameters**:
    * **ctx** - discord.py Context object  
    * **guild** (str) -  the requested group name, uses consume rest behavior
    * **member** - optional discord.Member object
    
**Returns**: Nothing

**Examples**:
```nohighlight
guild Test
{user.mention}: You've been successfully added to {guild_name}.

guild Test
{user.mention}: You've been removed from {guild_name}.
```

---

### update_role_list
*command* **update_role_list**(*ctx, add_or_remove, role_id, member*)
> Update the role list within the server configuration file to add or remove a group. Command is executed via the 
`role` command.

* **Parameters**:  
    * **ctx**: discord.py Context object  
    * **add_or_remove** (str) [add, remove] - passed in string to determine if a role is being added or removed  
    * **role_id** (str) - discord snowflake ID for the role, can be added via direct pinging of the role  
    * **member** - optional discord.Member object
    
**Returns**: Nothing

**Examples**:  
```nohighlight
> role add Test
Configuration file updated.

> role add Test
Role already added.

> role test Test
Please specify if I am adding or removing a role.

> role remove Test
Configuration file updated.
```

---

### update_channel_list
*command* **update_channel_list**(*ctx, add_or_remove, channel_id, member*)
> Update the configured channel list to add or remove a channel where the guild command can be used.  Command is 
executed via the `rolechannel` command.

* **Parameters**:  
    * **ctx**: discord.py Context object  
    * **add_or_remove** (str) [add, remove] - passed in string to determine if a channel is being added or removed  
    * **role_id** (str) - discord snowflake ID for the channel, requires the direct ID and cannot be added via pinging
    * **member** - optional discord.Member object
    
**Returns**: Nothing

**Examples**:  
```nohighlight
> rolechannel add 1234567890
Configuration file updated.

> rolechannel add 1234567890
Role already added.

> rolechannel test 1234567890
Please specify if I am adding or removing a channel.

> rolechannel remove 1234567890
Configuration file updated.
```