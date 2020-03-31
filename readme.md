ntlm.js
======
Javascript implementation of Microsoft NTLM authentication over HTTP. Gives you the possibility to do that AJAX NTLM
you've always wanted.

Usage
------
    Ntlm.setCredentials('domain', 'username', 'password');
    var url = 'http://myserver.com/secret.txt';

    if (Ntlm.authenticate(url)) {
        var request = new XMLHttpRequest();
        request.open('GET', url, false);
        request.send(null);
        console.log(request.responseText);
        // => My super secret message stored on server.
    }

Setup
------
On the server side, the following CORS HTTP Response headers are required:
* Access-Control-Allow-Headers: Authorization
* Access-Control-Allow-Methods: GET, OPTIONS
* Access-Control-Allow-Origin: *
* Access-Control-Expose-Headers: WWW-Authenticate



