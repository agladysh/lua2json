lua2json – A command-line tool to convert Lua to JSON
=====================================================

See the copyright information in the file named `COPYRIGHT`.

Usage:
------

`lua2json [options] < data.lua > data.json`

### Options:

    -h    Print help
    -v    Print script version
    -O    Force tables to be serialized as objects
          (default: off)
    -e    Do not print terminating EOL (default: do print)
    -r    Prefix "return " to the input before loading (default: do not prefix)

Dependencies
------------

### luajson

All actual work on JSON data is done here.

    sudo luarocks install luajson

Installation:
-------------

1. Install dependencies (see above).

2. Install lua2json:

  A. Copy / symlink it somewhere in path
  
  -- or --
  
  B. Install it with LuaRocks:

  Stable version:
  
      sudo luarocks install lua2json

  Developer version:

      sudo luarocks install \
        lua2json \
        --from=http://luarocks.org/repositories/rocks-cvs
  
  Note that LuaRocks 2.0.2 and below reset executable bit
  on the installed binaries. To ensure that lua2json is executable,
  run following command after installation:
  
      sudo chmod +x $(command -v lua2json)

  If you're using LuaRocks 2.0.3 and above, chmod is not needed.
