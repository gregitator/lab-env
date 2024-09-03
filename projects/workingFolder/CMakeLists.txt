#--------------------------------------------------------------------------
# example project
#--------------------------------------------------------------------------

PROJECT(workingFolder)
FILE(GLOB workingFolder_headers code/*.h)
FILE(GLOB workingFolder_sources code/*.cc)

SET(files_workingFolder ${workingFolder_headers} ${workingFolder_sources})
SOURCE_GROUP("workingFolder" FILES ${files_workingFolder})

ADD_EXECUTABLE(workingFolder ${files_workingFolder})
TARGET_LINK_LIBRARIES(workingFolder core render)
ADD_DEPENDENCIES(workingFolder core render)