# NAME

Kelp::Module::Config::ConfigGeneral - Config::General in your Kelp application

# SYNOPSIS

    # app.psgi
    use MyApp;
    my $app = MyApp->new( config_module => 'Config::ConfigGeneral' );
    $app->run;

# DESCRIPTION

This module provides support of [Config::General](https://metacpan.org/pod/Config::General) in your [Kelp](https://metacpan.org/pod/Kelp) applications.

Because [Config::General](https://metacpan.org/pod/Config::General) provides key/value interface you are not able to create array of arrays for your [Kelp::Module::Logger](https://metacpan.org/pod/Kelp::Module::Logger) configuration. This module does it for you.

Example:
    modules = \[ Logger \]

    <modules_init Logger>
      <outputs Screen>
         name      debug
         min_level debug
         newline   1
         binmode   :encoding(UTF-8)
      </outputs>
      <outputs Screen>
         name      error
         min_level error
         newline   1
         stderr    1
         binmode   :encoding(UTF-8)
      </outputs>
    </modules_init>

# AUTHOR

Konstantin Yakunin <twinhooker@gmail.com>

# COPYRIGHT

Copyright 2017- Konstantin Yakunin

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
