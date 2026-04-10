set(COMPONENT_SRCS "button.c")
set(COMPONENT_ADD_INCLUDEDIRS "include")

set(COMPONENT_REQUIRES esp_driver_gpio esp_timer)

register_component()
