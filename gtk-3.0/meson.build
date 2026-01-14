gtk3_dir = join_paths(theme_path, 'gtk-3.0')

gtk3_scss_deps = files([
  '_colors-public.scss',
  '_colors.scss',
  '_common.scss',
  '_drawing.scss',
])

theme_variants = [
  'dark',
]

gtk3_scss_sources = [
  'gtk',
  'gtk-dark',
]

foreach src : gtk3_scss_sources
  custom_target('effigy-' + src,
    input: src + '.scss',
    output: src + '.css',
    command: [
      sassc, sassc_opts, '@INPUT@', '@OUTPUT@',
    ],
    depend_files: gtk3_scss_deps,
    build_by_default: true,
    install: true,
    install_dir: gtk3_dir,
  )
endforeach

install_subdir('assets', install_dir : gtk3_dir, strip_directory : false)
