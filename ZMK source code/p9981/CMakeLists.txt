if(CONFIG_BOARD_P9981)
zephyr_library()
zephyr_library_sources(custom_driver/keyboard_backlight.c)
zephyr_library_include_directories(${ZEPHYR_BASE}/drivers)
zephyr_library_include_directories(../../../include)
zephyr_library_include_directories(${CMAKE_SOURCE_DIR}/include)
endif()
 