#
# Copyright (c) 2016-2017 Vinnie Falco (vinnie dot falco at gmail dot com)
#
# Distributed under the Boost Software License, Version 1.0. (See accompanying
# file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)
#
# Official repository: https://github.com/boostorg/beast
#

GroupSources(include/boost/beast beast)
GroupSources(example/common common)
GroupSources(example/websocket/client/coro-ssl "/")

add_executable (websocket-client-coro-ssl
    ${BOOST_BEAST_INCLUDES}
    ${PROJECT_SOURCE_DIR}/example/common/root_certificates.hpp
    Jamfile
    websocket_client_coro_ssl.cpp
)

target_link_libraries (websocket-client-coro-ssl
    ${OPENSSL_LIBRARIES}
    )
