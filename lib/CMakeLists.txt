# Option 1.
# add_executable(mytest test.c ../lib/Unity/src/unity.c)

# Option 2.
# mytest is the "target" (name of executable)
# who cares its PUBLIC
# target_include_directories(mytest PUBLIC ${CMAKE_SOURCE_DIR}/lib/Unity/src)

# Option 3.
# The BEST option according to Raka
# Cleanest
# Easiest
# STATIC 
add_library(Unity STATIC Unity/src/unity.c)

# Target is Unity (library or executable)
# Always PUBLIC
target_include_directories(Unity PUBLIC Unity/src)
