NodeJS S3 File Upload Example
=============================

Stream upload to S3 while downloading a file from a remote URL using [knox](https://github.com/LearnBoost/knox).

Running
-------

Install knox and express:

    npm install knox express

Add your S3 credentials:

    var client = knox.createClient({
        key: '<api-key-here>',
        secret: '<secret-here>',
        bucket: 'mybucket'
    });

Run the app:

		node app.js
		
Then in your browser replace src with the file you wish to upload to s3:
		
		http://localhost:3000/?src=http://www.example.com/file-to-download.txt