cmake_minimum_required(VERSION 3.5)

project(flywheel_connect)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/flywheel-apps/SlicerFlywheelConnect")
set(EXTENSION_CATEGORY "Informatics")
set(EXTENSION_CONTRIBUTORS "Joshua Jacobs (flywheel.io)")
set(EXTENSION_DESCRIPTION "This extension allows for downloading files from Flywheel to Slicer and uploading Slicer outputs back into Flywheel. Flywheel is a comprehensive data management solutions for life sciences and imaging research (https://flywheel.io/).")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/flywheel-apps/SlicerFlywheelConnect/master/Images/favicon.png")
set(EXTENSION_SCREENSHOTURLS "https://github.com/flywheel-apps/SlicerFlywheelConnect/blob/master/Images/TreeD_Slicer.png")
set(EXTENSION_DEPENDS "NA") # Specified as a space separated string, a list or 'NA' if any

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(FlywheelConnect)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
