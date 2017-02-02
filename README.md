# Amazon S3 Signed Request with STS

This package enables you to create signed requests with STS to Amazon
S3 for uploading files.  [AWS Signature Version
4](http://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html)
is the recommended approach to create signed requests.  The signature
can be created using your access keys (access key ID, secret access
key).  The Amazon [Security Token
Service](http://docs.aws.amazon.com/STS/latest/APIReference/Welcome.html)
(STS) provides temporary security credentials.  This package use the
credentials created using STS to sign request.

In fact, this package doesn't make the actual request.  This package
creates all the values required to make signed request.  Application
authors can use this library and send the values produced here to the
authenticated users.  The client (web or mobile application) can get
these values and make the actual request.

Regular auditing of S3 logs and event notification through SNS can be
used to improve the security.  Object versioning also will help to
mitigate spam issues.

This code is derived from [Tommy Back's
work](https://github.com/murrekatt/go-s3presigned-post).

This program is licensed under *The MIT License*.  See the LICENSE
file for the license text.
