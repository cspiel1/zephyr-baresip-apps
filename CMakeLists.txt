#
# Copyright (c) 2023 Christian Spielberger
#

include(CheckIncludeFile)

zephyr_library()

zephyr_include_directories(
        ${ZEPHYR_CURRENT_MODULE_DIR}/lib/include
        ${ZEPHYR_CURRENT_MODULE_DIR}/lib/src
)

zephyr_library_compile_definitions(
   -DSTATIC
)

zephyr_library_sources(
  lib/modules/auwm8960/auwm8960.c
  lib/modules/auwm8960/auwm8960_play.c
)
