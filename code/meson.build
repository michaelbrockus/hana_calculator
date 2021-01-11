chicken_stack = subproject('chicken-stack')

code_lib = static_library('code_lib', files('program.c'),
    dependencies : [chicken_stack.get_variable('chicken_stack_dep')],
    include_directories: '.',
    install: true)

code_dep = declare_dependency(
    link_with: code_lib,
    include_directories: '.')

executable('hana-calc', files('main.c'), dependencies: code_dep, install: true)
