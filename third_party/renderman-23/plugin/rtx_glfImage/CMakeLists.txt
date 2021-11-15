set(PXR_PREFIX "")
set(PXR_PACKAGE RtxGlfImage)

pxr_plugin(${PXR_PACKAGE}

    LIBRARIES
        tf
        glf
        ${PXRCORE_LIBRARY}
        ${PRMAN_LIBRARY}
        GLEW::GLEW

    INCLUDE_DIRS
        ${RENDERMAN_INCLUDE_DIR}

    CPPFILES
        main.cpp 

    PRIVATE_HEADERS

    RESOURCE_FILES

    DISABLE_PRECOMPILED_HEADERS
)
