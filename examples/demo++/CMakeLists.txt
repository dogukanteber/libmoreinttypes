# Build and run demo application
set(CMAKE_INSTALL_RPATH lib)
set(CMAKE_INSTALL_RPATH_USE_LINK_PATH TRUE)
add_executable(cpp-demo "main.cpp")
set_target_properties (cpp-demo PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${PROJECT_SOURCE_DIR}/build")
if (MSVC)
    target_compile_options(cpp-demo PRIVATE /EHsc)
endif()
target_link_libraries(cpp-demo PRIVATE moreinttypes)
