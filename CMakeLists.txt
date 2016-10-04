cmake_minimum_required(VERSION 3.3)

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

option(BOOST_REGEX_USE_ICU "Enable support for ICU" OFF)

project(test_regex)

add_subdirectory(libs)

add_executable(test_regex test.cpp)

if(BOOST_REGEX_USE_ICU)
  target_link_libraries(test_regex ICU::ICU)
endif(BOOST_REGEX_USE_ICU)

target_link_libraries(test_regex
  boost::assert
  boost::concept_check boost::config boost::conversion boost::core
  boost::detail
  boost::function boost::function_types boost::functional boost::fusion
  boost::integer boost::iterator
  boost::mpl
  boost::optional
  boost::predef boost::preprocessor
  boost::smart_ptr boost::static_assert
  boost::throw_exception boost::tuple boost::type_index boost::type_traits boost::typeof
  boost::utility
  boost::regex)
