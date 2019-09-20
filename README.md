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
* Set `ec2_access_key` and `ec2_secret_key` in `vars/ec2.yaml`

### `launch-web-server.yaml`

Use `ansible-playbook -i hosts.ini launch-web-server.yaml`.

You can change the private key for remote server based on your key pair in `ansible.cfg` file.

The `exact_count` parameter will ensure that there is only one instance, so it is idempotent.

### `terminate-web-server.yaml`

Use `ansible-playbook -i hosts.ini terminate-web-server.yaml`.

You will need to provide the key and value of the tag.
