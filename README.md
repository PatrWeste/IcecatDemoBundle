Akeneo PIM Icecat Demo Bundle
=============================

This bundle contains real world data coming from the Icecat databases.

To install the demo data, use the following commands :

WARNING: the contents of your database will be replaced

    git submodule add git@github.com:akeneo/IcecatDemoBundle.git src/Pim/Bundle/IcecatDemoBundle
    # Update your AppKernel to add PimIcecatDemoBundle
    sh install.sh db
    php app/console doctrine:fixtures:load --append --fixtures=src/Pim/Bundle/IcecatDemoBundle/DataFixtures/
    php app/console cache:clear --env=prod
    php app/console pim:icecat-demo:install --env=prod
    php app/console pim:product:completeness-calculator --env=prod
    php app/console pim:versioning:refresh --env=prod


For more information about Icecat, please see http://icecat.biz