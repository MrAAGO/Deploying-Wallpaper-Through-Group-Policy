# Deploying-Wallpaper-Through-Group-Policy

![screenshot-www google com-2022 12 24-12_26_40](https://user-images.githubusercontent.com/86381942/209515617-58079ac0-bb4f-463a-b9a7-f91102800bf4.png)



Before we begin, it's important to note that Group Policy is a feature of the Windows operating system that allows administrators to set policies for groups of users or computers in a domain. This means that in order to use Group Policy to deploy wallpaper to a PC, you'll need to have administrative privileges on the domain and access to the Group Policy Management Console.

With that said, let's get started!

Step 1: Open the Group Policy Management Console

![1](https://user-images.githubusercontent.com/86381942/209515413-b82cebca-a84c-447d-8728-ed1095d687aa.png)


To open the Group Policy Management Console, click the Start button and search for "Group Policy Management." Click on the "Edit Group Policy" option to open the console.

Step 2: Create a new Group Policy Object (GPO)

![2](https://user-images.githubusercontent.com/86381942/209515425-65e1d42a-b8e5-4265-a857-bdde90f7f01a.png)


In the Group Policy Management Console, right-click on the "Group Policy Objects" folder and select "New." This will create a new GPO, which you can then name and link to a specific organizational unit (OU) in your domain.

Step 3: Edit the GPO

![3](https://user-images.githubusercontent.com/86381942/209515451-8783fb24-2e82-4b8c-a4b0-003d3b9dc15c.png)


With the new GPO selected, click the "Edit" button to open the GPO editor. In the editor, navigate to the following path:

![10](https://user-images.githubusercontent.com/86381942/209515491-c0970733-8ac7-465b-9897-78d98d05c9c7.png)


User Configuration > Policies > Administrative Templates > Desktop > Desktop

![12](https://user-images.githubusercontent.com/86381942/209515499-4860263c-c8f4-417f-aa48-96fcd5563826.png)


In this folder, you'll find a setting called "Desktop Wallpaper." Double-click on this setting to edit it.

Step 4: Configure the wallpaper setting

![13](https://user-images.githubusercontent.com/86381942/209515515-23bf07d6-a867-49ef-94fe-3a1a20e8ccaa.png)


In the "Desktop Wallpaper" setting, select the "Enabled" option and enter the path to the wallpaper image that you want to use. You can use a local path or a network path to the image.

![14](https://user-images.githubusercontent.com/86381942/209515522-3bd3771e-4335-4b66-adf3-f0a6288955aa.png)


Step 5: Link the GPO to the OU

![18](https://user-images.githubusercontent.com/86381942/209515548-050a45ae-a67f-4bca-b305-87e8c8dddea0.png)

![19](https://user-images.githubusercontent.com/86381942/209515555-f2a142df-0010-4b5d-af78-229f53979a29.png)



After configuring the wallpaper setting, you'll need to link the GPO to the OU where you want the wallpaper to be applied. To do this, right-click on the OU and select "Link an Existing GPO." Select the GPO that you created in Step 2 and click "OK."

Step 6: Refresh Group Policy on the client computers

Finally, you'll need to refresh Group Policy on the client computers to apply the new wallpaper setting. To do this, open a command prompt on the client computer and type the following command:

gpupdate /force

![15](https://user-images.githubusercontent.com/86381942/209515569-2108c5a0-d225-401e-a8b4-8062657d1e18.png)


This will refresh Group Policy and apply the new wallpaper setting to the client computer.

And that's it! By following these steps, you should now be able to deploy wallpaper to a PC through Group Policy. With this method, you can easily change the wallpaper for multiple computers at once, saving you time and effort.

![17](https://user-images.githubusercontent.com/86381942/209515590-2c759aae-636d-49b8-80c1-ecd643c2831e.png)

