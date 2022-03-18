project(application_sandbox LANGUAGES ${RYTHE_LANGUAGE})

rythe_find_sources(sources "${PROJECT_SOURCE_DIR}")
add_executable(application_sandbox ${sources})
set_target_properties(application_sandbox PROPERTIES FOLDER applications)

rythe_configure_engine_application(application_sandbox)
