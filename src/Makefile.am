lib_LTLIBRARIES = libmysql-connector.la

libmysql_connector_la_SOURCES=mysql-connector.cpp

libmysql_connector_la_CXXFLAGS=$(PTHREAD_CXXFLAGS) $(LIBMYSQLCLIENT_CFLAGS) -I$(top_srcdir)
libmysql_connector_la_CXXFLAGS+=$(LIBOSLAYER_CFLAGS)
libmysql_connector_la_LIBADD=$(LIBOSLAYER_LIBS)
libmysql_connector_la_LDFLAGS=$(PTHREAD_CFLAGS) $(LIBMYSQLCLIENT_LIBS)

