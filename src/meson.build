tictactoe_sources = [
  'main.vala',
  'window.vala',
]

tictactoe_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
]

gnome = import('gnome')

tictactoe_sources += gnome.compile_resources('tictactoe-resources',
  'tictactoe.gresource.xml',
  c_name: 'tictactoe'
)

executable('tictactoe', tictactoe_sources,
  vala_args: '--target-glib=2.50',  dependencies: tictactoe_deps,
  install: true,
)
