# Openshift NGINX plus all

## NGINX

Nginx official image does not run in Openshift. We need to:

 * Change the group of some folders to root and give write permissions to it
 * Change the port to 8081
 * Disable the user directive

In order to improve the performance, the number of connections per process is increased by 10.

## All

The idea is to add to nginx:plus all clients needed to do tests from a pod
