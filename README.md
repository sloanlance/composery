# Composery
A Composer wrapper to read its configuration from a YAML file, composer.yml.

---
> > > ## ⚠️&nbsp;&nbsp;Note:  
> > > &nbsp;&nbsp;&nbsp;&nbsp;_This package is still in the very early stages of development._  
> > > &nbsp;&nbsp;&nbsp;&nbsp;_Don't be disappointed by its lack of substance._  
---

## Why‽
* Comments can't be added to composer.json because JSON doesn't allow comments.
* YAML allows comments.
* Bidirectional conversion between YAML and JSON is easy and reliable.  (Except for the loss of YAML comments.)
* If loss of fidelity between between YAML and JSON is a concern, fret not.  YAML can contain JSON and _still_ allow comments.
* The [igorw/composer-yaml](https://github.com/igorw/composer-yaml) project good, but it only converts composer.yml to composer.json.  It doesn't run Composer using the new composer.json file, though.
* In contrast, Composery will:
  * Convert composer.yml to composer.json.
  * Run composer using the new composer.json.
  * By default, delete composer.json before exiting.
  * Optionally keep composer.json when exiting, which is useful for debugging or distribution.
