# AttendanceCheckBot
A discord bot that checks attendances, mainly used for starwars servers!
invite the bot to your server today!

### Admin Perms: (Recommended)
https://discord.com/oauth2/authorize?client_id=1358504555473539469&permissions=8&integration_type=0&scope=bot
### Specific Perms: (Experimental)
https://discord.com/oauth2/authorize?client_id=1358504555473539469&permissions=2617583696&integration_type=0&scope=bot

## What can you do with this discord bot?
With this discord bot let a bot count attendances so you don't have to count it yourself.
You can add your ranks, rank requirements, roles that will give people access to commands and so much more!
You start off with 50 people max with 20 ranks max and if you want to upgrade to premium, you can have 500 people with 50 ranks!

## Update 1.01
You can now organise people with the /Give_Ordered_List by using "checkrequirement". This will allow you to only see the people who have enough attendances to rank up.
You can now use the command: "/settings_auto_clear_attendances"

## Commands list (needs to update)
Every settings command can only be accessed by people with admin permissions.

## ADMIN

### settings_attendance_protocols (newprotocols: No attendance, Attendance with commands, Attendance with messages, Attendance with commands and messages)
With this command you can change how the user in your discord server interacts with attendance. They can use commands, messages or commands and messages. The default mode is: "Attendance with commands and messages". Don't forget to also setup your channel where users can use attendance!

### /settings_add_rank (newrank: str, position: int)
You can add a rank so you can use "/ordered_attendance_list". Position 0 is the highest rank. Position 20 is the lowest rank unless you have premium then it is 50. The rank of each person is based of, if they have the letters of the rank in their nickname.

### /settings_remove_rank (position: int)
Position 0 is the highest rank. Position 20 is the lowest rank unless you have premium then it is 50. The rank of each person is based of, if they have the letters of the rank in their nickname.

### /settings_auto_clear_attendances (auto_clear_protocol: Clear all messages, Clear all messages except admins, Only clear attendance messages, Don't clear messages)
When the user uses "/reset_attendance_list". You can automatically clear the attendance text channel when you also reset the attendance list. there are also 4 modes you can use: Clear all messages, Clear all messages except admins, Only clear attendance messages & Don't clear messages. The default mode is: "Don't clear messages".

### /settings_rankup_requirement (rank_position: int, attendances_to_reach: int)
Change the number of attendances needed to reach a rank. You can use /rank_list to see every rank and position of it so it easier to modify the rankuprequirement.

### /rank_list ()
View all ranks and it's requirements to rank up. To change ranks you can use "/settings_add_rank" or "/settings_add_rank". To change rank requirements use "/settings_rankup_requirement.\

### /remove_user (member: discord.Member, nickname: str)

## Attendance_Manager

### /default_attendance_list (skipdates: bool = True)
Gives a list of troopers without order. This can be helpful for testing or if you don't want to set up a rank system with a rank requirement. If you want to see the date for each person his attendance, you can put "skipdates" to false.

### /ordered_attendance_list (checkrequirement: bool = False, allowdate: bool = False)
Gives a list of troopers in rank order and attendance. The rank order can be changed by using "/settings_add_rank" or "/settings_remove_rank". If you enable "checkRequirement" it will only show the people that can rank up based of the attendance they have and the rank up requirement you need. You can change the rank up requirement with "/settings_rankup_requirement". If you want to see the date for each person his attendance, you can put "allowdate" to true.

### /update_troopers_nicknames ()
Updates the nicknames of all troopers who have a discord account for the excel sheet. If people in the discord server forgot to use "/rename_user" and use discord's rename system instead of "/rename user". You can use this command to update it for every trooper and it will show you a list of every user that got updated. It will only update the nicknames in the excel sheet if the user has attended once.

## Name_Changer

### /rename_user

## Launch
Started development on 23-04-2025
It is made by yours truly, CroppedThrone :D
