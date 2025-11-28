add_library(series_core STATIC
        src/series.cpp
)

target_link_libraries(series_core PRIVATE project_warnings)
if (TARGET project_sanitizers)
        target_link_libraries(series_core PRIVATE project_sanitizers)
endif ()

target_include_directories(series_core
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

