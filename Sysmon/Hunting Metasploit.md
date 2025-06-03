We will first be looking at a modified Ion-Security configuration to detect the creation of new network connections. 
The code snippet below will use event ID 3 along with the destination port to identify active connectionsspecifically
connections on port 4444 and 5555. 

<RuleGroup name="" groupRelation="or">
	<NetworkConnect onmatch="include">
		<DestinationPort condition="is">4444</DestinationPort>
		<DestinationPort condition="is">5555</DestinationPort>
	</NetworkConnect>
</RuleGroup>

(XML RULE )
Hunting for Open Ports with PowerShell

Get-WinEvent -Path <Path to Log> -FilterXPath '*/System/EventID=3 and */EventData/Data[@Name="DestinationPort"] and */EventData/Data=4444'

![Image](https://github.com/user-attachments/assets/da088b93-bb68-4049-9f35-944bff1f2c4d)

