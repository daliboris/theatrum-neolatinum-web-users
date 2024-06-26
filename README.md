# Theatrum Neolatinum Annotation Users

This application has only one purpose: define an eXist-db user that will be used as an advanced user in Theatrum Neolatinum Annotation application.

## Modifications

Other files in the template you may need to change:

* local.secrets.xsl - change `permissions/@user` and `permissions/@password` attributes
  * change the username in the **theatrum-neolatinum-annotation** repository

When changing this module remember to reindex the data collection for the changes to be reflected by the indexes.

* build.xml - build file, used to create a xar package with ant

## Installing

Use Package Manager in eXist-db or `xst` command `xst package install ./build/tnlanno-users.xar --config admin.xstrc`.

You can check installed packages with `xst` command `xst package list --libraries --versions --config admin.xstrc`.

To see all defined users use `xst execute "sm:list-users()" --config admin.xstrc`.

## Unistalling

To uninstall the package use the following command: `xst package uninstall --config admin.xstrc tnlanno-users`.

Users are not removed from the database when the package is uninstalled.

You can install and uninstall the package to create users for other applications keeping their passwords secret.
