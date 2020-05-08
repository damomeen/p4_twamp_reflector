p4_twamp_reflector
=============

p4_twamp_reflector is the TWAMP reflector implementation (see RFC 5357 Two-Way Active Measurement Protocol) in the P4 language for bmv2 software switch. It also contains the TWAMP control server implemented in Python. 
p4_twamp_reflector uses [p4app](https://github.com/p4lang/p4app) containing mininet with bmv2 switches for build, run and test. 

More information about the design of p4_twamp_reflector can be found in an presentation in /docs/ folder.

Installation
------------

1. Install [docker](https://docs.docker.com/engine/installation/) if you don't
   already have it.

2. If you want, put the `p4app` script somewhere in your path. For example:

    ```
    cp p4app /usr/local/bin
    ```

Usage
-----

To start a P4 switch with the TWAMP reflector and the TWAMP control server just run:

```
./start.sh
```

To run the TWAMP client (you can choose twampy or twping client implementation) run within mininet prompt:

```
h1 sh /tmp/twampy.sh
```
or

```
h1 sh /tmp/twping.sh
```

Testbed and implementation details
----------------------------------
Our emulation environment is composed by one P4 switch emulated with Mininet. The switch connects to a single host.

The debug mode for the switch can be enabled by using:

``` 
    ./debug_switch1.sh
```    

The  terminal for the host is available by using:

``` 
    ./xterm_h1.sh
```    
