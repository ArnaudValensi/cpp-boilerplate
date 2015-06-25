include_directories(${FI_SDK_SOURCE_DIR}/src)

file(
    GLOB AE_SRC
    "*.h"
    "*.hpp"
    "*.cpp"
)

add_executable(ae ${AE_SRC})

target_link_libraries(ae ${LIBS})
