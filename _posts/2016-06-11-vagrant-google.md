[cloud-user@controller ~]$ curl -O https://releases.hashicorp.com/vagrant/1.8.3/vagrant_1.8.3_x86_64.rpm
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 72.3M  100 72.3M    0     0   105M      0 --:--:-- --:--:-- --:--:--  105M
[cloud-user@controller ~]$ rpm -i vagrant_1.8.3_x86_64.rpm
error: can't create transaction lock on /var/lib/rpm/.rpm.lock (Permission denied)
[cloud-user@controller ~]$ sudo rpm -i vagrant_1.8.3_x86_64.rpm
[cloud-user@controller ~]$ vagrant --version
Vagrant 1.8.3
[cloud-user@controller ~]$ vagrant plugin install vagrant-google

sudo yum -y install ruby

ruby -v

Complete!
[cloud-user@controller ~]$ ruby -v
ruby 2.0.0p598 (2014-11-13) [x86_64-linux]
[cloud-user@controller ~]$

[cloud-user@controller ~]$ vagrant plugin install vagrant-google
Installing the 'vagrant-google' plugin. This can take a few minutes...
/opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:303:in `block in sort_dependencies': undefined method `payload' for nil:NilClass (NoMethodError)
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `each'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_by'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_dependencies'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:131:in `block (2 levels) in <class:Resolution>'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:431:in `push_state_for_requirements'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:423:in `require_nested_dependencies_for'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:411:in `activate_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:353:in `attempt_to_swap_possibility'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:333:in `attempt_to_activate_existing_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:318:in `attempt_to_activate'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:147:in `process_topmost_state'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:72:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolver.rb:42:in `resolve'
## 

        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:201:in `start'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:184:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:200:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:140:in `specs'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:129:in `resolve_remotely!'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:195:in `resolve_if_need'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:70:in `run'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:22:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:230:in `block in internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:290:in `block in with_isolated_gem'
        from /opt/vagrant/embedded/lib/ruby/2.2.0/rubygems/user_interaction.rb:45:in `use_ui'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:289:in `with_isolated_gem'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:229:in `internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:102:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:62:in `block in install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/action/install_gem.rb:37:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/warden.rb:34:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/builder.rb:116:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `block in run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/util/busy.rb:19:in `busy'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/base.rb:14:in `action'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:32:in `block in execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `each'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/root.rb:56:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/cli.rb:42:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/environment.rb:302:in `cli'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/bin/vagrant:174:in `<main>'
[cloud-user@controller ~]$



sudo yum -y install ruby

ruby -v

Complete!
[cloud-user@controller ~]$ ruby -v
ruby 2.0.0p598 (2014-11-13) [x86_64-linux]
[cloud-user@controller ~]$

