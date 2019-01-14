add_executable(ixy-pktgen ixy-pktgen.c)
target_link_libraries(ixy-pktgen PRIVATE
  ixy
  )

add_executable(ixy-fwd ixy-fwd.c)
target_link_libraries(ixy-fwd PRIVATE
  ixy
  )
