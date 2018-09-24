cmake_minimum_required(VERSION 2.8)

project(libp11)
include_directories("C:\\OpenSSL-Win32\\include")

link_directories("C:\\OpenSSL-Win32\\lib")
add_library(${PROJECT_NAME} SHARED
    "./src/eng_back.c"
    "./src/eng_parse.c"
    "./src/p11_atfork.c"
    "./src/p11_ec.c"
    "./src/p11_load.c"
    "./src/pkcs11.exports"
    "./src/eng_err.c"
    "./src/p11_attr.c"
    "./src/p11_err.c"
    "./src/p11_misc.c"
    "./src/libpkcs11.c"
    "./src/p11_cert.c"
    "./src/p11_pkey.c"
    "./src/eng_front.c"
    "./src/p11_ckr.c"
    "./src/p11_front.c"
    "./src/p11_rsa.c"
    "./src/p11_key.c"
    "./src/p11_slot.c")

target_link_libraries(${PROJECT_NAME} "libcrypto")
