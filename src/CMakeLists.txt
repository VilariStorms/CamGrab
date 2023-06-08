# add the executable
add_executable(${PROJECT_NAME} main.cpp)

# link against the libraries  ole32.lib strmiids.lib oleaut32.lib
target_link_libraries(${PROJECT_NAME} PRIVATE ole32.lib strmiids.lib oleaut32.lib
)
