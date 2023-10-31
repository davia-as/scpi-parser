# List header files (optional, as headers aren't typically required for building, but listing can be useful for IDEs)
set(SRC_HEADERS
    ${CMAKE_CURRENT_SOURCE_DIR}/fifo_pricate.h
    ${CMAKE_CURRENT_SOURCE_DIR}/lexer_private.h
    ${CMAKE_CURRENT_SOURCE_DIR}/parser_private.h
    ${CMAKE_CURRENT_SOURCE_DIR}/utils_private.h
)

# Export the include directories to the parent scope
set(SRC_HEADERS ${CMAKE_CURRENT_SOURCE_DIR} PARENT_SCOPE)

# List source files
set(LIB_SOURCES
    ${CMAKE_CURRENT_SOURCE_DIR}/error.c
    ${CMAKE_CURRENT_SOURCE_DIR}/expression.c
    ${CMAKE_CURRENT_SOURCE_DIR}/fifo.c
    ${CMAKE_CURRENT_SOURCE_DIR}/ieee488.c
    ${CMAKE_CURRENT_SOURCE_DIR}/lexer.c
    ${CMAKE_CURRENT_SOURCE_DIR}/minimal.c
    ${CMAKE_CURRENT_SOURCE_DIR}/parser.c
    ${CMAKE_CURRENT_SOURCE_DIR}/units.c
    ${CMAKE_CURRENT_SOURCE_DIR}/utils.c
    PARENT_SCOPE  # Important to make these sources available in the parent CMakeLists.txt
)
