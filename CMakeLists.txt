cmake_minimum_required(VERSION 3.16)
project(QZXing)

find_package(Qt6 COMPONENTS Core REQUIRED)

SET(PROJECT_VERSION "3.3")
set(CMAKE_AUTOMOC ON)
set(CMAKE_WARN_ON)
set(CMAKE_OSX_ARCHITECTURES x86_64;arm64)

#if build example...
#add_compile_definitions(-DQZXING_USE_QML)
set(QZXING_MULTIMEDIA ON)
set(QZXING_USE_ENCODER ON)
#DECODE QR_CODE
set(QZXING_USE_DECODER_QR_CODE ON)
set(QZXING_USE_DECODER_1D_BARCODES ON)
set(QZXING_USE_DECODER_DATA_MATRIX ON)
set(QZXING_USE_DECODER_AZTEC ON)
set(QZXING_USE_DECODER_PDF17 ON)
add_subdirectory(src)
