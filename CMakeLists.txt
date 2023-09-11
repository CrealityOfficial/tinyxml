__files_group(${CMAKE_CURRENT_SOURCE_DIR}/tinyxml/ SRCS)

set(DEFS TIXML_USE_STL)
set(INTERFACE_DEFS TIXML_USE_STL)
set(LIBS)
set(INCS ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/tinyxml/)

__add_real_target(tinyxml lib SOURCE ${SRCS} 
							  DEF ${DEFS}
							  INC ${INCS}
							  INTERFACE ${INCS}
							  )

if(CC_INSTALL_TINYXML)
	__install_directory_specif(${CMAKE_CURRENT_SOURCE_DIR}/tinyxml tinyxml)
endif()
