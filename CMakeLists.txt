cmake_minimum_required(VERSION 3.3)

project(test_regex)

add_subdirectory(libs)

add_executable(test_regex test.cpp)

target_link_libraries(test_regex
  boost_assert
  boost_concept_check boost_config boost_conversion boost_core
  boost_detail
  boost_function boost_function_types boost_functional boost_fusion
  boost_integer boost_iterator
  boost_mpl
  boost_optional
  boost_predef boost_preprocessor
  boost_smart_ptr boost_static_assert
  boost_throw_exception boost_tuple boost_type_index boost_type_traits boost_typeof
  boost_utility
  boost_regex)
