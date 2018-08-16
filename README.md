# prep-product-image

Prepare or preprocess product images for Amazon or Google Shopping; that is remove logo and non-white / gray background

## Getting Started

### Prerequisites

1. PHP
2. ImageMagick (convert command/tool)

### Usage

```
php prep-product-image.php -i <source image> -o <destination image>
```

#### Switches

* `-v` or `--version` or `-h` for version and usage instruction
* `--verbose` or `--debug` for verbose output

## Examples

TODO

## How it works

This is a PHP wrapper script that executes convert command in each steps for:

1. Replacing non-white background with white background
2. Generating mask image to identify different objects in the image
3. From the mask image, identify logo portion
4. Fill that logo portion with white (or, erase with white color)
5. Perform smart crop with ImageMagick's `-trim`

## Todos/Roadmap

* [ ] Check in ImageMagick forum with experts
* [ ] Add gray shadow removal
