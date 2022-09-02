# noscan

`noscan` is a universal vulnerability scanner with deterministic 
results that works with any kind of artifact. 


## Usage

You can pipe files or give it a reference, it all works:

```
# Pipe files through the scanner:

cat virus.exe | ./scan.sh

# Scan a directory:

./scan.sh source/

# Scan a container image 

./scan.sh k8s.gcr.io/kube-proxy:v1.25.0

# Scan a website

./scan.sh https://openssf.org/

# Scan a postal address

./scan.sh One Apple Park Way Cupertino, CA 95014

```

## Security

There is nothing to worry about! We scanned noscan with itself to make
sure it's safe:

```
❯ ./scan.sh scan.sh
0 vulnerabilities found

```

`noscan` is super secure, it has an SBOM (Software Bill of Materials) 
[available in this repo](sbom.json.spdx), and it is also signed:

![digital signature](https://user-images.githubusercontent.com/3935899/188228827-80a188bb-6c9d-4488-9bde-bffa2a0edab6.png)


