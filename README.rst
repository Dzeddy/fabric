|version| |python| |license| |ci| |coverage|

.. |version| image:: https://img.shields.io/pypi/v/fabric
    :target: https://pypi.org/project/fabric/
    :alt: PyPI - Package Version
.. |python| image:: https://img.shields.io/pypi/pyversions/fabric
    :target: https://pypi.org/project/fabric/
    :alt: PyPI - Python Version
.. |license| image:: https://img.shields.io/pypi/l/fabric
    :target: https://github.com/fabric/fabric/blob/main/LICENSE
    :alt: PyPI - License
.. |ci| image:: https://img.shields.io/circleci/build/github/fabric/fabric/main
    :target: https://app.circleci.com/pipelines/github/fabric/fabric
    :alt: CircleCI
.. |coverage| image:: https://img.shields.io/codecov/c/gh/fabric/fabric
    :target: https://app.codecov.io/gh/fabric/fabric
    :alt: Codecov

======
Fabric
======

Overview
========

Fabric is a high level Python (2.7, 3.4+) library designed to execute shell
commands remotely over SSH, yielding useful Python objects in return. It builds
on top of `Invoke <https://pyinvoke.org>`_ (subprocess command execution and
command-line features) and `Paramiko <https://paramiko.org>`_ (SSH protocol
implementation), extending their APIs to complement one another and provide
additional functionality.

Features
========

- Execute local and remote shell commands
- Streamlined file transfer operations
- Parallel execution of tasks across multiple hosts
- Prompt handling for interactive scripts
- Integration with local and remote Python environments

Installation
============

You can install Fabric using pip:

.. code-block:: bash

    pip install fabric

Quick Start
===========

Here's a simple example to get you started:

.. code-block:: python

    from fabric import Connection

    # Connect to a remote server
    c = Connection('user@host')

    # Run a command
    result = c.run('uname -s')
    print(f"OS: {result.stdout.strip()}")

    # Transfer a file
    c.put('local_file.txt', 'remote_file.txt')

Documentation
=============

For more detailed information, check out the `official Fabric documentation <http://docs.fabfile.org/>`_.

Use Cases
=========

- Automating deployment processes
- Executing maintenance tasks on remote servers
- Configuring multiple servers simultaneously
- Running database migrations
- Restarting services across multiple hosts

Contributing
============

Contributions to Fabric are welcome! Please refer to the project's GitHub repository for guidelines on how to contribute.

License
=======

Fabric is distributed under the BSD license. See the LICENSE file for more details.

Support
=======

If you encounter any issues or have questions, please file an issue on the `GitHub issue tracker <https://github.com/fabric/fabric/issues>`_.
