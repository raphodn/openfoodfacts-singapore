# OpenFoodFacts x Singapore

OFF explorations, and looking at filling the gaps in Singapore.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Status](#status)
- [Get started](#get-started)
- [OpenFoodFacts](#openfoodfacts)
  - [Understand](#understand)
  - [License](#license)
  - [Ecosystem](#ecosystem)
  - [API](#api)
    - [View a product](#view-a-product)
    - [Write](#write)
- [Singapore Online Providers](#singapore-online-providers)
  - [Redmart](#redmart)
    - [Understand](#understand-1)
    - [Product details](#product-details)
    - [My List](#my-list)
    - [My Orders](#my-orders)
    - [Search](#search)
    - [API](#api-1)
    - [Ecosystem](#ecosystem-1)
  - [Cold Storage](#cold-storage)
  - [NTUC Fairprice](#ntuc-fairprice)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Status

- Joined OpenFoodFacts on April 04, 2019
- Project status: ongoing

## Get started

Current code is in Jupyter Notebooks

1. Clone the repository
2. Run `jupyter notebook`
3. Go to `http://localhost:8888/tree/`

Note: some files are not tracked in git, so some code may return errors

## OpenFoodFacts

### Understand

OpenFoodFacts is a collaborative, free and open database of food products from around the world. #Commons

- website: https://world.openfoodfacts.org/
- github: https://github.com/openfoodfacts

### License

Scraping is 'grey area'. So best to stay on the safe side. "Do not send copyrighted photos or information using the API. Everything you send is OdBL for the data, and CC-BY-SA for the pictures. If those are not yours (eg from scraping), you bear all the legal consequences."

### Ecosystem

Chrome extension: https://github.com/roiKosmic/DriveOff

### API

#### View a product

- docs: https://en.wiki.openfoodfacts.org/API/Read/Product
- endpoint: `https://world.openfoodfacts.org/api/v0/product/<code>`

#### Write

https://en.wiki.openfoodfacts.org/API/Write

## Singapore Online Providers

### Redmart

#### Understand

Redmart is one of Singapore's most used online supermarket. It is owned by Lazada.

- old website: https://redmart.com/
- new website (as of March 2019): https://redmart.lazada.sg/

#### Product details

The API returns many useful details on the product.

You can see an example product [here](redmart/redmart-products/redmart_product_instant_oatmeal_details.json)

Product fields:
- sku (string)
- title (string)
- category_tags (array)
- desc (string)
- description_fields {primary, secondary}
- filters {mfr_name, is_organic, country_of_origin, brand_name}
- img & images
- measure
- pricing
- product_life

#### My List

need to be logged in

#### My Orders

need to be logged in

#### Search

- endpoint: `https://api.redmart.com/v1.6.0/catalog/search`
- example: `https://api.redmart.com/v1.6.0/catalog/search?q=redmart&pageSize=18&sort=1024&category=redmart-label&page=1`

#### API

Work in progress

Goal: get Redmart products and store them in a CSV. Clean and check the data with a real product in hand (take pictures as well). Then upload to OFF.

#### Ecosystem

https://github.com/lologhi/redmart-per-kilo (Chrome extension)

### Cold Storage

- website: https://coldstorage.com.sg/
- offline supermarkets as well (scan parties possible)

### NTUC Fairprice

- website: https://www.fairprice.com.sg
- offline supermarkets as well (scan parties possible)