[cloud-user@controller ~]$ vagrant plugin install vagrant-google
Installing the 'vagrant-google' plugin. This can take a few minutes...
/opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:303:in `block in sort_dependencies': undefined method `payload' for nil:NilClass (NoMethodError)
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `each'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_by'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_dependencies'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:131:in `block (2 levels) in <class:Resolution>'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:431:in `push_state_for_requirements'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:423:in `require_nested_dependencies_for'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:411:in `activate_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:353:in `attempt_to_swap_possibility'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:333:in `attempt_to_activate_existing_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:318:in `attempt_to_activate'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:147:in `process_topmost_state'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:72:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolver.rb:42:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:201:in `start'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:184:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:200:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:140:in `specs'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:129:in `resolve_remotely!'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:195:in `resolve_if_need'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:70:in `run'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:22:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:230:in `block in internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:290:in `block in with_isolated_gem'
        from /opt/vagrant/embedded/lib/ruby/2.2.0/rubygems/user_interaction.rb:45:in `use_ui'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:289:in `with_isolated_gem'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:229:in `internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:102:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:62:in `block in install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/action/install_gem.rb:37:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/warden.rb:34:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/builder.rb:116:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `block in run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/util/busy.rb:19:in `busy'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/base.rb:14:in `action'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:32:in `block in execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `each'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/root.rb:56:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/cli.rb:42:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/environment.rb:302:in `cli'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/bin/vagrant:174:in `<main>'
[cloud-user@controller ~]$



sudo yum -y install ruby

ruby -v

Complete!
[cloud-user@controller ~]$ ruby -v
ruby 2.0.0p598 (2014-11-13) [x86_64-linux]
[cloud-user@controller ~]$

[cloud-user@controller ~]$ vagrant plugin install vagrant-google
Installing the 'vagrant-google' plugin. This can take a few minutes...
/opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:303:in `block in sort_dependencies': undefined method `payload' for nil:NilClass (NoMethodError)
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `each'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_by'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_dependencies'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:131:in `block (2 levels) in <class:Resolution>'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:431:in `push_state_for_requirements'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:423:in `require_nested_dependencies_for'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:411:in `activate_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:353:in `attempt_to_swap_possibility'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:333:in `attempt_to_activate_existing_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:318:in `attempt_to_activate'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:147:in `process_topmost_state'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:72:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolver.rb:42:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:201:in `start'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:184:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:200:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:140:in `specs'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:129:in `resolve_remotely!'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:195:in `resolve_if_need'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:70:in `run'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:22:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:230:in `block in internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:290:in `block in with_isolated_gem'
        from /opt/vagrant/embedded/lib/ruby/2.2.0/rubygems/user_interaction.rb:45:in `use_ui'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:289:in `with_isolated_gem'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:229:in `internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:102:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:62:in `block in install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/action/install_gem.rb:37:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/warden.rb:34:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/builder.rb:116:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `block in run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/util/busy.rb:19:in `busy'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/base.rb:14:in `action'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:32:in `block in execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `each'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/root.rb:56:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/cli.rb:42:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/environment.rb:302:in `cli'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/bin/vagrant:174:in `<main>'
[cloud-user@controller ~]$



sudo yum -y install ruby

ruby -v

Complete!
[cloud-user@controller ~]$ ruby -v
ruby 2.0.0p598 (2014-11-13) [x86_64-linux]
[cloud-user@controller ~]$

[cloud-user@controller ~]$ vagrant plugin install vagrant-google
Installing the 'vagrant-google' plugin. This can take a few minutes...
/opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:303:in `block in sort_dependencies': undefined method `payload' for nil:NilClass (NoMethodError)
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `each'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_by'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:300:in `sort_dependencies'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:131:in `block (2 levels) in <class:Resolution>'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:431:in `push_state_for_requirements'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:423:in `require_nested_dependencies_for'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:411:in `activate_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:353:in `attempt_to_swap_possibility'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:333:in `attempt_to_activate_existing_spec'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:318:in `attempt_to_activate'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:147:in `process_topmost_state'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolution.rb:72:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/vendor/molinillo/lib/molinillo/resolver.rb:42:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:201:in `start'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/resolver.rb:184:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:200:in `resolve'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:140:in `specs'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/definition.rb:129:in `resolve_remotely!'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:195:in `resolve_if_need'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:70:in `run'
        from /opt/vagrant/embedded/gems/gems/bundler-1.12.0/lib/bundler/installer.rb:22:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:230:in `block in internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:290:in `block in with_isolated_gem'
        from /opt/vagrant/embedded/lib/ruby/2.2.0/rubygems/user_interaction.rb:45:in `use_ui'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:289:in `with_isolated_gem'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:229:in `internal_install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/bundler.rb:102:in `install'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:62:in `block in install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/plugin/manager.rb:72:in `install_plugin'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/action/install_gem.rb:37:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/warden.rb:34:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/builder.rb:116:in `call'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `block in run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/util/busy.rb:19:in `busy'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/action/runner.rb:66:in `run'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/base.rb:14:in `action'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:32:in `block in execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `each'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/install.rb:31:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/plugins/commands/plugin/command/root.rb:56:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/cli.rb:42:in `execute'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/lib/vagrant/environment.rb:302:in `cli'
        from /opt/vagrant/embedded/gems/gems/vagrant-1.8.3/bin/vagrant:174:in `<main>'
[cloud-user@controller ~]$


... Fehler

Das gleiche auf der WIndows Ebene:

vagrant plugin install vagrant-google ist erfolgreich

C:\Users\Robert>vagrant plugin install vagrant-google
Installing the 'vagrant-google' plugin. This can take a few minutes...
Installed the plugin 'vagrant-google (0.2.4)'!

C:\Users\Robert>cd Workspace\Boxes\openshift-gce

C:\Users\Robert\Workspace\Boxes\openshift-gce>cat Vagrantfile
# -*- mode: ruby -*-
# vi: set ft=ruby :


VAGRANTFILE_API_VERSION = "2"
Vagrant.require_version ">= 1.7.2"

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version. Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.box = "gce"

  config.vm.provider :google do |google, override|
     google.google_project_id = "xxxxxxxxxxxxxxxxxxxx"
     google.google_client_email = "xxxxxxxxxxxxxxxxxxxxxxxxxx"
     google.google_json_key_location = "gce-credentials"

     override.ssh.username = "xxxxxx"
     override.ssh.private_key_path = "google_compute_engine"

  end

end

C:\Users\Robert\Workspace\Boxes\openshift-gce>vagrant up --provider=google
C:/HashiCorp/Vagrant/embedded/gems/gems/nokogiri-1.6.3.1-x86-mingw32/lib/nokogiri.rb:29:in `require': cannot load such file -- nokogiri/nokogiri (LoadError)
        from C:/HashiCorp/Vagrant/embedded/gems/gems/nokogiri-1.6.3.1-x86-mingw32/lib/nokogiri.rb:29:in `rescue in <top (required)>'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/nokogiri-1.6.3.1-x86-mingw32/lib/nokogiri.rb:25:in `<top (required)>'
        from C:/Users/Robert/.vagrant.d/gems/gems/fog-xml-0.1.2/lib/fog/xml.rb:2:in `require'
        from C:/Users/Robert/.vagrant.d/gems/gems/fog-xml-0.1.2/lib/fog/xml.rb:2:in `<top (required)>'
        from C:/Users/Robert/.vagrant.d/gems/gems/fog-google-0.2.0/lib/fog/google.rb:3:in `require'
        from C:/Users/Robert/.vagrant.d/gems/gems/fog-google-0.2.0/lib/fog/google.rb:3:in `<top (required)>'
        from C:/Users/Robert/.vagrant.d/gems/gems/vagrant-google-0.2.4/lib/vagrant-google/action/connect_google.rb:14:in `require'
        from C:/Users/Robert/.vagrant.d/gems/gems/vagrant-google-0.2.4/lib/vagrant-google/action/connect_google.rb:14:in `<top (required)>'
        from C:/Users/Robert/.vagrant.d/gems/gems/vagrant-google-0.2.4/lib/vagrant-google/action.rb:91:in `block in action_read_state'
        from C:/Users/Robert/.vagrant.d/gems/gems/vagrant-google-0.2.4/lib/vagrant-google/action.rb:89:in `tap'
        from C:/Users/Robert/.vagrant.d/gems/gems/vagrant-google-0.2.4/lib/vagrant-google/action.rb:89:in `action_read_state'
        from C:/Users/Robert/.vagrant.d/gems/gems/vagrant-google-0.2.4/lib/vagrant-google/provider.rb:29:in `action'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/machine.rb:187:in `block in action'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:561:in `lock'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/machine.rb:185:in `call'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/machine.rb:185:in `action'
        from C:/Users/Robert/.vagrant.d/gems/gems/vagrant-google-0.2.4/lib/vagrant-google/provider.rb:45:in `state'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/machine.rb:501:in `state'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/machine.rb:144:in `initialize'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/vagrantfile.rb:79:in `new'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/vagrantfile.rb:79:in `machine'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:663:in `machine'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/plugin/v2/command.rb:177:in `block in with_target_vms'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/plugin/v2/command.rb:201:in `call'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/plugin/v2/command.rb:201:in `block in with_target_vms'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/plugin/v2/command.rb:183:in `each'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/plugin/v2/command.rb:183:in `with_target_vms'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/plugins/commands/up/command.rb:89:in `block in execute'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:278:in `block (2 levels) in batch'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:276:in `tap'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:276:in `block in batch'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:275:in `synchronize'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:275:in `batch'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/plugins/commands/up/command.rb:88:in `execute'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/cli.rb:42:in `execute'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/lib/vagrant/environment.rb:302:in `cli'
        from C:/HashiCorp/Vagrant/embedded/gems/gems/vagrant-1.8.1/bin/vagrant:174:in `<main>'

C:\Users\Robert\Workspace\Boxes\openshift-gce>




















