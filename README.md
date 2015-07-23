# Luadch - ADC Hub Server

## Features:

    - Encryption, AES128 and AES256 cipher suites with TLSv1.2 support
    - Fast, stable and small (complete server has ~1,5 MB)
    - Supports ARM architecture
    - Easy to use Lua Scripting API
    - Many additional scripts available
    - Comfortable rightclick menu

## To run a Luadch Hub:

1. Without encryption, start the Hub and login with:

    Nick: dummy
    Password: test
    Address: adc://127.0.0.1:5000

2. With encryption:

    - go to: �certs/� and start �make_cert.sh� on Linux/Unix or �make_cert.bat� on Windows to generate the certificates
    - alternatively you can use the Luadch Certmanager
    - after that you can login with:

       Nick: dummy
       Password: test
       Address: adcs://127.0.0.1:5001

3. Register an own nickname for you, there are two possibillities to do that:

    - use rightclick menu: User/Control/Reg
    - use command: +reg nick <Nick> <Level>

    Where <Nick> is your new nickname and <Level> should be the highest level 100

4. Now delete the dummy account, there are two possibillities to do that:

    - use rightclick menu: User/Control/Delreg
    - use command: +delreg nick <Nick>

5. After this first test you should adapt the hub to your needs:

    - open: �cfg/cfg.tbl� with a UTF-8 compatible Texteditor best with Lua syntax highlighting
    - Read the descriptions and set the values to your need, Luadch uses a fair and reasonable default user permissions, but nevertheless you should read all

6. If it's done, start your hub again and login, if he still runs there are to possibillities to enable your changes in the hub:

    - use rightclick menu: Hub/Core/Hub reload
    - use command: +reload

7. If you want to set other styles for lines or something:

    - go to: �scripts/lang/� here you can find all language files for each script, after that: hub reload

## Done


## Note:

    If you compiling the source from a Windows x64 host you need to know:
    There is a 32bit/64bit bug in the Microsoft "msvcrt", the size of "time_t" in os.difftime() was not
    interpreted correctly. if you skirt this issue use the precompiled "lua/tmp/lua.dll". if you want to
    know more about this problem read this:
    http://www.marshut.com/ikhziq/building-on-windows-from-scratch.html#inrpiz