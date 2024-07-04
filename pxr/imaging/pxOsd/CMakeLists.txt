set(PXR_PREFIX pxr/imaging)
set(PXR_PACKAGE pxOsd)

pxr_library(pxOsd
    LIBRARIES
        tf
        gf
        vt
        opensubdiv::opensubdiv
        Boost::python

    PUBLIC_HEADERS
        api.h

    PUBLIC_CLASSES
        meshTopology
        meshTopologyValidation
        refinerFactory
        subdivTags
        tokens

    PYTHON_CPPFILES
        moduleDeps.cpp

    PYMODULE_CPPFILES
        module.cpp
        wrapMeshTopology.cpp
        wrapMeshTopologyValidation.cpp
        wrapSubdivTags.cpp
        wrapTokens.cpp

    PYMODULE_FILES
        __init__.py
)
