add_library(pico_ssd1306_i2c INTERFACE)

target_sources(pico_ssd1306_i2c INTERFACE
  ${CMAKE_CURRENT_LIST_DIR}/ssd1306-i2c.c
)

target_include_directories(pico_ssd1306_i2c INTERFACE ${CMAKE_CURRENT_LIST_DIR})

# Pull in pico libraries that we need
target_link_libraries(pico_ssd1306_i2c INTERFACE pico_stdlib hardware_i2c)


add_library(pico_ssd1306_spi INTERFACE)

target_sources(pico_ssd1306_spi INTERFACE
  ${CMAKE_CURRENT_LIST_DIR}/ssd1306-spi.c
)

target_include_directories(pico_ssd1306_spi INTERFACE ${CMAKE_CURRENT_LIST_DIR})

# Pull in pico libraries that we need
target_link_libraries(pico_ssd1306_spi INTERFACE pico_stdlib hardware_spi)