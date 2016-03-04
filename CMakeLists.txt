#
# CMakeLists.txt
# @author Omar Moreno
# @date March 01, 2016
#

# Specify the minimum CMake version required.  If the cmake version 
# minimum is not met, cmake will fail.
cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

# Set the name of the project
project(cv NONE)

# Include the file containing the CMake LaTeX macros required to build the
# document.
include(UseLATEX.cmake)

set(PDFLATEX_COMPILER xelatex)

# Add the document to the build
add_latex_document(cv.tex
    BIBFILES publications.bib 
)
