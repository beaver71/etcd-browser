
# etcd browser

## Demo
[http://henszey.github.io/etcd-browser/](http://henszey.github.io/etcd-browser/)

## Screen Shot
![etcd-browser Screen Shot](http://henszey.github.io/etcd-browser/images/etcdbrowser.png)

## To build/run as a Docker container together with ETCD:

1. build etcd-browser image:

    docker-compose build
	
2. run etcd container (from quay.io/coreos/etcd image) and etcd-browser container (image built previously):
	
    docker-compose up -d

### Configuration
You can configure the builtin server using environment variables:

 * AUTH_USER: Username for http basic auth (skip to disable auth)
 * AUTH_PASS: Password for http basic auth
 * ETCD_HOST: IP of the etcd host the internal proxy should use [172.17.42.1]
 * ETCD_PORT: Port of the etcd daemon [4001]
 * SERVER_PORT: Port of builtin server
 
If you use a secured etcd:
 * ETCDCTL_CA_FILE
 * ETCDCTL_KEY_FILE
 * ETCDCTL_CERT_FILE