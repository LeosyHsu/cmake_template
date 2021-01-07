# 生成lib #
add_library(mylib SHARED
    myclass.cpp
    #...
)
# 連結lib到執行檔案上 #
target_link_libraries(
    mylib
    ${THIRD_PARTY_LIBS}
)
