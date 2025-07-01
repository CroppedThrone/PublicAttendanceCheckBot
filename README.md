# AttendanceCheckBot
A discord bot that checks attendances, mainly used for starwars servers! <br/>
invite the bot to your server today! <br/>

### Invite link with Admin Perms: (Recommended)
https://discord.com/oauth2/authorize?client_id=1358504555473539469&permissions=8&integration_type=0&scope=bot
### Invite link with Specific Perms: (Experimental)
https://discord.com/oauth2/authorize?client_id=1358504555473539469&permissions=2617583696&integration_type=0&scope=bot

## What can you do with this discord bot?
With this discord bot let a bot count attendances so you don't have to count it yourself. <br />
You can add your ranks, rank requirements, roles that will give people access to commands and so much more! <br />
You start off with 50 people max with 20 ranks max and if you want to upgrade to premium, you can have 500 people with 50 ranks! <br />
The bot also adds 3 roles: Name_Changer, Attendance_Creator & Attendance_Manager. If you want to know what each role can do check out the commands list! <br />

## Update 1.02
Updated the Readme. <br />

# Commands list
## ADMIN

### /settings_attendance_protocols (newprotocols: No attendance, Attendance with commands, Attendance with messages, Attendance with commands and messages)
With this command you can change how the user in your discord server interacts with attendance. They can use commands, messages or commands and messages. The default mode is: "Attendance with commands and messages". Don't forget to also setup your channel where users can use attendance!

### /settings_attendance_channel (channel: discord.TextChannel)
Use this command to select which text channel the discord bot should check for people typing in "i attended". This is also the channel that get's autocleaned if you have "/settings_auto_clear_attendances" set up.

### /settings_add_rank (newrank: str, position: int)
You can add a rank so you can use "/ordered_attendance_list". Position 0 is the highest rank. Position 20 is the lowest rank unless you have premium then it is 50. The rank of each person is based of, if they have the letters of the rank in their nickname.

### /settings_remove_rank (position: int)
Position 0 is the highest rank. Position 20 is the lowest rank unless you have premium then it is 50. The rank of each person is based of, if they have the letters of the rank in their nickname.

### /settings_auto_clear_attendances (auto_clear_protocol: Clear all messages, Clear all messages except admins, Only clear attendance messages, Don't clear messages)
When the user uses "/reset_attendance_list". You can automatically clear the attendance text channel when you also reset the attendance list. there are also 4 modes you can use: Clear all messages, Clear all messages except admins, Only clear attendance messages & Don't clear messages. The default mode is: "Don't clear messages".

### /settings_rankup_requirement (rank_position: int, attendances_to_reach: int)
Change the number of attendances needed to reach a rank. You can use /rank_list to see every rank and position of it so it easier to modify the rankuprequirement.

### /rank_list ()
View all ranks and it's requirements to rank up. To change ranks you can use "/settings_add_rank" or "/settings_add_rank". To change rank requirements use "/settings_rankup_requirement".

### /remove_user (member: discord.Member, nickname: str)
Removes a user from the attendance sheet so you have more room for other people in the sheet. You can remove users using their discord account that you can select while using the command. Or if the perosn that is in your group doesn't have a discord account but is registered in the attendance sheet. You can use "nickname" and fill in their nickname. You can only use one of these options in 1 command, not both.

### /reset_attendance_list (areyousure: bool, areyousure2: bool, areyousure3: bool)
Resets the attendance list by mkaing everyones attendance number go to 0. You have to put in 3x true, just to make sure you can't do it accidentally. Using this command will activate reset setttings protocols so check out if you're interested! "/settings_auto_clear_attendances".

### /settings_change_rolename
This setting is not available and may be removed in the future.

## Attendance_Manager

### /default_attendance_list (skipdates: bool = True)
Gives a list of troopers without order. This can be helpful for testing or if you don't want to set up a rank system with a rank requirement. If you want to see the date for each person his attendance, you can put "skipdates" to false.

### /ordered_attendance_list (checkrequirement: bool = False, allowdate: bool = False)
Gives a list of troopers in rank order and attendance. The rank order can be changed by using "/settings_add_rank" or "/settings_remove_rank". If you enable "checkRequirement" it will only show the people that can rank up based of the attendance they have and the rank up requirement you need. You can change the rank up requirement with "/settings_rankup_requirement". If you want to see the date for each person his attendance, you can put "allowdate" to true.

### /update_troopers_nicknames ()
Updates the nicknames of all troopers who have a discord account for the excel sheet. If people in the discord server forgot to use "/rename_user" and use discord's rename system instead of "/rename user". You can use this command to update it for every trooper and it will show you a list of every user that got updated. It will only update the nicknames in the excel sheet if the user has attended once.

### /create_forced_attendance (member: discord.Member, nickname: str)
This command is mainly used for non-discord users, that need to be registrated for the attendance sheet. And if they attended their training for the first time, then you can use "nickname" for them. If one of your discord members can't use their discord at the time. You can use this command aswell. You can only use one of these options in 1 command, not both.

### /increment_attendance (amount: int, member: discord.Member, username: str)
You can decrease or increase attendance of a user and by how much you increase or decrease depends on what you put in the "amount", TIP: don't let it go into -1 or less attendance XD. You can change the attendance numbers for discord users by using "member". And you can change it for non-discord users with "username". You can only use one of these options in 1 command, not both.

## Attendance_Creator

### /set_attendance_timer (hourstosignin: int, minutestosignin: int, secondstosignin: int))
Sets a timer for your users to collect their attendance. You can fill in the variables: "hourstosignin, minutestosignin, secondstosignin" to select how long you want attendance to be available for your users. if you do not set anything it will automatically be 1 hour and 30 minutes.

### /set_attendance_state (allowstate: bool)
With this command you can disable or enable your troopers from getting attendance. This is kind of a security command where if someone accidentally uses "/set_attendance_timer" while it's not meant to happen. Then you can set the "allowstate" to false to prevent people from gettign attendance. Using "/set_attendance_timer" after someone used "/set_attendance_state (allowstate: false)", will automatically set "allowstate" to true.

## Name_Changer

### /rename_user (newname: str, member: discord.Member, nickname: str)
Renames the username of a user. If you use the member variable, it will rename the user in the attendance sheet. But also rename the user in discord. If you use nickname it will only change the username in the attendance sheet. You can only use one of these options in 1 command, not both.

## Everyone

### /attendance
This commands checks if a user can get attendance. If "/set_attendance_timer" is activated the user can use this command to get the attendance. But this does depends what has been selected with the command: "/settings_attendance_protocols". If the settings: "Attendance with commands" or "Attendance with commands and messages" have been selected you can use the command. If the settings: "Attendance with messages" or "Attendance with commands and messages" have been selected you cannot use the command "/attendance" but will have to type in "i attended" in the correct discord channel. To setup the discord channel use "/settings_attendance_channel".

# UpdateLogs
## Update 1.01
You can now organise people with the /Give_Ordered_List by using "checkrequirement". This will allow you to only see the people who have enough attendances to rank up. <br />
You can now use the command: "/settings_auto_clear_attendances". <br />
The word "derp" is now removed o7. <br />

# Launch
Started development on 23-04-2025 <br />
It is made by yours truly, CroppedThrone :D <br />
