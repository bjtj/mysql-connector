TESTS=$(check_PROGRAMS)

check_PROGRAMS=test-mysqlclient-database-connector

test_mysqlclient_database_connector_SOURCES=test-mysqlclient-database-connector.cpp


AM_CPPFLAGS=-I$(top_srcdir)

# cxxflags
AM_CXXFLAGS=$(PTHREAD_CXXFLAGS)
AM_CXXFLAGS+=$(LIBMYSQLCLIENT_CFLAGS)

# libs
AM_LDFLAGS=$(PTHREAD_CFLAGS)
AM_LDFLAGS+=$(LIBMYSQLCLIENT_LIBS)

# 
LDADD=../src/libmysql-connector.la
