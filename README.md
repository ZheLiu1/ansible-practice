## Team info

|Name           |NUID     |
|---------------|---------|
|Yunlu Liaozheng|001470321|
|Feng Huang     |001230993|
|Zhichao Pan    |001493794|
|Zhe Liu        |001475826|

## Instruction

### Preparation

* Create a key pair on AWS.
* Add ssh port(22) to in-bound rules.
* export AWS_ACCESS_KEY_ID='XXX';export AWS_SECRET_ACCESS_KEY='XXX'

### `launch-web-server.yaml`

Use `ansible-playbook launch-web-server.yaml --private-key path/key.pem`.

You will need to provide the keypair name.

The `exact_count` parameter will ensure that there is only one instance, so it is idempotent.

### `terminate-web-server.yaml`

Use `ansible-playbook terminate-web-server.yaml`.

You will need to provide the key and value of the tag.
