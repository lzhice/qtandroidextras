# Generated from jar.pro.

set(java_sources
    src/org/qtproject/qt/android/extras/QtAndroidBinder.java
    src/org/qtproject/qt/android/extras/QtAndroidServiceConnection.java
    src/org/qtproject/qt/android/extras/QtNative.java
)

qt_internal_add_jar(Qt${QtAndroidExtras_VERSION_MAJOR}AndroidExtras # special case
    INCLUDE_JARS ${QT_ANDROID_JAR}
    SOURCES ${java_sources}
    OUTPUT_DIR "${QT_BUILD_DIR}/jar"
)

install_jar(Qt${QtAndroidExtras_VERSION_MAJOR}AndroidExtras # special case
    DESTINATION jar
    COMPONENT Devel
)

