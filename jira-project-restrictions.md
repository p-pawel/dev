# Restrict JIRA users to single projects

This is based on the answer from StackOverflow http://stackoverflow.com/a/27955264/2045440. It was so hard to find an instruction clear enough, that just in case I quote the full core of that answer here.

> **1) Create a new group (restricted to project xyz group).**
>
> - Click User management in top right (click the cog icon) > login as Administrator > click Groups (left menu)
> - Add group, self explanatory > Name = restricted to xyz group (or whatever you like)

> **2) Create a new permission scheme (Restricted to Project XYZ permission scheme)**
> 
>  - From Administration area > Click Issues > Permission Schemes
>  - Copy the default scheme as the guide says, > Click "copy" next to "Default Permission Scheme".
>  - Now this part takes some time. I deleted every single permission, then clicked "add" next to the below items.
>  - add > Click "Group" Radio Button > select your group "restricted to project xyz group" etc
>  - ***Hint***: I middle mouse clicked each item open all at once, first to delete, then to add. Makes it less tedious.
> 
> - Here are the items I Assigned to my group:
>   - Project Permissions 
>     - Browse Project
>   - Issue permissions
>     - *everything*
>   - Comments Permissions 
>     - Add Comments
>     -  Delete Own Comments
>     -  Edit Own Comments
>   - Time Tracking permissions
>     - Delete Own Worklogs
>     - Edit Own Worklogs
>     - Work On Issues
> 
>
> **3) Link the permission scheme with project XYZ**
> - Click Projects > Select your Project (project XYZ) > Click "Administration" at top of screen (Next to overview) > Click Permissions (left menu) > Click Actions > Select Use a Different Scheme
>
> **4) Grant the Global Permission "JIRA users" to the group "restricted to project xyz group" so they will be able to log in.**
> 
> - Go back to Administration area > Click Cog top right > Click System > Click Global Permissions (left menu)
> - Add Permission > Select Permission = JIRA Users, select Group = restricted to project xyz group (etc)
> - After this you should see your group appear next to "JIRA Users" just click View users, then invite/add the users as appropriate with your group selected.
