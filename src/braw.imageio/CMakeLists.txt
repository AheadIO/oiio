if (USE_BlackMagicRAW AND BlackMagicRAW_FOUND)
    message (STATUS "Building BlackMagicRAW plugin")
    add_oiio_plugin (brawinput.cpp BlackmagicRawAPIDispatch.cpp
        INCLUDE_DIRS ${BlackMagicRAW_INCLUDE_DIR}
        LINK_LIBRARIES ${BlackMagicRAW_LIBRARIES}
        DEFINITIONS "-DUSE_BlackMagicRAW=1")
else ()
    message (WARNING "BlackMagicRAW plugin will not be built")
endif ()

