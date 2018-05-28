# Ansible role: AWS VPC

This role handles the creation of AWS S3 buckets

[![Build Status](https://travis-ci.org/Flaconi/ansible-role-aws-s3-bucket.svg?branch=master)](https://travis-ci.org/Flaconi/ansible-role-aws-s3-bucket)
[![Version](https://img.shields.io/github/tag/Flaconi/ansible-role-aws-s3-bucket.svg)](https://github.com/Flaconi/ansible-role-aws-s3-bucket/tags)
[![Ansible Galaxy](https://img.shields.io/ansible/role/d/25927.svg)](https://galaxy.ansible.com/Flaconi/aws-s3-bucket/)

## Requirements

* Ansible 2.5


## Additional variables

Additional variables that can be used (either as `host_vars`/`group_vars` or via command line args):

| Variable                    | Description                  |
|-----------------------------|------------------------------|
| `aws_s3_bucket_profile`     | Boto profile name to be used |
| `aws_bucket_default_region` | Default region to use        |
| `aws_bucket_default_policy` | Default policy to use        |


## Example definition

#### Required parameter only

```yml
aws_s3_buckets:
  - name: my-first-bucket
  - name: my-second-bucket
```
#### All available parameter
```yml
aws_s3_buckets:
  - name: my-first-bucket
    policy: '{}'
    versioning: True
    region: eu-central-1
    tags:
      - key: env
        val: development
      - key: department
        val: infra
  - name: my-second-bucket
    policy: '{}'
    versioning: True
    region: eu-central-1
    tags:
      - key: env
        val: development
      - key: department
        val: infra
```
