
add_library(tess2 STATIC
  libtess2/Source/bucketalloc.c
  libtess2/Source/dict.c
  libtess2/Source/geom.c
  libtess2/Source/mesh.c
  libtess2/Source/priorityq.c
  libtess2/Source/sweep.c
  libtess2/Source/tess.c
)

target_include_directories(tess2 PUBLIC libtess2/Include PRIVATE libtess2/Source)

set(BUILD_SHARED_LIBS OFF CACHE BOOL "" FORCE)
set(KISSFFT_TEST OFF CACHE BOOL "" FORCE)
set(KISSFFT_TOOLS OFF CACHE BOOL "" FORCE)
set(KISSFFT_STATIC ON CACHE BOOL "" FORCE)
add_subdirectory(kissfft)

add_subdirectory(openFrameworks)
