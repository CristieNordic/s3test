# s3test
Python Tools for Cloudian and IBM Cloud Object Storage S3 interface

## Pre-reqs
Make sure you running a virtualenv, Python3 and git on your machine.

### Installation
Clone this s3test project to your local machine.
`git clone https://github.com/CristieNordic/s3test.git`

Create and activate your virtual environment in the s3test directory.
```
cd s3test
virtualenv . -p python3
source bin/activate
```

Install all requirement to run the python code.
`pip install -r requirement.txt`


## Upload and Download Files
Upload file to a Bucket

```
$ python s3.py --access-key <my-access-key> --secret_key <my-secret-key> --url <s3 url> --bucket <bucket name> --upload --filename my_file.txt
```

 Download file from a bucket
 ```
 $ python s3.py --access-key <my-access-key> --secret_key <my-secret-key> --url <s3 url> --bucket <bucket name> --download --filename my_file.txt
 ```

### Using Config file

If you don't want to specify your credentials, url or bucket everytime you can add that information to the `config.py` file.

## Help Menu

```
python s3.py --help
usage: s3.py [-h] [--access-key ACCESS_KEY] [--secret-key SECRET_KEY]
            [--bucket BUCKET] [--upload | --download] [--dir DIR]
            [--filename FILENAME]

Upload and download files from the FYNB server

optional arguments:
 -h, --help            show this help message and exit
 --access-key ACCESS_KEY
                       Your access key
 --secret-key SECRET_KEY
                       Your secret key
 --bucket BUCKET       The bucket name.
 --upload
 --download
 --delete
 --commMethod COMMMETHOD
                       Change this value if not https, by typing
                       --commMethod=http
 --url URL              The URL to the COS e.g. s3.company.com
 --remote REMOTE, -D REMOTE
                       Remote directory at the S3 Storage
 --local LOCAL, -d LOCAL
                       Local directory on your host
 --filename FILENAME   The filename to upload or download
Contact support@cristie.se
```
