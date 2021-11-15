set(PXR_PREFIX pxr/imaging)
set(PXR_PACKAGE hgiGL)

if (NOT ${PXR_ENABLE_GL_SUPPORT})
    message(STATUS
        "Skipping ${PXR_PACKAGE} because PXR_ENABLE_GL_SUPPORT is OFF")
    return()
endif()

pxr_library(hgiGL
    LIBRARIES
        arch
        hgi
        tf
        trace
        GLEW::GLEW
        ${OPENGL_gl_LIBRARY}
        ${OPENGL_glu_LIBRARY}

    INCLUDE_DIRS
        ${OPENGL_INCLUDE_DIR}

    PRIVATE_CLASSES
        conversions
        diagnostic
        scopedStateHolder

    PUBLIC_CLASSES
        blitCmds
        buffer
        computeCmds
        computePipeline
        device
        framebufferCache
        garbageCollector
        graphicsCmds
        graphicsPipeline
        hgi
        ops
        resourceBindings
        sampler
        shaderFunction
        shaderProgram
        texture

    PUBLIC_HEADERS
        api.h

    RESOURCE_FILES
        plugInfo.json
)
