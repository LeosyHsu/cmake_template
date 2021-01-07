# 執行檔案 #
add_executable( helloworld main.cpp)
# 連結庫到執行檔案上 # 若無使用到opencv後方＄{OpenCV_LIBS} 不用加入
target_link_libraries(
    helloworld
    mylib
    #${OpenCV_LIBS}
)
