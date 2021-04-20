# BWAPI-Lua
### Ancient and outdated Lua bindings around the [Brood War API](https://github.com/bwapi/bwapi).

I wrote this Lua wrapper for BWAPI 2.3 [back in 2009](https://code.google.com/archive/p/bwapi-lua/). BWAPI 2.3 is horribly old and no longer supported anywhere.

I've uploaded BWAPI-Lua on the offchance someone is interested in adding Lua bindings and wants to see alternatives to other (and better/newer) Lua bindings like the identically-named-but-unrelated [BWAPI-Lua](https://github.com/squeek502/BWAPI-Lua) or [TorchCraft](https://github.com/TorchCraft/TorchCraft). Updating it to a modern version (at time of writing, 4.4) should be straightforward should you endeavor to do so.

The original 2009 README follows (with minor amendments).

---

## About
BWAPI-Lua is a set of Lua bindings for BWAPI.

BWAPI-Lua is currently built against BWAPI 2.3 and supports almost all BWAPI calls. Future updates (Editor's note from 2021: LOL!) will bring it up to date with the latest stable BWAPI version and add bindings for BWTA.

## Included
The repository currently includes:

Headers and compiled static libraries for BWAPI-Lua
Headers and compiled static libraries for BWAPI 2.3 and BWTA
Headers and compiled static libraries for LuaJIT 2.0.0-beta2
MSVC++ 2008 project files

## Quick start
If you would like to try writing AIs in Lua as quickly as possible, follow these steps. This assumes working knowledge of BWAPI:

From the "Source" tab, check out the trunk
From ExampleLuaAI/lib, copy ExampleLuaAI.dll to bwapi-data/ai
From ExampleScript, copy Interface.lua to bwapi-data/ai/scripts
Edit bwapi-data/bwapi.ini, set ai_dll = bwapi-data\ai\ExampleLuaAI.dll
From the BWAPI homepage, get a copy of BWAPI 2.3 and follow installation instructions

## Calling BWAPI from Lua
The Lua version of BWAPI isn't yet documented, but the names usually map directly to BWAPI methods:

UnitType::getName() --> unitTypeGetName( MY_UNIT_TYPE )

If in doubt, refer to the BWAPI-Lua/source/Binder/BWAPI for the Lua name.

---

## License
BWAPI-Lua is MIT licensed. See LICENSE for terms. This repository includes BWAPI 2.3 and an equally old version of LuaJIT, distributed under terms of their respective licenses (which are also MIT-based).