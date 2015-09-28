# NAME

Catalyst::View::MicroTemplate::DataSection - Text::MicroTemplate::DataSection View For Catalyst

# SYNOPSIS

     # subclassing to making your view class
     package MyApp::View::DataSection;
     use Moose;
     extends 'Catalyst::View::MicroTemplate::DataSection';
     1;

     # using in a controller
     sub index :Path :Args(0) {
         my ( $self, $c ) = @_; 
         $c->stash->{username} = 'masakyst';
     }
     ...
     ..
     __PACKAGE__->meta->make_immutable;

     1;
     __DATA__
    
     @@ index.mt
     ? my $stash = shift;
     hello <?= $stash->{username} ?> !!

# DESCRIPTION

Catalyst::View::MicroTemplate::DataSection is simple wrapper module allows you to render MicroTemplate template from \_\_DATA\_\_ section in Catalyst controller.

# SEE ALSO

- [Text::MicroTemplate::DataSection](https://metacpan.org/pod/Text::MicroTemplate::DataSection)
- [Data::Section::Simple](https://metacpan.org/pod/Data::Section::Simple)

# LICENSE

Copyright (C) Masaaki Saito.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

Masaaki Saito &lt;masakyst.public@gmail.com>
