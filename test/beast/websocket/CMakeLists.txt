#
# Copyright (c) 2016-2017 Vinnie Falco (vinnie dot falco at gmail dot com)
#
# Distributed under the Boost Software License, Version 1.0. (See accompanying
# file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)
#
# Official repository: https://github.com/boostorg/beast
#

GroupSources(test/extras/include/boost/beast extras)
GroupSources(include/boost/beast beast)
GroupSources(test/beast/websocket "/")

add_executable (tests-beast-websocket
    ${BOOST_BEAST_INCLUDES}
    ${EXTRAS_INCLUDES}
    ${TEST_MAIN}
    Jamfile
    test.hpp
    accept.cpp
    close.cpp
    error.cpp
    handshake.cpp
    option.cpp
    ping.cpp
    read.cpp
    rfc6455.cpp
    role.cpp
    stream.cpp
    teardown.cpp
    frame.cpp
    mask.cpp
    utf8_checker.cpp
    write.cpp
)
