# aws-env

## Usage

    Set environment variables for AWS based on profile

    OPTIONS:
      -p --profile      choose a profile (default: default)
      -c --credentials  path to credential file (default: ~/.aws/credentials)
      -l --list         list available profiles
      -h --help         shows this help

## Credentials file

Your AWS Credentials file should adhere to the standard AWS format:

    [profile-name]
    aws_access_key_id = XXXXXXXXXX
    aws_secret_access_key = XXXXXXXXXXXXXXXXXXXX

Arbitrary environment variables may also be included under a given profile. 
The variable names wil be automatically converted to uppercase. e.g.:

    foo = bar

Will evaluate as:

    export FOO=bar

In addition to the environment variables defined for a given profile, the variable
`AWS_DEFAULT_PROFILE` will be exported with the selected profile name as its value.
