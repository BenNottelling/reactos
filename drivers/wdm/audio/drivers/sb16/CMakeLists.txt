
set_cpp()

list(APPEND SOURCE
    adapter.cpp
    main.cpp
    stdunk.cpp)

add_library(sb16 MODULE ${SOURCE})
add_dependencies(sb16 xdk)
add_cd_file(TARGET sb16 DESTINATION reactos/system32/drivers FOR all)
