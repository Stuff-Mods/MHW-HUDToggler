project(HUDToggler)
FILE(GLOB_RECURSE HUDTogglerSources CONFIGURE_DEPENDS ${PROJECT_SOURCE_DIR} *.h *.cpp)
add_library(HUDToggler SHARED ${HUDTogglerSources})
target_compile_features(HUDToggler PRIVATE cxx_std_20)
target_link_libraries(HUDToggler
PRIVATE
  stuff
  mhw-common
  GamepadLib
  yaml-cpp
)
