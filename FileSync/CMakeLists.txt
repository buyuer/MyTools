cmake_minimum_required (VERSION 3.8)

project ("Qt")

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 打开全局moc
set(CMAKE_AUTOMOC ON)
# 打开全局uic
set(CMAKE_AUTOUIC ON)
# 打开全局rcc
set(CMAKE_AUTORCC ON)

find_package(Qt5 COMPONENTS Core Gui Widgets Qml Quick REQUIRED)

add_executable(test FileSync.cpp)

target_link_libraries(test Qt5::Core Qt5::Gui Qt5::Widgets Qt5::Qml Qt5::Quick)
