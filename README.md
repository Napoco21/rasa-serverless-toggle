# Endpoints interfacing with RASA EC2 Server

```bash
Only for turning on my ec2 Server using some AWS lambda functions

```

# Endpoints:

POST - https://< URL >/dev/rasa/toggle

Body for POST:
```
{
    "toggle": "ON" | "OFF"
}
```


GET - https://< URL >/dev/rasa/status
# Installation

`> npm install serverless`

`> pip install -r requirements.txt`


Set up an AWS IAM serverless-admin with Admin privileges

`> aws configure`

Use your key and secret credentials; Find your proper region in aws console (default us-east-1); Last section set to json


# Installation of python packages on lambda
[serverless packaging](https://serverless.com/blog/serverless-python-packaging/)

`npm install --save-dev serverless-python-requirements`

# Activate python virtualenv
`virtualenv -p python3 env`

`source env/bin/activate`

### Deploy
`serverless deploy function --function <function name>`
Once you deploy you will get endpoint

### Debug
`serverless logs -f <function name> -t`