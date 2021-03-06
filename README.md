> This project has two homes.
> It is ok to work in github, still, for a better decentralized web
> please consider contributing (issues, PR, etc...) throught:
>
> https://gitlab.esy.fun/yogsototh/ekg

---


# EKG: Remote monitoring of running processes over HTTP

This library lets you remotely monitor a running process over HTTP.
It provides a simple way to integrate a monitoring server into any
application.

# Getting started

Adding monitoring to your application is simple.  Just launch the
monitoring server as soon as your application starts

    import System.Remote.Monitoring
    
    main = do
         forkServer "localhost" 8000
         ...

and then visit [http://localhost:8000/](http://localhost:8000/) in
your web browser.

# JSON API

The monitoring server also lets you to retrieve the stats as JSON.
Simply send the server an HTTP GET request with the Accept header set
to "application/json":

    curl -H "Accept: application/json" http://localhost:8000/

You can use the JSON API to e.g. write applications that monitor other
applications.

# Get involved!

Please report bugs via the
[GitHub issue tracker](https://github.com/tibbe/ekg/issues).

Master [git repository](https://github.com/tibbe/ekg):

    git clone https://github.com/tibbe/ekg.git


# Authors

This library is written and maintained by Johan Tibell,
<johan.tibell@gmail.com>.
