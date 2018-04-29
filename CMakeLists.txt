cmake_minimum_required(VERSION 3.10)

set(THEMES_INSTALL_DIR /usr/share/themes)
project(Manjarin)
install(DIRECTORY gtk-2.0 gtk-3.0 DESTINATION ${THEMES_INSTALL_DIR}/Manjarin)
