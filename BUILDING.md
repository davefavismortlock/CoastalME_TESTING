.. _building_from_source:

================================================================================
Building CoastalME from source
================================================================================

.. _build_requirements:

Build requirements
--------------------------------------------------------------------------------

The minimum requirements to build CoastalME are:

- CMake >= 3.16, and an associated build system (make, ninja, Visual Studio, etc.)
- GDAL >= 2.1 
- C++11 
- F77 compiler


CMake (CoastalME versions >= 3.5.0)
--------------------------------------------------------------------------------

Since version 3.5.0, CoastalME can be built using the CMake build system.
With the CMake build system you can compile and install CoastalME on more or less any
platform. After unpacking the source distribution archive (or cloning the repository)
step into the source tree:

.. code-block:: bash

    cd CoastalME-{VERSION}

Create a build directory and step into it:

.. code-block:: bash

    mkdir build
    cd build

From the build directory you can now configure CMake, build and install the binaries:

.. code-block:: bash

    cmake ..
    cmake --build .
    cmake --build . --target install

.. note::

    For a minimal build, add these options to the initial ``cmake`` command: ``...``.
    To enable specific DEBUG drivers, add ``....`` or ``...``.
    