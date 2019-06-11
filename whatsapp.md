
Feature: Send messages

	Given tap in the <element>
	When make one <action> and conecction is <signal>
	Then message is sending 
	And status icon is showed how <status>

	Background: 
		Given app is open 
		And one contact is select for send a message

	Scenario: Intermittent connection	

	|element 		|action									|signal	|status	|
	|text bar       |write a message and tap intro			|off	|oclock	|
	|text bar       |write a message and tap intro			|on		|check	|
	|mic bottom bar |send a voice message and release mic 	|off	|oclock	|
	|mic bottom bar |send a voice message and release mic 	|on		|check	|
	|camera			|take a picture and send 			 	|off	|oclock	|
	|camera			|take a picture and send 			 	|on		|check	|
	|galery			|select a picture and send 			 	|off	|oclock	|
	|galery			|select a picture and send 			 	|on		|check	|
	|galery			|select a video and send 			 	|off	|oclock	|
	|galery			|select a video and send 			 	|on		|check	|
	|document		|select a document and send 			|off	|oclock	|
	|document		|select a document and send 			|on		|check	|
	|location		|select a location and send 			|off	|oclock	|
	|location		|select a location and send 			|on		|check	|
	|contact		|select a contact and send 			 	|off	|oclock	|
	|contact		|select a contact and send 			 	|on		|check	|
	|gift			|select a gift and send 				|off	|oclock	|
	|gift			|select a gift and send 				|on		|check	|	
	|emoticon		|select a emoticon and send 			|off	|oclock	|
	|emoticon		|select a emoticon and send 			|on		|check	|


Feature: Calls 

	Given tap in the <element>
	When make one <action>
	Then <status> is showed
	And the conecction is <signal>

	Background: 
		Given app is open 
		And one contact is select for send a message

	Scenario: Intermittent connection	

	|element 		|action				|signal	|status				|
	|camera			|make video call	|off 	|error message		|
	|camera			|make video call	|on 	|call in progress	|
	|telephone		|make audio call	|off	|error message		|
	|telephone		|make audio call	|on		|call in progress	|

#First I thought to create a scenario for each state of the connection but it is more visual to group it in a table because the data is the same.
#It could still be optimized by leaving the data in an external file and execute the test with the change of connection status





