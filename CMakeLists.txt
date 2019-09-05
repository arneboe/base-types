cmake_minimum_required(VERSION 2.6)
find_package(Rock)
rock_init(base 1.0)

set(CMAKE_CXX_STANDARD 11)

# rock_export_includedir(${PROJECT_SOURCE_DIR}/base ${PROJECT_NAME})
rock_export_includedir(${PROJECT_SOURCE_DIR}/src base/geometry)
include_directories(BEFORE ${PROJECT_SOURCE_DIR})

rock_find_pkgconfig(Eigen3 eigen3 REQUIRED)


rock_standard_layout()
