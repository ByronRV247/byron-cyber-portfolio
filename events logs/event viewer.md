In any Windows system, the Event Viewer, a Microsoft Management Console (MMC) snap-in, can be launched by simply right-clicking the Windows icon in the taskbar
and selecting Event Viewer . For the savvy sysadmins that use the CLI much of their day, Event Viewer can be launched by typing eventvwr.msc. It is a GUI-based 
application that allows you to interact quickly with and analyze logs.

Event Viewer has three panes.

The pane on the left provides a hierarchical tree listing of the event log providers.
The pane in the middle will display a general overview and summary of the events specific to a selected provider.
The pane on the right is the actions pane.

![Image](https://github.com/user-attachments/assets/6513fa9b-4bab-4317-aece-0074479dc4ed)

Within Properties, you see the log location, log size, and when it was created, modified, and last accessed. Within the Properties window, you can also see the maximum
set log size and what action to take once the criteria are met. This concept is known as log rotation. These are discussions held with corporations of various sizes.
How long does it take to keep logs, and when it's permissible to overwrite them with new data.

Lastly, notice the Clear Log button at the bottom right. There are legitimate reasons to use this button, such as during security maintenance, but adversaries will likely 
attempt to clear the logs to go undetected. Note: This is not the only method to remove the event logs for any given event provider.

![Image](https://github.com/user-attachments/assets/59088260-adfc-44be-b8d3-8ee8efc86a42)

use case finding the earliest log recorded by power shell operations 

![Image](https://github.com/user-attachments/assets/e8f08932-5b47-425b-af6b-0f3b051e7e37)

use case filtering to find a commands executed in a session 

![Image](https://github.com/user-attachments/assets/b904aed3-bcf1-4a52-bfda-0b99fe2b9e05)

list all logs with 4104 ID 

![Image](https://github.com/user-attachments/assets/2f6fa560-8250-47cb-a404-27d964a30ea9)

command executed in the second log session

![Image](https://github.com/user-attachments/assets/040a017a-55f6-4362-b3a3-338e79b5bd60)
