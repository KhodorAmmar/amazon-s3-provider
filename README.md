Sitefinity's Amazon S3 Blob Storage Provider
===================================================

Sitefinity's Amazon S3 Blob Storage Provider is an implementation of a cloud blob storage provider, which stores the binary blob data of Sitefinity's library items on Amazon's Simple Storage Service (S3). This document describes how to use the provider.

Note that only the binary data of the items in a library are stored on the remote blob storage. Sitefinity still manages its logical items by library with their regular meta-data properties (title, description etc) in its own database.

Deployment steps:

* Copy the project dll and amazon dll to your bin folder
* Go to Sitefinity/Settings/Advanced/Library/Blob Sotrage/Providers
* Add a new provider and call it Amazon (for brevity), provider type should be
 `Telerik.Sitefinity.Amazon.BlobStorage.AmazonBlobStorageProvider, Telerik.Sitefinity.Amazon`
* Add 5 parameters
	* accessKeyId: Amazon access key id
	* secretKey: Amazon secret key
	* bucketName: Bucket name
	* regionEndpoint: for example: EUCentral1
	* cloudFrontUrl [Optional]: If you're serving the data from cloudfront
* Now you have the option to move libraries to amazon storage