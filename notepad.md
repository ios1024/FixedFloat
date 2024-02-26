https://dhenandi.com/easy-ways-to-transfer-your-file-to-file-io/
All files are encrypted when stored on our servers.
Or, if you are on CLI mode, you also can upload your file to file.io with this command:

$ curl -F "file=@/your/folder/file.txt" https://file.io
{"success":true,"key":"2ojE41","link":"https://file.io/2ojE41","expiry":"14 days"}
$ curl https://file.io/2ojE41
This is a test
$ curl https://file.io/2ojE41
{"success":false,"error":404,"message":"Not Found"}
