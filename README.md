# popup

Index.js uses nodejs and express framework. 

The "click here for sample report" button stays on the side of the page.

Clicking it makes the form appear; when the client fills and sends it, there is a timeout of 700ms to facilitate the sending of data to the server.

Socket.io is used to emit the data to the server. 
The data recieved by the server has it's date changed and is uploaded to the database on aws rds.

By the time the data is recieved by the server(700ms)(I hope), the client sends a GET request by opening a new tab and url.

This calls the puppeteer function and it uses the data, generates and send the pdf to the new tab.
This function also uses SMTP protocol to send the generated pdf to the email submitted by the client.
