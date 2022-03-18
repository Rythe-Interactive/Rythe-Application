project(application LANGUAGES ${RYTHE_LANGUAGE})

rythe_find_sources(sources "${PROJECT_SOURCE_DIR}/src")
add_library(application ${RYTHE_LIBRARY_TYPE} ${sources})

rythe_add_third_party(
	CURRENT application
	LIBRARY glfw
	PATH "${RYTHE_DIR_ENGINE}/application/third_party/glfw"
	INCLUDE "${RYTHE_DIR_ENGINE}/application/third_party/glfw/include"
	FOLDER "third_party/glfw3"
	FOLDER_TARGETS glfw docs uninstall update_mappings
)

rythe_configure_module(application)
rythe_copy_module_output(application rythe/engine/application)
