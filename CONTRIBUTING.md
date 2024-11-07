# How to contribute?

There are several ways for developers and users to contribute to CoastalME:

- [Contributing code](#contributing-code)
- [Filing high-quality reports](#filing-high-quality-reports)
- [Improving documentation](#improving-documentation)
- [Credits](#credits)

## Contributing code

Minor changes to CoastalME, such as bug fixes, may be made by opening a GitHub pull request.

Major changes should be discussed on the [coastalme-dev emaillist](http://lists.osgeo.org/mailman/listinfo/coastalme-dev) and may require the drafting of a RFC (request for comment) document.

CoastalME's policy on substantial code additions is documented at :ref:`rfc-85`.

## Filing high-quality issue reports

Using the GitHub [issue reports](https://github.com/apayo/CoastalME/issues) at the Master repository. 

## Improving documentation

CoastalME's documentation includes C++ [API documentation](https://codedocs.xyz/apayo/CoastalME/) built automatically from source comments using Doxygen and [CodeDocx.XYZ](https://codedocs.xyz files containing manually-edited content.

To be correctly parsed, the documentation should follow the Doxygen block documentation style (https://doxygen.nl/manual/docblocks.html#specialblock)

.. code-block:: bash
	/*! \brief Brief description.
	*         Brief description continued.
	*
	*  Detailed description starts here.
	*/

## Credits

This section has been largely inspired by https://github.com/OSGeo/gdal