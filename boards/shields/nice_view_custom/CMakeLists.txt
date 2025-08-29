if(CONFIG_ZMK_DISPLAY AND CONFIG_NICE_VIEW_WIDGET_STATUS)
    zephyr_library_include_directories(${CMAKE_SOURCE_DIR}/include)

    zephyr_library_sources(
        cat-animation-1bit/boards/shields/nice_view_custom/custom_status_screen.c
        cat-animation-1bit/boards/shields/nice_view_custom/widgets/peripheral_status.c
        cat-animation-1bit/boards/shields/nice_view_custom/widgets/art.c
    )
endif()
