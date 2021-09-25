project(raysettings CXX)

set (CMAKE_CXX_STANDARD 17)
set (CMAKE_CXX_EXTENSIONS off)

#==========================================
set (SRC_FILES
"SettingsWindow.cpp"
"WinWrapper.cpp"
)
#==========================================
set (HEADER_FILES
"SettingsWindow.h"
"WinWrapper.h"
"RaySettingsTypes.h"
)
#==========================================
add_library(raysettings ${SRC_FILES} ${HEADER_FILES})
target_link_libraries(raysettings raylib)
set (INCLUDE_DIR
"../raylib/src"
"../raylib/src/extras"
)
target_include_directories(raysettings PUBLIC ${INCLUDE_DIR})
