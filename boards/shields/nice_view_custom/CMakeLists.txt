if(CONFIG_ZMK_DISPLAY AND CONFIG_NICE_VIEW_WIDGET_STATUS)
  zephyr_library_include_directories(${CMAKE_SOURCE_DIR}/include)
  zephyr_library_sources(widgets/art.c)             # <-- apenas seu art.c

  if(NOT CONFIG_ZMK_SPLIT OR CONFIG_ZMK_SPLIT_ROLE_CENTRAL)
    # Nenhum outro widget necessário no central/master
  else()
    zephyr_library_sources(widgets/peripheral_status.c)  # se quiser manter status do periférico
  endif()
endif()
