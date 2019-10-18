# part0
ExercisesPart0FullStackOpen2019

# 0.4: new note
Create a similar diagram depicting the situation where the user creates a new note on page https://fullstack-exampleapp.herokuapp.com/notes by writing something into the text field and clicking the submit button.

browser->server: HTTP POST https://fullstack-exampleapp.herokuapp.com/new_note
server-->browser: HTTP status code 302
note over browser:
This is a URL redirect, with which server asks browser 
to do a new HTTP GET request to the address defined
in the header's Location - the address notes
end note
browser->server: HTTP GET https://fullstack-exampleapp.herokuapp.com/notes
server-->browser: HTTP status code 200 OK (HTML-code of page)
browser->server: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.css
server-->browser: HTTP status code 200 OK (main.css)
browser->server: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.js
server-->browser: HTTP status code 200 OK (main.js)

note over browser:
browser starts executing js-code
that requests JSON data from server 
end note

browser->server: HTTP GET https://fullstack-exampleapp.herokuapp.com/data.json
server-->browser: [..., {content: "note for 0.4", date: "2019-10-18T17:43:09.440Z"}]

note over browser:
browser executes the event handler
that renders notes to display
end note

Created this repository for submission of part0 exercises. Thanks
