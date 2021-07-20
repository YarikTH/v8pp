function(v8pp_add_plugin name)
    add_library(plugin_${name} MODULE ${name}.cpp)

    set_target_properties(plugin_${name} PROPERTIES OUTPUT_NAME "${name}" PREFIX "")
    
    target_link_libraries(plugin_${name} PRIVATE v8pp::v8pp)
endfunction()

v8pp_add_plugin(console)
v8pp_add_plugin(file)
