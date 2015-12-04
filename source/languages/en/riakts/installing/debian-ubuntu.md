---
title: Installing on Debian and Ubuntu
project: riakts
version: 1.0.0+
document: tutorial
audience: beginner
keywords: [tutorial, installing, debian, ubuntu, linux]
download:
  key: debian
  name: "Debian or Ubuntu"
---

[AAE]: http://docs.basho.com/riak/2.1.1/theory/concepts/aae/
[riak security]: http://docs.basho.com/riak/2.1.1/ops/running/authz/
[configuring]: http://docs.basho.com/riakts/1.0.0/using/configuring

Riak TS can be installed on Debian- or Ubuntu-based systems using a binary
package available through ZenDesk.

Check your e-mail for the link to the download in ZenDesk.


##Dependencies

###PAM Library Requirement for Ubuntu **?? Does this apply to TS?**

You must have the `libpam0g-dev` package used for [Pluggable Authentication Module (PAM)][riak security] authentication in order to install Riak TS.

To install this dependency:

```bash
sudo apt-get install libpam0g-dev
```


##Install Riak TS
Once you have downloaded the package from ZenDesk, execute the following command to install Riak TS:

```bash
sudo dpkg -i riak-ts_{{VERSION}}-1_amd64.deb
```


##Turn off AAE
Once you've installed Riak TS, you must turn off [AAE][AAE]. To do this, edit riak.conf as follows:

```riak.conf
anti_entropy = passive
```


##Next Steps
Now that you've installed Riak TS, check out [Configuring Your Riak TS Table][configuring].