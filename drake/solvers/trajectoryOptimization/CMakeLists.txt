add_library_with_exports(LIB_NAME drakeTrajectoryOptimization SOURCE_FILES
  direct_trajectory_optimization.cc)
target_link_libraries(drakeTrajectoryOptimization drakeOptimization
  drakeTrajectories)
pods_install_libraries(drakeTrajectoryOptimization)
drake_install_headers(direct_trajectory_optimization.h)
pods_install_pkg_config_file(drake-trajectory-optimization
  LIBS -ldrakeTrajectoryOptimization
  REQUIRES
  VERSION 0.0.1)

add_subdirectory(test)
