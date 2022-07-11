# Secret Scanner
## The Problem
People will sometimes commit secrets to a GitHub repository

## How it works
Uses `Yelp/detect-secrets` to look for newly committed secrets. If it finds any potential secrets, it will:
* Fail
* Create a Job Summary with a list of the potential secrets found, and some advice on how to deal with the issue
* Provide an updated secrets baseline that contains the newly added secrets. This is useful if secrets that were discovered are not actually secrets.

## Inputs
|Input|Description|Required|default value|
|-----|-----------|--------|-------------|
|detect-secrets-version|The version of Yelp/detect-secrets to use|no|1.2.0|
|baseline-file|A path to the baseline secrets file|no|.secrets.baseline|
