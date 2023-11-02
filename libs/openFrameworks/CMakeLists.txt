find_package(OpenGL REQUIRED)
find_package(glm REQUIRED)
find_package(GLEW REQUIRED)
find_package(pugixml REQUIRED)
find_package(glfw3 REQUIRED)
find_package(nlohmann_json REQUIRED)
find_package(Fontconfig REQUIRED)
find_package(X11 REQUIRED)
find_package(SndFile REQUIRED)
find_package(OpenAL REQUIRED)
find_package(uriparser REQUIRED)
find_package(CURL REQUIRED)

find_package(PkgConfig REQUIRED)
pkg_check_modules(gtk3 REQUIRED IMPORTED_TARGET gtk+-3.0)
pkg_search_module(gstreamer REQUIRED IMPORTED_TARGET gstreamer-1.0>=1.4)
pkg_search_module(gstreamer-sdp REQUIRED IMPORTED_TARGET gstreamer-sdp-1.0>=1.4)
pkg_search_module(gstreamer-app REQUIRED IMPORTED_TARGET gstreamer-app-1.0>=1.4)
pkg_search_module(gstreamer-video REQUIRED IMPORTED_TARGET gstreamer-video-1.0>=1.4)
pkg_search_module(CAIRO REQUIRED cairo>=1.12.16)
pkg_search_module(RtAudio REQUIRED rtaudio>=5.0.0)

set(OF_HEADERS
  ofMain.h

  3d/of3dPrimitives.h
  3d/of3dUtils.h
  3d/ofCamera.h
  3d/ofEasyCam.h
  3d/ofMesh.h
  3d/ofMesh.inl
  3d/ofNode.h

  app/ofAppBaseWindow.h
  # app/ofAppEGLWindow.h for ARM
  app/ofAppGLFWWindow.h
  app/ofAppGlutWindow.h
  app/ofAppNoWindow.h
  app/ofAppRunner.h
  app/ofBaseApp.h
  app/ofIcon.h
  app/ofMainLoop.h
  app/ofWindowSettings.h

  communication/ofArduino.h
  communication/ofSerial.h

  events/ofEvent.h
  events/ofEvents.h
  events/ofEventUtils.h

  gl/ofBufferObject.h
  gl/ofCubeMap.h
  gl/ofCubeMapShaders.h
  gl/ofFbo.h
  gl/ofGLBaseTypes.h
  gl/ofGLProgrammableRenderer.h
  gl/ofGLRenderer.h
  gl/ofGLUtils.h
  gl/ofLight.h
  gl/ofMaterial.h
  gl/ofMaterialBaseTypes.h
  gl/ofShader.h
  gl/ofShadow.h
  gl/ofTexture.h
  gl/ofVbo.h
  gl/ofVboMesh.h

  graphics/of3dGraphics.h
  graphics/ofBitmapFont.h
  graphics/ofCairoRenderer.h
  graphics/ofGraphics.h
  graphics/ofGraphicsBaseTypes.h
  graphics/ofGraphicsCairo.h
  graphics/ofGraphicsConstants.h
  graphics/ofImage.h
  graphics/ofPath.h
  graphics/ofPixels.h
  graphics/ofPolyline.h
  graphics/ofPolyline.inl
  graphics/ofRendererCollection.h
  graphics/ofTessellator.h
  graphics/ofTrueTypeFont.h

  math/ofMath.h
  math/ofMathConstants.h
  math/ofMatrix3x3.h
  math/ofMatrix4x4.h
  math/ofQuaternion.h
  math/ofVec2f.h
  math/ofVec3f.h
  math/ofVec4f.h
  math/ofVectorMath.h

  sound/ofOpenALSoundPlayer.h
  sound/ofRtAudioSoundStream.h
  sound/ofSoundBaseTypes.h
  sound/ofSoundBuffer.h
  sound/ofSoundPlayer.h
  sound/ofSoundStream.h
  sound/ofSoundUtils.h

  types/ofBaseTypes.h
  types/ofColor.h
  types/ofParameter.h
  types/ofPoint.h
  types/ofRectangle.h
  types/ofTypes.h

  utils/ofConstants.h
  utils/ofFileUtils.h
  utils/ofFpsCounter.h
  utils/ofJson.h
  utils/ofLog.h
  utils/ofMatrixStack.h
  utils/ofNoise.h
  utils/ofRandomDistributions.h
  utils/ofRandomEngine.h
  utils/ofSingleton.h
  utils/ofSystemUtils.h
  utils/ofThread.h
  utils/ofThreadChannel.h
  utils/ofTimer.h
  utils/ofURLFileLoader.h
  utils/ofUtils.h
  utils/ofXml.h

  video/ofGstUtils.h
  video/ofGstVideoGrabber.h
  video/ofGstVideoPlayer.h
  video/ofVideoBaseTypes.h
  video/ofVideoGrabber.h
  video/ofVideoPlayer.h
)

