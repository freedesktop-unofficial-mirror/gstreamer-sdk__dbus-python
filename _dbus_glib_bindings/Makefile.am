pyexec_LTLIBRARIES = _dbus_glib_bindings.la

AM_CPPFLAGS = -I$(top_srcdir)/include $(DBUS_CFLAGS) $(DBUS_GLIB_CFLAGS) \
	      $(PYTHON_INCLUDES)
AM_LDFLAGS = -module -avoid-version \
	     -export-symbols-regex \(PyInit__\|init_\)dbus_glib_bindings \
	     $(DBUS_LIBS) $(DBUS_GLIB_LIBS)

if PLATFORM_WIN32
AM_LDFLAGS += -no-undefined $(PYTHON_LIBS)
endif

_dbus_glib_bindings_la_SOURCES = module.c
