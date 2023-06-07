# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
'''

from http.server import HTTPServer,BaseHTTPRequestHandler

content='''

<!doctype html>
<title> My Web Server</title> 

## LANGUAGES USED IN WEB DEVELOPMENT:
## 1.HTML
## 2.CSS
## 3.Javascript
## 4.Bootstrap
'''

class MyServer(BaseHTTPRequestHandler):

def do_GET(self):
    print("Get request received...")
    self.send_response(200) 
    self.send_header("content-type", "text/html")       
    self.end_headers()
    self.wfile.write(content.encode())

print("This is my webserver")

server_address =('',8000)

httpd = HTTPServer(server_address,MyServer)

httpd.serve_forever() '''
## OUTPUT:
![Screenshot (1)](https://user-images.githubusercontent.com/122986499/230133678-b0dfee95-9d82-468c-9a2f-abceee50ddc5.png)


## RESULT:

The program is executed succesfully
