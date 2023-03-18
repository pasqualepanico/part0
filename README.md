# part0
	Excercice 0.6 - New note in Single page app diagram -
	
		sequenceDiagram
			partecipant browser
			partecipant server
			
			Note: When a new note is created by clicking the Save button, JavaScript makes a lot of work. There is a event handler or callback function that is associated to				the button for submitting a new form with data input to the server. The callback function prevents to raise a new GET request towards the server. A new        					variable is created with the name note, that contains two value: content and date. That var note is pushed into the array notes and is placed at the end of it.   			The input data is displayed into the browser by calling the function redrawNote() and the input data is sent to the server by the function sendToServer(notes)    			that has, as input parameter, the variable note. Now the browser makes a HTTP POST Request to the server where it lets the server know about the header in JSON 				format.
			
  			browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
  			activate server
  			server --> broswer: new note as JSON data with content and date
  			deactivate server
  
