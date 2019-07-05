## Example Server (channel) Configuration File
In case you may have generated your channel configuration file before a change to the config generator, 
this is here to help you match yours up, ensuring that all sections exist. Below is how the file would be generated the 
first time you run the ``genconfig`` command as the server owner.

---


[ServerSettings]  
owner_id = your_discord_user_id  
server_id = discord_server_id  
  
[BotAdmins]  
bot_admin_users = NOT_SET  
bot_admin_roles = NOT_SET  
  
[ConfigSettings]  
not_accepted_channel_id = NOT_SET  
  
[RoleAssignment]  
role_list = NOT_SET  
enabled = False  
assignment_channel_id = NOT_SET  
  
[JoinPart]  
welcome_channel_id = NOT_SET  
member_join_enabled = False  
leave_channel_id = NOT_SET  
member_part_enabled = False  
welcome_message = Welcome to {server}\'s Discord, {user}! Relax and have some fun! {emote}  
part_message = {name} ({display_name}) has left the server.  
assign_role_enabled = false
role_assignment_id = NOT_SET
  
[BettingGame]  
bet_channel_id = NOT_SET  
minimum_bet = NOT_SET  
enabled = False  
helpme_cooldown = 86400  
helpme_minimum = 500  
helpme_bonus = 100  
  
[ApiCommands]  
enabled = False  
api_channel_id = NOT_SET
