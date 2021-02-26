project('zlib', 'c', version: '1.2.11')

compiler = meson.get_compiler('c')
link_deps = [
]

incdirs = ['.']

sources = [
	'adler32.c',
	'compress.c',
	'crc32.c',
	'uncompr.c',
	'deflate.c',
	'trees.c',
	'gzlib.c',
	'gzclose.c',
	'gzread.c',
	'gzwrite.c',
	'zutil.c',
	'inflate.c',
	'infback.c',
	'inftrees.c',
	'inffast.c',
]

incdirs = include_directories(incdirs)

lib = static_library(
    'z',
    sources,
    include_directories: incdirs,
    dependencies: link_deps,
)

zlib_dep = declare_dependency(
    include_directories: incdirs,
    dependencies: link_deps,
    link_with: lib,
    version: meson.project_version()
)

meson.override_dependency('zlib', zlib_dep)

# vim: set ts=4 sts=4 sw=4 et:
