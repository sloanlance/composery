# Composery
A wrapper for Composer to read its configuration from a YAML file, composer.yml.

## Why‽
* Comments can't be added to composer.json because JSON doesn't allow comments.
* YAML allows comments.
* Bidirectional conversion between YAML and JSON is easy and reliable.  (Except for the loss of YAML comments.)
* If loss of fidelity between between YAML and JSON is a concern, fret not.  YAML can contain JSON and _still_ allow comments.
* The [igorw/composer-yaml](https://github.com/igorw/composer-yaml) project good, but it only converts composer.yml to composer.json.  It doesn't run composer using the new composer.json file, though.
* In contrast, Composery will:
  * Convert composer.yml to composer.json.
  * Run composer using the new composer.json.
  * By default, delete composer.json before exiting.
  * Optionally keep composer.json when exiting, which is useful for debugging or distribution.
