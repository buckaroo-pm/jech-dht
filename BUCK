load('//:buckaroo_macros.bzl', 'buckaroo_deps')

prebuilt_cxx_library(
  name = 'crypt',
  header_only = True,
  exported_linker_flags = [
    '-lcrypt',
  ],
)

cxx_library(
  name = 'dht',
  header_namespace = '',
  exported_headers = [
    'dht.h',
  ],
  srcs = [
    'dht.c',
  ],
  licenses = [
    'LICENCE',
  ],
  deps = [
    ':crypt',
  ] + buckaroo_deps(),
  visibility = [
    'PUBLIC',
  ],
)

cxx_binary(
  name = 'example',
  srcs = [
    'dht-example.c',
  ],
  deps = [
    '//:dht',
  ],
)
