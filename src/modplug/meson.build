modplug_dep = dependency('libmodplug', required: false)


modplug_archive_sources = [
  'archive/arch_raw.cc',
  'archive/archive.cc',
  'archive/open.cc'
]


modplug_plugin_sources = [
  'modplugbmp.cc',
  'plugin_main.cc'
]


if modplug_dep.found()
  shared_module('modplug',
    modplug_archive_sources,
    modplug_plugin_sources,
    dependencies: [audacious_dep, modplug_dep],
    include_directories: [src_inc],
    install: true,
    install_dir: input_plugin_dir,
  )
endif

