add_library(wepoll STATIC
  wepoll.c
)

target_compile_definitions(wepoll PUBLIC WIN32_LEAN_AND_MEAN)

install(FILES "wepoll.h" DESTINATION ${CMAKE_INSTALL_PREFIX}/include)

set_target_properties(wepoll
  PROPERTIES
  LIBRARY_OUTPUT_DIRECTORY "${CMAKE_INSTALL_PREFIX}/lib"
  ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_INSTALL_PREFIX}/bin"
  PDB_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/"
)
