project(main)

add_executable(${PROJECT_NAME} main.cpp)
target_include_directories(${PROJECT_NAME} PRIVATE ./main)

# target_link_libraries(${PROJECT_NAME} PRIVATE third_party)
if(EMSCRIPTEN)
    target_link_options(${PROJECT_NAME} PRIVATE -sWASM=1)
    target_link_options(${PROJECT_NAME} PRIVATE -sASSERTIONS=1)
    set(CMAKE_EXECUTABLE_SUFFIX ".html")
endif()
