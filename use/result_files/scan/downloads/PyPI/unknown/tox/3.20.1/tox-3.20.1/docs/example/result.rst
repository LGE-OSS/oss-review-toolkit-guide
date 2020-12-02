Writing a JSON result file
--------------------------------------------------------

.. versionadded: 1.6

You can instruct tox to write a json-report file via:

.. code-block:: shell


    tox --result-json=PATH

This will create a json-formatted result file using this schema:

.. code-block:: json

    {
      "testenvs": {
        "py27": {
          "python": {
            "executable": "/home/hpk/p/tox/.tox/py27/bin/python",
            "version": "2.7.3 (default, Aug  1 2012, 05:14:39) \n[GCC 4.6.3]",
            "version_info": [ 2, 7, 3, "final", 0 ]
          },
          "test": [
            {
              "output": "...",
              "command": [
                "/home/hpk/p/tox/.tox/py27/bin/pytest",
                "--instafail",
                "--junitxml=/home/hpk/p/tox/.tox/py27/log/junit-py27.xml",
                "tests/test_config.py"
              ],
              "retcode": "0"
            }
          ],
          "setup": []
        }
      },
      "platform": "linux2",
      "installpkg": {
        "basename": "tox-1.6.0.dev1.zip",
        "sha256": "b6982dde5789a167c4c35af0d34ef72176d0575955f5331ad04aee9f23af4326"
      },
      "toxversion": "1.6.0.dev1",
      "reportversion": "1"
    }
