cmake_minimum_required(VERSION 3.11)

project(sobjectizer_fetchcontent_demo LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(FetchContent)

set(FETCHCONTENT_QUIET OFF)

set(SOBJECTIZER_BUILD_SHARED ON CACHE INTERNAL "")
set(SOBJECTIZER_BUILD_STATIC ON CACHE INTERNAL "")
set(SOBJECTIZER_INSTALL ON CACHE INTERNAL "")

FetchContent_Declare(sobjectizer
	GIT_REPOSITORY https://github.com/stiffstream/sobjectizer
	GIT_TAG v.5.7.4.1
	SOURCE_SUBDIR dev
	OVERRIDE_FIND_PACKAGE
	LOG_DOWNLOAD TRUE
	LOG_CONFIGURE TRUE
	LOG_BUILD TRUE
	LOG_INSTALL TRUE
)

FetchContent_MakeAvailable(sobjectizer)

add_subdirectory(hello_world)
