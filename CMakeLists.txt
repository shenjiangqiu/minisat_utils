cmake_minimum_required(VERSION 3.10)
project(minisat_utiles)
find_package(Boost REQUIRED COMPONENTS serialization)
set(CMAKE_CXX_STANDARD 17)

file(GLOB_RECURSE  SOURCES *.cc)
add_library(minisat_utiles  "${SOURCES}")
target_link_libraries(minisat_utiles PUBLIC ${Boost_LIBRARIES} fmt::fmt )
target_include_directories(minisat_utiles PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} ${Boost_INCLUDE_DIRS} )
