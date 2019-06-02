cmake_minimum_required(VERSION 3.13)
project(efanna_graph)

set(CMAKE_CXX_STANDARD 14)

include_directories(include)
include_directories(include/efanna2e)

add_executable(efanna_graph
        include/efanna2e/distance.h
        include/efanna2e/exceptions.h
        include/efanna2e/index.h
        include/efanna2e/index_graph.h
        include/efanna2e/index_kdtree.h
        include/efanna2e/index_pq.h
        include/efanna2e/index_random.h
        include/efanna2e/neighbor.h
        include/efanna2e/parameters.h
        include/efanna2e/util.h
        src/index.cpp
        src/index_graph.cpp
        src/index_kdtree.cpp
        src/index_pq.cpp
        src/index_random.cpp
        tests/test_faiss_graph.cpp
        tests/test_kdtree_graph.cpp
        tests/test_nndescent.cpp
        tests/test_nndescent_refine.cpp)
