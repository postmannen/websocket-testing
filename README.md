# websocket-testing

Test loading templates, and send them to be drawn via websocket to the browser. The element that is made in the browser can then be deleted on the fly without reloading the page.
The templates are being parsed normally but instead of executing the template to http.ResponseWriter, we execute it to a bytes.Buffer which got a io.Writer,
and we then send that buffer over the websocket.
