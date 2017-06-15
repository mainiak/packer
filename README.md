# Packer configurations

## Usage

- [Download](https://www.packer.io/downloads.html) and install **Packer v1.0.0** or later.
- [Download](https://www.virtualbox.org/wiki/Downloads) and install **Virtualbox**.
- Follow code examples bellow.

### Ubuntu 16.04 LTS (Xenial Xerus)

#### Usage

File `ubuntu-16.04.json` produces [Vagrant](https://www.vagrantup.com/) box with Virtualbox [builder](https://www.packer.io/docs/builders/index.html).

```bash
packer validate ubuntu-16.04.json
packer build ubuntu-16.04.json

# Test VM
cd tmp
vagrant init ../builds/virtualbox-ubuntu1604.box
vagrant up

# Play with VM
vagrant halt
vagrant destroy

# Add box
vagrant box add ubuntu1604 ../builds/virtualbox-ubuntu1604.box
```

#### Notes

* Vagrant mount might fail - which is not important to might use case.
* Password for vagrant user and root user is vagrant - **THIS VIRTUAL MACHINE IS FOR DEVELOPMENT PURPOSE ONLY, USE AT YOUR OWN RISK**. Or take your own security measures.

## License

   Copyright 2017 Jakub Vitak

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
