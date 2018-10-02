# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5)
project(BoostIostreams LANGUAGES CXX)

add_library(boost_iostreams
    src/file_descriptor.cpp
	src/mapped_file.cpp
)
add_library(Boost::iostreams ALIAS boost_iostreams)

target_include_directories(boost_iostreams PUBLIC include)

target_link_libraries(boost_iostreams
    PUBLIC
        Boost::assert
        Boost::bind
        Boost::config
        Boost::core
        Boost::detail
        Boost::function
        Boost::integer
        Boost::iterator
        Boost::mpl
        Boost::preprocessor
        Boost::random
        Boost::range
        Boost::regex
        Boost::smart_ptr
        Boost::static_assert
        Boost::throw_exception
        Boost::type_traits
        Boost::utility
)

