# Ansible Playbook Repository

## To run on localhost targets.
Running on localhost targets require you to use `-K` and type in your sudo password.
Example: `ansible-playbook install-sublimetxt.yml -K`

## Creating new package installer playbook for Ubuntu.
Template found in [roles/ubuntu-install_template](roles/ubuntu-install_template)

Usage:
Modify the values in [roles/ubuntu-install_template/vars/main.yml](roles/ubuntu-install_template/vars/main.yml)

| Variable | Value description |
|----------|-------------------|
|direct_dl | The direct url from the manufacturer's website. To be used whenever possible.  |
|s3_dl     | The backup .deb package installer from S3.                                     |
|package   | The package name.                                                              |

Example:
`direct_dl: https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64`
`s3_dl: https://ubuntu-packages-erwyne.s3.ap-southeast-1.amazonaws.com/code_1.74.2-1671533413_amd64.deb`
`package: vscode_amd64.deb`