# vscode-ts-node-problems
This repo just exists for the purpose of helping reproduce a problem seen with VS Code and ts-node

## Reproducing the Problem
1. Clone this repo
2. If you are using `volta`, run `npm install`. If you are using some other way to bootstrap your `node` and `npm` versions, install `node` 20.18.0 and `npm` 10.8.2. (It might work with other versions. This is just what I tested.) Then run `npm install`.
3. In VS Code, run the one configuration available, `Run Test`. You should see `Hello World 1` and `Hello World 2` printed to the console.
4. In VS Code, set a breakpoint on the `Hello World 2` line and start the `Run Test` configuration in the VS Code debugger. Sometimes it will work, and sometimes it will fail with error code 139. The failure only happens when breakpoints are set.

## Environment for Reproducing
I just got a new dev machine, and I never saw any problems with it on my old machine. My new dev machine has a "Intel(R) Core(TM) i7-14700 2.10 GHz" CPU which has far more cores than my previous machine. I haven't noticed any other problems in any other software, so it's not obviously a hardware flaw specific to this machine.

I ran these tests in 2 different versions of Ubuntu in WSL2 (on Windows 11) with the same results:
```
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.1 LTS
Release:        24.04
Codename:       noble
```
and
```
Distributor ID: Ubuntu
Description:    Ubuntu 22.04.5 LTS
Release:        22.04
Codename:       jammy
```
