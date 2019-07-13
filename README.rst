TEfy
====

|Build Status| |PyPI version| 

``TEfy`` was born out of the need to streamline the conversion of doc,
docx and odt documents into TEI XML when using Python scripts. It's a
very basic wrapper around the OxGarage_
API at https://oxgarage.tei-c.org/ege-webservice/ and
covers a small subset of conversions, namely from doc, docx and odt to TEI
XML. The conversion result is output as an lxml_ etree Element. 

.. _OxGarage: https://github.com/TEIC/oxgarage
.. _lxml: https://github.com/lxml/lxml

Usage 
-----
You can install TEfy from `PyPI <https://pypi.org/project/TEfy/>`__ (``$ pip
install TEfy``) and convert let's say an ODT document like this:

.. code:: python

    from TEfy import OxGaWrap
    example_file = OxGaWrap('path/to/example.odt')
    example_file.convert_to_tei()
    etree_object = example_file.get_et_output()

.. |Build Status| image:: https://travis-ci.org/03b8/TEfy.svg?branch=master
   :target: https://travis-ci.org/03b8/TEfy
.. |PyPI version| image:: https://badge.fury.io/py/TEfy.svg
   :target: https://badge.fury.io/py/TEfy