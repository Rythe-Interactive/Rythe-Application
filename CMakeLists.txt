project(application LANGUAGES ${RYTHE_LANGUAGE})

rythe_find_sources(sources "${PROJECT_SOURCE_DIR}/src")
add_library(application ${RYTHE_LIBRARY_TYPE} ${sources})

rythe_configure_module(application)
rythe_copy_module_output(application rythe/engine/application)
