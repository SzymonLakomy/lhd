lhd
===

LHD Van Centre (lhdvancentre.com). Symfony 7.4 LTS on PHP 8.3, MariaDB.

Setup: `composer install`, then put the real values in `.env.local`
(`APP_ENV=prod`, `APP_SECRET`, `DATABASE_URL`, `MAILER_TO`, `GOOGLE_MAPS_API_KEY`).

Deploy traps:
- Customer car photos are not in git. `public/bundles/app/img/stock` must be a symlink
  to the photo directory on the server.
- Do not run `bin/console assets:install`: it deletes unknown folders in `public/bundles/`,
  including `public/bundles/app` (site images and JS).
