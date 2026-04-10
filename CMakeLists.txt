cmake_minimum_required(VERSION 3.16)

# 1. Use the environment variable so it works with 5.4.1 or whatever is active
include($ENV{IDF_PATH}/tools/cmake/project.cmake)

# 2. Add your extra components
set(EXTRA_COMPONENT_DIRS "./components/button")

# 3. Suppress those format errors (Put these BEFORE the project() call)
add_compile_options("-Wno-format")
add_compile_options("-Wno-error=format=")

# 4. Initialize the project
project(esp32-xbee)

# 5. Global "Sledgehammer" to ignore warnings-as-errors (Put this AFTER project())
idf_build_set_property(COMPILE_OPTIONS "-Wno-error=all" APPEND)