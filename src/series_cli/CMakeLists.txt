add_executable(series_cli
        src/main.cpp
)

target_link_libraries(series_cli PRIVATE series_core project_warnings)
if (TARGET project_sanitizers)
        target_link_libraries(series_cli PRIVATE project_sanitizers)
endif ()

