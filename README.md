# JSON::Ext reproduction


In order to run the script with the 1.7.x version of JRuby, use `./gradlew spec`.

In order to run it with the 9000 preview1, use: `JRUBY=9k ./gradlew spec`

Example:

    ➜  json-9kp1-bug git:(master) ✗ ./gradlew spec
    :spec
    .
    
    Finished in 0.011 seconds (files took 1.41 seconds to load)
    1 example, 0 failures
    
    BUILD SUCCESSFUL
    
    Total time: 8.327 secs
    ➜  json-9kp1-bug git:(master) ✗ JRUBY=9k ./gradlew spec
    :spec
    NameError: uninitialized constant JSON::Ext::Parser
        const_missing at org/jruby/RubyModule.java:2935
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/json-1.8.2-java/lib/json/ext.rb:16
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/json-1.8.2-java/lib/json.rb:1
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/json-1.8.2-java/lib/json.rb:58
              require at org/jruby/RubyKernel.java:954
           __script__ at uri:classloader:/META-INF/jruby.home/lib/ruby/stdlib/rubygems/core_ext/kernel_require.rb:69
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/activesupport-4.2.0/lib/active_support/json/decoding.rb:1
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/activesupport-4.2.0/lib/active_support/json/decoding.rb:3
              require at org/jruby/RubyKernel.java:954
           __script__ at uri:classloader:/META-INF/jruby.home/lib/ruby/stdlib/rubygems/core_ext/kernel_require.rb:69
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/activesupport-4.2.0/lib/active_support/json.rb:1
              require at org/jruby/RubyKernel.java:954
           __script__ at uri:classloader:/META-INF/jruby.home/lib/ruby/stdlib/rubygems/core_ext/kernel_require.rb:69
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/activesupport-4.2.0/lib/active_support/json.rb:1
              require at org/jruby/RubyKernel.java:954
           __script__ at uri:classloader:/META-INF/jruby.home/lib/ruby/stdlib/rubygems/core_ext/kernel_require.rb:128
               (root) at /home/tyler/source/github/json-9kp1-bug/spec/some_spec.rb:1
                 load at org/jruby/RubyKernel.java:969
               (root) at /home/tyler/source/github/json-9kp1-bug/spec/some_spec.rb:2
                 each at org/jruby/RubyArray.java:1569
               (root) at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/rspec-core-3.1.7/lib/rspec/core/configuration.rb:1
      load_spec_files at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/rspec-core-3.1.7/lib/rspec/core/configuration.rb:1105
      load_spec_files at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/rspec-core-3.1.7/lib/rspec/core/configuration.rb:1105
                setup at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/rspec-core-3.1.7/lib/rspec/core/runner.rb:96
                  run at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/rspec-core-3.1.7/lib/rspec/core/runner.rb:84
                  run at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/gems/rspec-core-3.1.7/lib/rspec/core/runner.rb:69
                 load at org/jruby/RubyKernel.java:969
           __script__ at /home/tyler/source/github/json-9kp1-bug/build/tmp/jrubyExec/bin/rspec:23
    :spec FAILED
    
    FAILURE: Build failed with an exception.
    
    * What went wrong:
    Execution failed for task ':spec'.
    > Process 'command '/home/tyler/scratch/tools/jdk1.8.0_25/bin/java'' finished with non-zero exit value 1
    
    * Try:
    Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.
    
    BUILD FAILED
    
    Total time: 8.752 secs
    ➜  json-9kp1-bug git:(master) ✗ 
    
