# SPDX-FileCopyrightText:  2023 Andy Curtis <contactandyc@gmail.com>
# SPDX-License-Identifier: Apache-2.0
cmake_minimum_required(VERSION 3.10)
project(a_tokenizer_library_example VERSION 1.0)

# Enable testing
enable_testing()

# Set the directory for test sources
set(TEST_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/src/parse.c ${CMAKE_CURRENT_SOURCE_DIR}/src/parse_expression.c)

set(CUSTOM_PACKAGES a-tokenizer-library a-json-library a-memory-library the-macro-library the-lz4-library the-io-library)
set(THIRD_PARTY_PACKAGES ZLIB)

find_package(a-cmake-library REQUIRED)

include(BinaryConfig)
