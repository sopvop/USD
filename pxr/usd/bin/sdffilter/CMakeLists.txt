set(PXR_PREFIX pxr/usd)
set(PXR_PACKAGE usd)

pxr_cpp_bin(sdffilter
    LIBRARIES
        arch
        tf
        sdf
        Boost::boost
        Python::Python
        Boost::program_options
)
