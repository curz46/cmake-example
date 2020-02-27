# All the garbage in the top-level file is inherited
# e.g. minimum required version

# Executable name and each source file line-or-space separated
add_executable(myprogram my_program.c)

# In order to move the position of the myprogram binary after running make
# We would put all of our executables here if we had more, but we only have one
# Executable, so we write RUNTIME
install(TARGETS myprogram RUNTIME DESTINATION ${CMAKE_SOURCE_DIR}/bin)
