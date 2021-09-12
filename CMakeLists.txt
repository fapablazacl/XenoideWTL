cmake_minimum_required(VERSION 3.10)

project (XenoideWTL)

set (target XenoideWTL)

set (sources
	"src/CDocumentManager.h"
    "src/CDocument.h"
    "src/CIdeFrame.h"
	"src/CClassView.h"
	"src/CFolderBrowser.h"
	"src/CDialogManager.h"

	"src/CDocumentManager.cpp"
	"src/CDocument.cpp"
	"src/CIdeFrame.cpp"
	"src/CClassView.cpp"
	"src/CFolderBrowser.cpp"
    "src/CDialogManager.cpp"
	"src/Main.cpp"

	"src/Resource.rc"
	"src/resource.h"
)

add_executable (${target} WIN32 ${sources})

# target_compile_definitions (${target} PUBLIC _UNICODE)
target_include_directories (${target} PUBLIC "src")
#target_include_directories (${target} PUBLIC "include")
#target_include_directories (${target} PUBLIC "res")
#target_include_directories (${target} PUBLIC ${XENOIDE_WTL_INCLUDE_DIR})
#target_link_libraries (${target} Xenoide.Core Xenoide.Gui)
