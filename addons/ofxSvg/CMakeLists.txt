set(OFX_SVG_SOURCES
  src/ofxSvg.h
  src/ofxSvg.cpp
)
add_library(ofxSvg STATIC ${OFX_SVG_SOURCES})
add_library(ofx::Svg ALIAS ofxSvg)
target_include_directories(ofxSvg PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)
target_link_libraries(ofxSvg PUBLIC openFrameworks)
