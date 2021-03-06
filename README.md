# Rust web framework comparison

A comparison of some web frameworks written in [Rust](https://rustlang.org).

## Server frameworks

At the moment there are seven interesting framworks to build web applications
with Rust:

- **iron**     ([homepage](http://ironframework.io/) / [repository](https://github.com/iron/iron/)            / [documentation](http://ironframework.io/doc/iron/))
- **nickel**   ([homepage](http://nickel.rs/)        / [repository](https://github.com/nickel-org/nickel.rs/) / [documentation](http://docs.nickel.rs/nickel/))
- **rustful**  ( -                                   / [repository](https://github.com/Ogeon/rustful)         / [documentation](http://ogeon.github.io/docs/rustful/master/rustful/))
- **rustless** ([homepage](http://rustless.org/)     / [repository](https://github.com/rustless/rustless)     / [documentation](http://rustless.org/rustless/doc/rustless/))
- **conduit**  ( -                                   / [repository](https://github.com/conduit-rust/conduit)  / - )
- **rouille**  ( -                                   / [repository](https://github.com/tomaka/rouille)        / [documentation](http://tomaka.github.io/rouille/rouille/index.html))
- **pencil**   ( -                                   / [repository](https://github.com/fengsp/pencil)         / [documentation](http://fengsp.github.io/pencil/))

If you need a more low level control you can choose between three libraries:

- **hyper**     ([homepage](http://hyper.rs/) / [repository](https://github.com/hyperium/hyper)      / [documentation](http://hyper.rs/hyper/hyper/))
- **tiny-http** ( -                           / [repository](https://github.com/frewsxcv/tiny-http)) / [documentation](http://frewsxcv.github.io/tiny-http/tiny_http/index.html))
- **solicit**   ( -                           / [repository](https://github.com/mlalic/solicit)      / [documentation](https://mlalic.github.io/solicit/solicit/index.html))
- **kinglet**   ( -                           / [repository](https://github.com/pyfisch/kinglet)     / - )

## Client frameworks

To build web clients with Rust, you can chosse between three libraries:

- **hyper**   ([homepage](http://hyper.rs/) / [repository](https://github.com/hyperium/hyper)          / [documentation](http://hyper.rs/hyper/hyper/))
- **ease**    (-                            / [repository](https://github.com/SimonPersson/ease)       / [documentation](http://simonpersson.github.io/ease/))
- **jsonrpc** (-                            / [repository](https://github.com/apoelstra/rust-jsonrpc/) / [documentation](https://www.wpsoftware.net/rustdoc/jsonrpc/))

## Supplemental libraries

- **websocket** ([homepage](http://cyderize.github.io/rust-websocket/) / [repository](https://github.com/cyderize/rust-websocket) / [documentation](http://cyderize.github.io/rust-websocket/doc/websocket/))
- **ws-rs**     (-                                                     / [repository](https://github.com/housleyjk/ws-rs)         / [documentation](http://housleyjk.github.io/ws-rs/ws))

## Blog posts


- [Introducing Pencil: A Microframework Inspired By Flask For Rust](https://fengsp.github.io/blog/2016/3/introducing-pencil/)
- [Trying Rust for web services](https://blog.wearewizards.io/trying-rust-for-web-services)
- [Are we web yet?](http://arewewebyet.com/)
- [Reimplementing ashurbanipal.web in Rust](http://maniagnosis.crsr.net/2015/07/reimplementing-ashurbanipalweb-in-rust.html)
- [A web app with Nickel: From first line to Heroku deployment](http://blog.thoughtram.io/rust/2015/07/29/a-web-app-with-nickel-from-first-line-to-heroku-deployment.html)
- [What features Iron does not have compared to a web server like nginx?](https://www.reddit.com/r/rust/comments/3t1mze/what_features_iron_does_not_have_compared_to_a/)
- [Build an API in Rust with JWT Authentication using Nickel.rs](https://auth0.com/blog/2015/11/30/build-an-api-in-rust-with-jwt-authentication-using-nickelrs/)
- [Selective Middleware for Iron](http://gregchapple.com/selective-middleware-for-iron/)
- [Rust for the Web - RESTful API in Rust, impressions](https://medium.com/@eugeniyoz/restful-api-in-rust-impressions-63250d611d15)

## Demos

- [rustwebapp](https://github.com/superlogical/rustwebapp) - Iron and Postgres
- [webrust](https://github.com/Keats/webrust) - Iron and Postgres
- [httptest](https://github.com/brson/httptest) - Iron
- [nickel-todo-backend](https://github.com/Ryman/nickel-todo-backend/) - Nickel and Postgres

## Comparison

### General

|                      Name | iron   | nickel  | rustful   | rustless  | conduit | rouille   | hyper  | tiny-http  | solicit | ease  | jsonrpc | websocket |  ws-rs     | kinglet   |  pencil       |
| ------------------------- | ------ | ------- | --------- | --------- | ------- | --------- | ------ | ---------- | ------- | ----- | ------- | --------- |  --------- | --------- |  ------------ |
|               **License** | MIT    | MIT     | MIT       | MIT       | MIT     | ?         | MIT    | Apache 2.0 | MIT     | MIT   | CC0-1.0 | MIT       |  MIT       | MIT       |  BSD-3-Clause |
|          **Github Stars** | 2.5k   | 1.3k    | 0.7k      | 0.2k      | 0.1k    | 0k        | 1.4k   | 0.2k       | 0.1k    | 0.1k  | 0k      | 0.2k      |  0.1k      | 0.1k      |  0.1k         |
|          **Contributors** | 51     | 39      | 9         | 8         | 4       | 1         | 88     | 7          | 2       | 2     | 2       | 16        |  2         | 1         |  1            |
|                **Server** | yes    | yes     | yes       | yes       | yes     | yes       | yes    | yes        | yes     | no    | no      | yes       |  yes       | yes       |  yes          |
|                **Client** | ?      | ?       | ?         | ?         | no      | no        | yes    | ?          | yes     | yes   | yes     | yes       |  yes       | no        |  no           |
|        **Base framework** | hyper  | hyper   | hyper     | iron      | civet   | tiny-http | yes    | yes        | -       | hyper | hyper   | no        |  no        | yes       |  hyper        |
|         **HTTPS support** | yes    | no      | yes       | ?         | ?       | ?         | yes    | yes        | -       | -     | -       | -         |  -         | -         |  ?            |
|        **HTTP/2 support** | ?      | ?       | ?         | ?         | ?       | ?         | ?      | ?          | yes     | ?     | ?       | -         |  -         | -         |  ?            |

### Middleware & Plugins

|                      Name | iron                                        | nickel                                                | conduit | rouille | rustful   | rustless  | pencil    |
| ------------------------- | ------------------------------------------- | ----------------------------------------------------- | ------- | ------- | --------- | --------- | --------- |
|   **Static File Serving** | [yes](https://github.com/iron/static)       | yes                                                   | yes     | no      | ?         | ?         | yes       |
|              **Mounting** | [yes](https://github.com/iron/mount)        | yes                                                   | ?       | no      | ?         | ?         | ?         |
|               **Logging** | [yes](https://github.com/iron/logger)       | no                                                    | ?       | no      | ?         | ?         | yes       |
|     **JSON-Body-Parsing** | [yes](https://github.com/iron/body-parser)  | yes                                                   | ?       | no      | ?         | ?         | ?         |
|              **Sessions** | [yes](https://github.com/iron/session)      | ?                                                     | ?       | no      | ?         | ?         | ?         |
|               **Cookies** | [yes](https://github.com/iron/cookie)       | ?                                                     | ?       | no      | ?         | ?         | ?         |
| **PostgreSQL middleware** | ?                                           | [yes](https://github.com/nickel-org/nickel-postgres)  | ?       | no      | ?         | ?         | ?         |
|     **SQLite middleware** | ?                                           | [yes](https://github.com/flosse/nickel-sqlite)        | ?       | no      | ?         | ?         | ?         |
|      **Redis middleware** | ?                                           | [yes](https://github.com/matthewbentley/nickel-redis) | ?       | no      | ?         | ?         | ?         |
|      **MySQL middleware** | ?                                           | [yes](https://github.com/zither/nickel-mysql)         | ?       | no      | ?         | ?         | ?         |

## Examples

To compile or run the examples use [Cargo](https://github.com/rust-lang/cargo).
First clone this repo

    git clone https://github.com/flosse/rust-web-framework-comparison
    cd rust-web-framework-comparison/

and change to the desired frameworkd directory (e.g. `cd iron/`) and type

    cargo run --example hello_world

Then visit `http://localhost:3000` to see the result.
