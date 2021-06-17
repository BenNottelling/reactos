list(APPEND SOURCE
    adapter.cpp
    main.cpp
    stdunk.cpp)

add_library(sb16 MODULE ${SOURCE})
add_importlibs(sb16 portcls ntoskrnl)
add_cd_file(TARGET sb16 DESTINATION reactos/system32/drivers FOR all)
