cmake_minimum_required(VERSION 3.10)
project(stoken)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract( token stoken stoken.cpp )
target_include_directories( stoken PUBLIC ${CMAKE_SOURCE_DIR}/../include )
target_ricardian_directory( stoken ${CMAKE_SOURCE_DIR}/../ricardian )
# may cause cmake errors, see https://github.com/EOSIO/eosio.cdt/issues/1205

