# 定義需求版本和工程名稱#
cmake_minimum_required(VERSION 3.12)
project(image_dynamic_range_adjustment)
# cmake相關的一些設定#
set(CMAKE_CXX_STANDARD 14)
set( CMAKE_BUILD_TYPE "Release" )
set( CMAKE_CXX_FLAGS "-std=c++11 -O3" )
# 新增cmake_modules到CMAKE_MODULE_PATH路徑列表中和
list( APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake_modules )
# 設定可執行檔案與庫檔案的輸出路徑bin、lib #
set( EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin )
set( LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib )

###### 找第三方庫和新增標頭檔案 ######
# 無使用可直接省略
#find_package( OpenCV 4.5.0 REQUIRED )
#include_directories(
#    ${OpenCV_INCLUDE_DIRS}
#)

####### 自己寫的標頭檔案 ######
include_directories( ${PROJECT_SOURCE_DIR}/include )
#增加子目錄#
add_subdirectory( src )
add_subdirectory( test )
