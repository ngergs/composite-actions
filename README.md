# Github actions collection

My personal collection of composite GitHub Actions for personal use.

The composite actions are aimed at simplicity and do not offer full customizable compared to their individual components.

## Content
todo

## Caching
Go modules are cached using the GitHub Action [actions/cache@v3](https://github.com/actions/cache) and the key 
```
${{ runner.os }}-go-${{ hashFiles('**/go.sum') }}
```