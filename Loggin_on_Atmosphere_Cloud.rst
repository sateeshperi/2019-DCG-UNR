**Logging onto Atmosphere Cloud**
=================================

For the duration of this workshop, we will be accessing data and tools
required to analyze our data on a remote computer using the **CyVerse's Atmosphere cloud**.

This is the first and last place in these lessons where it will matter if you are using PC, Mac, or Linux. After we connect, we will all be on
the same operating system/computing environment.

Below, we've provided screenshots of the whole process. You can click on them to zoom in. The important areas to fill in are highlighted.

First, go to the `Atmosphere <https://atmo.cyverse.org/application/images>`_ application and then click `login`

|atmo-1|

.. important::

  As descrbied in the `pre-workshop setup <https://upendrak.github.io/2018-06-05-noble>`_, you need to have access to the CyVerse Atmosphere Cloud. If you are not able to log-in for some reason, please let us know and we will fix it immediately.

1. Fill in the username and password and click "LOGIN"

- Fill in the username, which is your CyVerse username, and then enter the password (which is your CyVerse password).

|atmo-2|

2. Select the "Projects" tab and then click the "CREATE NEW PROJECT" button

- This is something you only need to do once.

- A project is a workspace that lets you keep things together.

- Click on the "Projects" tab on the top and then click the "CREATE NEW PROJECT" button

|atmo-3|

|atmo-4|

- Enter the name "Genomics" into the Project Name and put something simple like "Genomics" into the description. Then click "CREATE".

|atmo-5|

3. Select the newly created project

- Click on your newly created project.

- Click "NEW" and then "Instance" from the dropdown menu to start up a new virtual machine.

|atmo-7|

- Naviagate to "Show All tab and Search for "DC_Genomics"; click the "DC_Genomics_Noble_2018" image.

|atmo-8|

- Name your virtual machine something simple such as "workshop" or leave it as default which is the image name and select the following"

	-	Provider: "CyVerse Cloud - Marana" or "DC_Genomics_Noble"

	- 	Instance size: "medium3 (CPU: 4, Mem: 32GB, Disk: 240GB)"

	- 	Leave rest of the fields as default.

|atmo-9|

- Wait for it to become active

- It will now be booting up! This will take 2-5 minutes. Just wait! Don't reload or do anything.One the virtual machine is ready, the "Status" column will turn green and described as "Active" (see below)

|atmo-10|

- Click on your new instance's name to get more information!

- Now, you can either click "Open Web Shell", *or*, if you know how to use ssh, you can ssh in with your CyVerse username on the IP address of the machine

|atmo-11|

4. **Deleting your instance**

- To completely remove your instance, you can select the "Delete" button from the instance details page.

- This will open up a dialogue window. Select the "Yes, delete this instance" button.

- It may take Atmosphere a few minutes to process your request. The instance should disappear from the project when it has been successfully deleted.

|atmo-12|

.. Note::

  It is advisable to delete the machine if you are not planning to use it in future to save valuable resources. However if you want to use it in future, you can suspend it.


.. |atmo-1| image:: ./img/atmo-1.png
.. |atmo-2| image:: ./img/atmo-2.png
.. |atmo-3| image:: ./img/atmo-3.png
.. |atmo-4| image:: ./img/atmo-4.png
.. |atmo-5| image:: ./img/atmo-5.png
.. |atmo-6| image:: ./img/atmo-6.png
.. |atmo-7| image:: ./img/atmo-7.png
.. |atmo-8| image:: ./img/atmo-8.png
.. |atmo-9| image:: ./img/atmo-9.png
.. |atmo-10| image:: ./img/atmo-10.png
.. |atmo-11| image:: ./img/atmo-11.png
.. |atmo-12| image:: ./img/atmo-12.png

