project('Effigy')

sassc = find_program('sass', required: true)

if get_option('generate_sourcemaps')
    sassc_opts = [ '--source-map' ]
else
    sassc_opts = [ '--no-source-map' ]
endif

glib_compile_resources = find_program('glib-compile-resources', required: true)

theme_deps = []
theme_path = join_paths(get_option('datadir'), 'themes/Effigy')

subdir('gtk-3.0')

install_data('index.theme', install_dir : theme_path)
