
add_executable(dbghelp_winetest dbghelp.c testlist.c)
target_compile_definitions(dbghelp_winetest PRIVATE WINETEST_USE_DBGSTR_LONGLONG)
set_module_type(dbghelp_winetest win32cui)
add_importlibs(dbghelp_winetest dbghelp gdi32 user32 msvcrt kernel32 ntdll)
add_rostests_file(TARGET dbghelp_winetest)
