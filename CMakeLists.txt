# Generated from qtandroidextras.pro.

cmake_minimum_required(VERSION 3.15.0)

include(.cmake.conf)
project(QtAndroidExtras
    VERSION "${QT_REPO_MODULE_VERSION}"
    DESCRIPTION "Qt AndroidExtras Libraries"
    HOMEPAGE_URL "https://qt.io/"
    LANGUAGES CXX C
)

find_package(Qt6 ${PROJECT_VERSION} CONFIG REQUIRED COMPONENTS BuildInternals Core Gui) # special case

# special case begin
if (NOT ANDROID)
    message(NOTICE "Skipping the build as the condition \"ANDROID\" is not met.")
    return()
endif()
# special case end

if(NOT TARGET Qt::Gui)
    message(NOTICE "Skipping the build as the condition \"TARGET Qt::Gui\" is not met.")
    return()
endif()

qt_build_repo()
