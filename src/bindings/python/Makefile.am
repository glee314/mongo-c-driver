if ENABLE_PYTHON

pymoduledir = $(libdir)/python2.7/site-packages

pymodule_LTLIBRARIES = pymongoc.la

pymongoc_la_SOURCES = \
	src/bindings/python/pymongoc.c \
	src/bindings/python/pymongoc-client.c \
	src/bindings/python/pymongoc-client.h \
	src/bindings/python/pymongoc-client-pool.c \
	src/bindings/python/pymongoc-client-pool.h \
	src/bindings/python/pymongoc-uri.c \
	src/bindings/python/pymongoc-uri.h

pymongoc_la_LIBADD = \
	libmongoc-1.0.la \
	$(BSON_LIBS) \
	-l$(PYTHON_LIB)

pymongoc_la_LDFLAGS = -module

pymongoc_la_CPPFLAGS = \
	-DBSON_COMPILATION \
	-I$(top_srcdir)/src/mongoc \
	-I$(top_builddir)/src/mongoc \
	-I$(PYTHON_INCLUDE_DIR)

endif
