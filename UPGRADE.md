## 4.x.x to 5.0.0

- HPKP `hashes` field only supports sha256 algorithm, change other algorithms to sha256.
- CSP `https-transform-on-https-connections` was removed, dont forget to use the explicit protocol.
- CSP `child-src` directive was removed, use `frame-src` or `worker-src` directive instead.
- CSP `img-src` directive `data` field was removed, use `schemes` field instead.
- CSP directive `hashes` field has new format, you can find it [here](https://github.com/BePsvPT/secure-headers/blob/50a803790f2f41767b9dc36459443725db4a1f64/config/secure-headers.php).

## 3.x.x to 4.0.0

- If you are a Lumen user, change `$app->register(Bepsvpt\SecureHeaders\LumenServiceProvider::class);` to `$app->register(Bepsvpt\SecureHeaders\SecureHeadersServiceProvider::class);` in `bootstrap/app.php`
- Because of dependency changing, please check your Content-Security-Policy(CSP) header is correct after upgrade. 

## 2.2.0 to 3.0.0

- Rename `config/security-header.php` to `config/secure-headers.php`
- Change provider from `Bepsvpt\LaravelSecurityHeader\SecurityHeaderServiceProvider::class,` to `Bepsvpt\SecureHeaders\SecureHeadersServiceProvider::class,` in `config/app.php`
- Change middleware from `\Bepsvpt\LaravelSecurityHeader\SecurityHeaderMiddleware::class,` to `\Bepsvpt\SecureHeaders\SecureHeadersMiddleware::class,` in `app/Http/Kernel.php`

## 2.1.x to 2.2.0

- The following new headers are added, you can find it [here](https://github.com/BePsvPT/laravel-security-header/blob/655c007418ac03bb56e152f5f5bfe6f7117a964b/config/security-header.php) and copy to your config file.
  - X-Download-Options
  - X-Permitted-Cross-Domain-Policies
  - Referrer-Policy

## 2.0.0 to 2.1.0

- You need to republish the config file and set up according to your need.
