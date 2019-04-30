coyim-port
==========

FreeBSD Ports script for CoyIM.

You can find CoyIM [here][1]

NOTE: This port is not yet available in the FreeBSD Ports tree.

Installation
------------

Copy `net-im/coyim` folder to `/usr/ports` directory.

NOTE: If your ports directory is different from above, copy to the respective
place.

Usage
-----

Once you have copied the folder, install it as you would do for any port.

`$ cd /usr/ports/net-im/coyim`<br>
`$ make install clean`

For a list of dependencies for the build check [here][2]

Credits
-------

* The CoyIM is developed and maintained by the [CoyIM Team][3]
* Thanks to `@ppaeps` for a machine to do and test the port development and
  testing out / fixing the port.
* Thanks to `@claucece` for improving the documentation and providing a proper
  `MAINTAINER` mail.
* Thanks to `@rarguello` for minor bug fixes.  
* This work has been partially sponsored by [CAD][4]

License
-------

BSD 2-clause. See LICENSE.

[1]: https://coy.im/
[2]: https://github.com/coyim/coyim
[3]: https://github.com/orgs/coyim/people
[4]: https://autonomia.digital/
