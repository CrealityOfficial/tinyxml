file(GLOB SRCS "*.c" "*.cpp")
file(GLOB PUBLIC_HEADERS "*.h")

set(SRCS ${SRCS} ${PUBLIC_HEADERS})
set(DEFS TIXML_USE_STL)
set(LIBS )

__add_real_target(tinyxml lib SOURCE ${SRCS} DEF ${DEFS} LIB ${LIBS}
						INTERFACE ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/../)

if(CC_INSTALL_TINYXML)
	INSTALL(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} DESTINATION include/ FILES_MATCHING PATTERN "*.h")
endif()
