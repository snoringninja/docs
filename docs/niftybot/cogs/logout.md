# Logout

---

## Logout
*class* cogs.logout.Logout()  
Handles all logout functionality, depending on which platform the bot is running on.

---

### get_system_environment
*static* **get_system_environment()**  
>Check which platform the bot is running under.  

**Returns**: Nothing

---

### systemd_logout
*static* **systemd_logout**(*service_name*)  
>Attempt to stop the service that is running the bot so that the logout is successful and the
bot does not restart, which is something that can be configured when using systemd.  

* **Parameters**:
    * **service_name** (str) - systemd service name that the bot is running under  
    
**Returns**: Nothing
  
---

### logout
*command* **logout**(*ctx*)  

!!! important
    This function is designed to log the bot out depending on the environment in use.  It still 
    makes use of the logout functionality built right into discord.py, but with an extra step if using a linux 
    environment.  
    
    It is important to note that the systemd_logout functionality won't work if the user/group the bot is running under 
    requires authentication to run the following: systemctl stop SERVICENAME  
    
    **Please keep that in mind.**

* **Parameters**:
    * **ctx**: discord.py Context object  
  
**Returns**: Nothing