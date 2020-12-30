
SNMP simulation data
--------------------
[![PyPI](https://img.shields.io/pypi/v/snmpsim-data.svg?maxAge=2592000)](https://pypi.org/project/snmpsim-data/)
[![Python Versions](https://img.shields.io/pypi/pyversions/snmpsim-data.svg)](https://pypi.org/project/snmpsim-data/)
[![GitHub license](https://img.shields.io/badge/license-BSD-blue.svg)](https://raw.githubusercontent.com/inexio/snmpsim-data/master/LICENSE.txt)

The `snmpsim-data` package contains simulation data for
[snmpsim](http://snmplabs.thola.io/snmpsim) - free and open-source SNMP agent simulator.
The package is distributed under 2-clause
[BSD license](http://snmplabs.thola.io/snmpsim/license.html).

Why this fork?
--------------
[Original project](https://github.com/etingof/snmpsim-data) by [Ilya Etingof](https://github.com/etingof) seems not to be continued anymore.
Because of that, we try to maintain / enhance SNMP simulation data.

Download
--------

SNMP simulation data can be downloaded as a Python package from
[PyPI](https://pypi.org/project/snmpsim-data/).

Installation
------------

Just run:

```bash
$ pip install snmpsim-data
```

How to use simulation data
--------------------------

Invoke `snmpsimd.py` and point it to a directory with simulation data:

```
$ snmpsimd.py --data-dir=snmpsim-data/data --agent-udpv4-endpoint=127.0.0.1:1024
```

Simulation data is stored in simple plain-text files having `OID|TYPE|VALUE`
format:

```
$ cat public.snmprec
1.3.6.1.2.1.1.1.0|4|Linux 2.6.25.5-smp SMP Tue Jun 19 14:58:11 CDT 2007 i686
1.3.6.1.2.1.1.2.0|6|1.3.6.1.4.1.8072.3.2.10
1.3.6.1.2.1.1.3.0|67|233425120
1.3.6.1.2.1.2.2.1.6.2|4x|00127962f940
1.3.6.1.2.1.4.22.1.3.2.192.21.54.7|64x|c3dafe61
...
```

Simulator maps query parameters like SNMP community names, SNMPv3 contexts or
IP addresses onto data files paths relative to the `data` directory.

Documentation
-------------

Detailed information on SNMP simulator usage could be found at
[snmpsim site](http://snmplabs.thola.io/snmpsim/).

Getting help
------------

If you run into bad simulation data, feel free to
[open an issue](https://github.com/inexio/snmpsim-data/issues) on GitHub.

Contributions
-------------

If you have an SNMP-managed device, consider snmpwalk'ing it (or use `snmprec` tool
from `snmpsim` package) and submit a PR offering your data.

If you want to contact us, please mail to the [Thola Team](mailto:snmplabs@thola.io)

Copyright (c) 2019, [Ilya Etingof](mailto:etingof@gmail.com). All rights reserved.
