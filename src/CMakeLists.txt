set(SOURCES
  driver/device.c
  driver/ixgbe.c
  driver/virtio.c
  memory.c
  pci.c
  stats.c
  )

set(HEADERS
  driver/device.h
  driver/ixgbe.h
  driver/virtio.h
  driver/virtio_type.h
  log.h
  memory.h
  pci.h
  stats.h
  )

add_library(ixy SHARED
  ${SOURCES}
  ${HEADERS}
  )

target_include_directories(ixy PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
  )

target_compile_definitions(ixy PUBLIC
  "_XOPEN_SOURCE=700"
  "_DEFAULT_SOURCE"
  "_POSIX_C_SOURCE"
  )

target_link_libraries(ixy PRIVATE
  pthread
  )

add_subdirectory(app)