set(OF_SOURCES
  3d/of3dPrimitives.cpp
  3d/of3dUtils.cpp
  3d/ofCamera.cpp
  3d/ofEasyCam.cpp
  3d/ofNode.cpp

  # app/ofAppEGLWindow.cpp for ARM
  app/ofAppGLFWWindow.cpp
  app/ofAppGlutWindow.cpp
  app/ofAppNoWindow.cpp
  app/ofAppRunner.cpp
  app/ofBaseApp.cpp
  app/ofMainLoop.cpp

  communication/ofArduino.cpp
  communication/ofSerial.cpp

  events/ofEvents.cpp

  gl/ofBufferObject.cpp
  gl/ofCubeMap.cpp
  gl/ofFbo.cpp
  gl/ofGLProgrammableRenderer.cpp
  gl/ofGLRenderer.cpp
  gl/ofGLUtils.cpp
  gl/ofLight.cpp
  gl/ofMaterial.cpp
  gl/ofShader.cpp
  gl/ofShadow.cpp
  gl/ofTexture.cpp
  gl/ofVbo.cpp
  gl/ofVboMesh.cpp

  graphics/of3dGraphics.cpp
  graphics/ofBitmapFont.cpp
  graphics/ofCairoRenderer.cpp
  graphics/ofGraphics.cpp
  graphics/ofGraphicsBaseTypes.cpp
  graphics/ofGraphicsCairo.cpp
  graphics/ofImage.cpp
  graphics/ofPath.cpp
  graphics/ofPixels.cpp
  graphics/ofRendererCollection.cpp
  graphics/ofTessellator.cpp
  graphics/ofTrueTypeFont.cpp

  math/ofMath.cpp
  math/ofMatrix3x3.cpp
  math/ofMatrix4x4.cpp
  math/ofQuaternion.cpp
  math/ofVec2f.cpp
  math/ofVec4f.cpp

  sound/ofOpenALSoundPlayer.cpp
  sound/ofRtAudioSoundStream.cpp
  sound/ofSoundBaseTypes.cpp
  sound/ofSoundBuffer.cpp
  sound/ofSoundPlayer.cpp
  sound/ofSoundStream.cpp

  types/ofBaseTypes.cpp
  types/ofColor.cpp
  types/ofParameter.cpp
  types/ofParameterGroup.cpp
  types/ofRectangle.cpp

  utils/ofFileUtils.cpp
  utils/ofFpsCounter.cpp
  utils/ofLog.cpp
  utils/ofMatrixStack.cpp
  utils/ofSystemUtils.cpp
  utils/ofThread.cpp
  utils/ofTimer.cpp
  utils/ofURLFileLoader.cpp
  utils/ofUtils.cpp
  utils/ofXml.cpp

  video/ofGstUtils.cpp
  video/ofGstVideoGrabber.cpp
  video/ofGstVideoPlayer.cpp
  video/ofVideoBaseTypes.h
  video/ofVideoGrabber.cpp
  video/ofVideoPlayer.cpp
)

add_library(openFrameworks STATIC ${OF_HEADERS} ${OF_SOURCES})

target_link_libraries(openFrameworks PUBLIC tess2 OpenGL::EGL glm glfw GLEW::glew nlohmann_json::nlohmann_json
pugixml kissfft PkgConfig::gtk3 Fontconfig::Fontconfig X11::X11 SndFile::sndfile uriparser freeimage
    PkgConfig::gstreamer
    PkgConfig::gstreamer-sdp
    PkgConfig::gstreamer-app
    PkgConfig::gstreamer-video ${CAIRO_LIBRARIES} ${RtAudio_LIBRARIES} ${OPENAL_LIBRARY} ${CURL_LIBRARIES} udev)
target_include_directories(openFrameworks PUBLIC ${CAIRO_INCLUDE_DIRS} ${RtAudio_INCLUDE_DIRS})

target_include_directories(openFrameworks PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
  ${CMAKE_CURRENT_SOURCE_DIR}/3d
  ${CMAKE_CURRENT_SOURCE_DIR}/app
  ${CMAKE_CURRENT_SOURCE_DIR}/communication
  ${CMAKE_CURRENT_SOURCE_DIR}/events
  ${CMAKE_CURRENT_SOURCE_DIR}/gl
  ${CMAKE_CURRENT_SOURCE_DIR}/graphics
  ${CMAKE_CURRENT_SOURCE_DIR}/math
  ${CMAKE_CURRENT_SOURCE_DIR}/sound
  ${CMAKE_CURRENT_SOURCE_DIR}/types
  ${CMAKE_CURRENT_SOURCE_DIR}/utils
  ${CMAKE_CURRENT_SOURCE_DIR}/video
)
