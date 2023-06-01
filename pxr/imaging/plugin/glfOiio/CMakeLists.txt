set(PXR_PREFIX pxr/imaging)
set(PXR_PACKAGE glfOiio)

if (NOT ${PXR_ENABLE_GL_SUPPORT})
    message(STATUS
            "Skipping ${PXR_PACKAGE} because PXR_ENABLE_GL_SUPPORT is OFF")
    return()
endif()

pxr_plugin(glfOiio
    LIBRARIES
        ar
        arch
        gf
        glf
        tf
        OpenImageIO::OpenImageIO
        OpenEXR::IlmImf

    CPPFILES
        oiioImage.cpp

    RESOURCE_FILES
        plugInfo.json
)
