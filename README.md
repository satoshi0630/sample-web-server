# sample-web-server
テクノロジー（藤原）Node.jsによるサンプルWebサーバ

```
Last login: Fri Jun 14 11:26:59 on ttys000
takedareishinoMacBook-Pro:~ takedasatoshi$ cd ~/fujiwara
takedareishinoMacBook-Pro:fujiwara takedasatoshi$ cd sample-web-server
takedareishinoMacBook-Pro:sample-web-server takedasatoshi$ ls
README.md	mywebapi	thecat.json
takedareishinoMacBook-Pro:sample-web-server takedasatoshi$ cd mywebapi
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ ls
index.js		package-lock.json	web
node_modules		package.json
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ node index.js
-bash: node: command not found
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ nodebrew use latest
-bash: nodebrew: command not found
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ nodebrew install-binary latest
-bash: nodebrew: command not found
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ curl -L git.io/nodebrew | perl - setup
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
  0     0    0     0    0     0      0      0 --:--:--  0:00:02 --:--:--     0
  0     0    0     0    0     0      0      0 --:--:--  0:00:02 --:--:--     0
100 24634  100 24634    0     0   7064      0  0:00:03  0:00:03 --:--:--  7064
Fetching nodebrew...
Installed nodebrew in $HOME/.nodebrew

========================================
Export a path to nodebrew:

export PATH=$HOME/.nodebrew/current/bin:$PATH
========================================
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ export PATH=$HOME/.nodebrew/current/bin:$PATH >> ~/.bashrc
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ source ~/.bashrc
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ nodebrew
nodebrew 1.0.1

Usage:
    nodebrew help                         Show this message
    nodebrew install <version>            Download and install <version> (from binary)
    nodebrew compile <version>            Download and install <version> (from source)
    nodebrew install-binary <version>     Alias of `install` (For backward compatibility)
    nodebrew uninstall <version>          Uninstall <version>
    nodebrew use <version>                Use <version>
    nodebrew list                         List installed versions
    nodebrew ls                           Alias for `list`
    nodebrew ls-remote                    List remote versions
    nodebrew ls-all                       List remote and installed versions
    nodebrew alias <key> <value>          Set alias
    nodebrew unalias <key>                Remove alias
    nodebrew clean <version> | all        Remove source file
    nodebrew selfupdate                   Update nodebrew
    nodebrew migrate-package <version>    Install global NPM packages contained in <version> to current version
    nodebrew exec <version> -- <command>  Execute <command> using specified <version>

Example:
    # install
    nodebrew install v8.9.4

    # use a specific version number
    nodebrew use v8.9.4
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ nodebrew install-binary latest
v12.4.0 is already installed
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ nodebrew ls
v12.4.0

current: v12.4.0
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ nodebrew ls
v12.4.0

current: v12.4.0
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ node -v
v12.4.0
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ node index.js
/Users/takedasatoshi/Documents/fujiwara/sample-web-server/mywebapi/index.js:8
app.use(express.stadic('web'));
                ^

TypeError: express.stadic is not a function
    at Object.<anonymous> (/Users/takedasatoshi/Documents/fujiwara/sample-web-server/mywebapi/index.js:8:17)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ node index.js
/Users/takedasatoshi/Documents/fujiwara/sample-web-server/mywebapi/index.js:8
app.use(express.stadic('web'));
                ^

TypeError: express.stadic is not a function
    at Object.<anonymous> (/Users/takedasatoshi/Documents/fujiwara/sample-web-server/mywebapi/index.js:8:17)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ ls
index.js		package-lock.json	web
node_modules		package.json
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ cd web
takedareishinoMacBook-Pro:web takedasatoshi$ ls
index.html
takedareishinoMacBook-Pro:web takedasatoshi$ vi index.html
takedareishinoMacBook-Pro:web takedasatoshi$ cd ..
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ node index.js
/Users/takedasatoshi/Documents/fujiwara/sample-web-server/mywebapi/index.js:8
app.use(express.stadic('web'));
                ^

TypeError: express.stadic is not a function
    at Object.<anonymous> (/Users/takedasatoshi/Documents/fujiwara/sample-web-server/mywebapi/index.js:8:17)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ vi index.js
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ node index.js
Listening on port 3000
^C
takedareishinoMacBook-Pro:mywebapi takedasatoshi$ 


```
