=======
TAC ETL
=======

This project documents the process of ETL for the data consumed by TAC modules

The full documentation is hosted at `Read the Docs <https://tac-etl.readthedocs.io/>`_.

Run the below command to build Docs

.. code-block:: bash
    
    sphinx-build /docs docs/_build/


- To serve the docs locally

.. code-block:: bash

    python3 -m http.server 8080


.. note:: 

    To generate local PDF outputs

       - Install Sphinx-SimplePDF extension `Simple PDF instructions <https://sphinx-simplepdf.readthedocs.io/en/latest/_downloads/b7f58750273e059215e38486bce6e343/Sphinx-SimplePDF.pdf>`_
       
       - Run the following command to output PDF
   
            .. code-block:: bash

                sphinx-build -M simplepdf docs/ docs/pdf

       - Navigate to the _build directory and the PDF output will be inside that folder


- Alternatively, you can run the build commands together as below

.. code-block:: bash

    sphinx-build docs/ docs/_build/ && sphinx-build -M simplepdf docs/ docs/pdf