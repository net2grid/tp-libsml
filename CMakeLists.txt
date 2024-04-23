file(GLOB srcs_libsml ${CMAKE_CURRENT_LIST_DIR}/sml/src/*.c)
set(incl_libsml       ${CMAKE_CURRENT_LIST_DIR}/sml/include)
set(incl_libsml       ${CMAKE_CURRENT_LIST_DIR}/sml/include)

set(defs_libsml       "SML_NO_UUID_LIB")

if(NOT CMAKE_SCRIPT_MODE_FILE OR CMAKE_PARENT_LIST_FILE)
  add_library(libsml ${srcs_libsml})
  target_include_directories(libsml PUBLIC ${incl_libsml})
  target_compile_definitions(libsml PRIVATE ${defs_libsml})
endif()
