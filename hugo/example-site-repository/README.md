# cloud-hugo/hugo/example-site-repository

An example of how to setup a repo leveraging the `cloud-hugo` design.

## Creating the Hugo base.

After creating a new repo:

``` shell
cd repo-dir-name
hugo new site -f yaml .
mkdir src
mkdir hugo
mv archetypes hugo/
mv content src/
mv data src/
mv layouts hugo/
mv static src/
mv themes hugo/
```

Remove `baseURL:` from `config.yaml`, and add the following:

``` yaml
publishDir: out
archetypeDir: hugo/archetypes
assetDir: hugo/assets
layoutDir: hugo/layouts
themesDir: hugo/themes
resourceDir: hugo/resources
contentDir: src/content
dataDir: src/data
staticDir: src/static
```
