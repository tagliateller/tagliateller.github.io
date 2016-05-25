https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Installation_Guide/sect-atomic-virtualization-google.html

curl https://sdk.cloud.google.com | bash

source ~/.bashrc

gcloud auth login

gcloud config set project XXXX-YYYY

$ gcloud config set compute/zone europe-west1-b

[vagrant@localhost ~]$ gsutil mb gs://rhel-7_2-16-atomic-bucket
Creating gs://rhel-7_2-16-atomic-bucket/...
[vagrant@localhost ~]$

Abweichung zur Anleitung - Image ist nicht komprimiert ??

$ sudo yum -y install qemu-img

$ qemu-img convert -S 4096 -f qcow2 -O raw rhel-atomic-cloud-7.2-16.x86_64.qcow2 disk.raw

$ tar -Szcf rhel-atomic-cloud-7.2-16.x86_64.tar.gz disk.raw

$ gsutil cp rhel-atomic-cloud-7.2-16.x86_64.tar.gz gs://atomicbucket

$ gcloud compute instances create my-atomic-instance --machine-type n1-standard-1 --image rhel-7-2-16-atomic

