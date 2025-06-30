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

## Update 0.11
You can now organise people with the /Give_Ordered_List by using "checkrequirement". This will allow you to only see the people who have enough attendances to rank up.
You can now use the command: /settings_auto_clear_attendances

## Commands list (needs to update)
Every settings command can only be accessed by people with admin permissions.

### /ordered_attendance_list (checkrequirement: bool = False, allowdate: bool = False)
Gives a list of troopers in rank order and attendance. The rank order can be changed by using "/settings_add_rank" or /settings_remove_rank.

### /settings_add_rank (newrank: str, position: int)
You can add a rank so you can use "/ordered_attendance_list". Position 0 is the highest rank. Position 20 is the lowest rank unless you have premium then it is 50. The rank of each person is based of, if they have the letters of the rank in their nickname.

### /settings_remove_rank (position: int)
Position 0 is the highest rank. Position 20 is the lowest rank unless you have premium then it is 50. The rank of each person is based of, if they have the letters of the rank in their nickname.

### /settings_auto_clear_attendances: 
When the user uses "/reset_attendance_list". You can automatically clear the attendance text channel when you also reset the attendance list. there are also 4 modes you can use: Clear all messages, Clear all messages except admins, Only clear attendance messages & Don't clear messages. Don't clear messages is the default.

### /settings_rankup_requirement (rank_position: int, attendances_to_reach: int)
Change the number of attendances needed to reach a rank. You can use /rank_list to see every rank and position of it so it easier to modify the rankuprequirement.


## Launch
Started development on 23-04-2025
