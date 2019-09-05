rock_library(
    base-types 
        Angle.cpp
        Pose.cpp
        TransformWithCovariance.cpp
    HEADERS
        Angle.hpp
        Eigen.hpp
        Float.hpp

        TransformWithCovariance.hpp
    DEPS_PKGCONFIG 
        eigen3
)


configure_file(base-lib.pc.in ${CMAKE_BINARY_DIR}/base-lib.pc @ONLY)
install(FILES ${CMAKE_BINARY_DIR}/base-lib.pc DESTINATION lib/pkgconfig)
