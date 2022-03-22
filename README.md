# NAME

Alien::7zip - Find or build 7-Zip

# SYNOPSIS

Command line tool:

    use Alien::7zip;
    use Env qw( @PATH );

    unshift @PATH, Alien::7zip->bin_dir;
    system "@{[ Alien::7zip->exe ]}";

# DESCRIPTION

This distribution provides 7-Zip so that it can be used by other
Perl distributions that are on CPAN.  It does this by first trying to
detect an existing install of 7-Zip on your system.  If found it
will use that.  If it cannot be found, the source code will be downloaded
from the internet and it will be installed in a private share location
for the use of other modules.

# METHODS

## exe

    Alien::7zip->exe

Returns the command name for running 7-Zip.

# HELPERS

## 7z

    %{7z}

Returns '7z', '7zz', or appropriate command for
platform.

# SEE ALSO

- [7-Zip](https://www.7-zip.org/)

    The 7-Zip home page.

- [Alien](https://metacpan.org/pod/Alien)

    Documentation on the Alien concept itself.

- [Alien::Base](https://metacpan.org/pod/Alien%3A%3ABase)

    The base class for this Alien.

- [Alien::Build::Manual::AlienUser](https://metacpan.org/pod/Alien%3A%3ABuild%3A%3AManual%3A%3AAlienUser)

    Detailed manual for users of Alien classes.
