## Create package
python setup.py sdist

### That will create package in
dist/package1-0.1.tar.gz

### Install Server
pip install pypiserver

### Host Repo
pypi-server -p 8080 ~/packages

### Install package from local repo
pip install --extra-index-url http://localhost:8080/simple package1

### Upgrade package
pip install ... -U

### Add pip.conf to store extra-index-url
touch ~/.pip/pip.conf

#pip.conf
[global]
extra-index-url = http://localhost:8080/simple

#to run
import package1
package1.function1()