cmake_minimum_required(VERSION 3.16)

project(play VERSION 0.1 LANGUAGES CXX)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 6.2 COMPONENTS Quick REQUIRED)

qt_add_executable(play
    src/main.cpp
)

target_include_directories(play PUBLIC
    "${CMAKE_CURRENT_SOURCE_DIR}/src"
)

qt_add_qml_module(play
    URI play
    VERSION 1.0
    QML_FILES
        qml/main.qml
        qml/Bullet.qml
        qml/Enemy.qml
    SOURCES
        src/Controller.h src/Controller.cpp
        src/Bullet.h src/Bullet.cpp
        src/Enemy.h src/Enemy.cpp
    RESOURCES
        qml/bullet.qrc
)

set_target_properties(play PROPERTIES
    MACOSX_BUNDLE_BUNDLE_VERSION ${PROJECT_VERSION}
    MACOSX_BUNDLE_SHORT_VERSION_STRING ${PROJECT_VERSION_MAJOR}.${PROJECT_VERSION_MINOR}
    MACOSX_BUNDLE TRUE
    WIN32_EXECUTABLE TRUE
)

target_link_libraries(play
    PRIVATE Qt6::Quick)

include(GNUInstallDirs)
install(TARGETS play
    BUNDLE DESTINATION .
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
