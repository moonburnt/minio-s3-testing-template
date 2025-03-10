# Minio S3 Testing Template

## Description

This is a docker-compose template for local s3 testing with minio. The problem
I was trying to solve is the requirement to test backend s3 integration without
having a pre-configured s3 instance available. This snippet does exactly that -
provides a temporary S3-compatible storage to be used locally.

## Usage

- Copy `compose.yml`'s content into your own compose, or clone this repo.
- Copy `.env.template`'s content to your local `.env`, or create a new one and
configure things as you please. If you are extending the existing dotenv and
don't want to overload it with variables - the bare minimum would be `MINIO_ADMIN`
and `MINIO_PASSWORD`.
-  Run `docker-compose up`.

With default values, this will do the following:
- Create an S3 instance on port `9000`, with bucket named `bucket` accessible to
read and write by everyone.
- Create a web interface on port `9001`, accessible with login `admin` and password `adminadmin`.

## Contribution

I've made this template for personal use and only sharing it because it was kinda
popular within my local chat network. It fits my own needs and I'm happy with it.
However, if you see any possible ways to improve this - please, open an issue or
create a PR!

## Credits

https://rogs.me/2021/01/using-minio-to-upload-to-a-local-s3-bucket-in-django/

https://stackoverflow.com/a/78580294

## License

Public domain, obviously - most of this template is sourced from the web, as
specified above - use it as you please!
