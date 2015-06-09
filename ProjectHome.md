iText has dependencies on certain Java classes (java.awt.Color,
java.nio.MappedByteBuffer etc.) which are  not  allowed by the Google AppEngine runtime (see
http://code.google.com/appengine/docs/java/jrewhitelist.html). Google App Engine throws an exception e.g "java.lang.NoClassDefFoundError:
java.nio.MappedByteBuffer is a restricted class. Please see the Google App Engine developer's guide for more details." is thrown for the unsupported class(es).

- Would it be possible to remove the dependency by iText on these Java classes, so as to enable the library to work within Google App Engine?

See attached (very rough) Subversion patch file, for how I quickly removed some of the dependencies, so as to get iText to process a PDF form within Google App Engine.