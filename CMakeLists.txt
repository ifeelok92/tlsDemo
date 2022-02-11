cmake_minimum_required(VERSION 3.16)
project(tlsDemo C)

set(CMAKE_C_STANDARD 17)

find_package(OpenSSL)

add_executable(tlsDemoServer src/Server.c)
target_link_libraries(tlsDemoServer PUBLIC OpenSSL::SSL)
target_link_libraries(tlsDemoServer PUBLIC OpenSSL::Crypto)

add_executable(tlsDemoClient src/Client.c)
target_link_libraries(tlsDemoClient PUBLIC OpenSSL::SSL)
target_link_libraries(tlsDemoClient PUBLIC OpenSSL::Crypto)
