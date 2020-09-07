# read12

The only thing displayed to the user is the URL called. As we mentioned above, with a GET request the user will see the data in their URL bar, but with a POST request they won't. This can be very important for two reasons:

- If you need to send a password (or any other sensitive piece of data), never use the GET method or you risk displaying it in the URL bar, which would be very insecure.
- If you need to send a large amount of data, the POST method is preferred because some browsers limit the sizes of URLs. In addition, many servers limit the length of URLs they accept.


If you want to send files, you need to take three extra steps:

- Set the method attribute to POST because file content can't be put inside URL parameters.
- Set the value of enctype to multipart/form-data because the data will be split into multiple parts, one for each file plus one for the text data included in the form body (if text is also entered into the form).
- Include one or more input type="file" controls to allow your users to select the file(s) that will be uploaded.