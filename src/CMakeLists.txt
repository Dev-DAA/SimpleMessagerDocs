cmake_minimum_required(VERSION 3.0)

set(CMAKE_CXX_STANDARD 11)

file(GLOB_RECURSE src main.cpp)

set(sources
    ${src}
)

add_executable(${PROJECT_NAME} ${sources})

find_library(POCO_LIB Poco)

if(POCO_LIB)
    message ("POCO FOUND!!!")
else()
    message ("POCO NOT FOUND!!!")
endif()


find_package(Poco REQUIRED COMPONENTS Foundation Net Zip )

target_link_libraries(${PROJECT_NAME} PUBLIC Poco::Foundation Poco::Zip Poco::Net)