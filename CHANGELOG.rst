django-reversion changelog
==========================


1.9.1 - 04/08/2015
------------------

- Fixing packaging error that rendered the 1.9.0 release unusable. No way to cover up the mistake, so here's a brand new bugfix release! (@etianen).


1.9.0 - 04/08/2015
------------------

- Using database transactions do render consistent views of past revisions in database admin, fixing a lot of lingering minor issues (@etianen).
- Correct handling of readonly fields in admin (@etianen).
- Updates to Czech translation (@cuchac).
- Arabic translation (@RamezIssac).
- Fixing deleterevisions to work with Python2 (@jmurty).
- Fixing edge-cases where an object does not have a PK (@johnfraney).
- Tweaks, code cleanups and documentation fixes (@claudep, @johnfraney, @podloucky-init, Drew Hubl, @JanMalte, @jmurty, @etianen).



1.8.7 - 21/05/2015
------------------

- Fixing deleterevisions command on Python 3 (@davidfsmith).
- Fixing Django 1.6 compatibility (@etianen).
- Removing some Django 1.9 deprecation warnings (@BATCOH, @niknokseyer).
- Minor tweaks (@nikolas, @etianen).


1.8.6 - 13/04/2015
------------------

- Support for MySQL utf8mb4 (@alexhayes).
- Fixing some Django deprecation warnings (Drew Hubl, @khakulov, @adonm).
- Versions passed through by reversion.post_revision_commit now contain a primary key (@joelarson).


1.8.5 - 31/10/2014
------------------

- Added support for proxy models (@AgDude, @bourivouh).
- Allowing registration of models with django-reversion using custom signals (@ErwinJunge).
- Fixing some Django deprecation warnings (@skipp, @narrowfail).


1.8.4 - 07/09/2014
------------------

- Fixing including legacy south migrations in PyPi package (@GeyseR).


1.8.3 - 06/09/2014
------------------

- Provisional Django 1.7 support (@etianen).
- Multi-db and multi-manager support to management commands (@marekmalek).
- Added index on reversion.date_created (@rkojedzinszky).
- Minor bugfixes and documentation improvements (@coagulant).


1.8.2 - 01/08/2014
------------------

- reversion.register() can now be used as a class decorator (@aquavitae).
- Danish translation (@Vandborg).
- Improvements to Travis CI integration (@thedrow).
- Simplified Chinese translation (@QuantumGhost).
- Minor bugfixes and documentation improvements (@marekmalek, @dhoffman34, @mauricioabreu, @mark0978).


1.8.1 - 29/05/2014
------------------

- Slovak translation (@jbub).
- Deleting a user no longer deletes the associated revisions (@daaray).
- Improving handling of inline models in admin integration (@blueyed).
- Improving error messages for proxy model registration (@blueyed).
- Improvements to using migrations with custom user model (@aivins).
- Removing sys.exit() in deleterevisions management command, allowing it to be used internally by Django projects (@tongwang).
- Fixing some backwards-compatible admin deprecation warnings (Thomas Schreiber).
- Fixing tests if RevisionMiddleware is used as a decorator in the parent project (@jmoldow).
- Derived models, such as those generated by deferred querysets, now work.
- Removed deprecated low-level API methods.


1.8.0 - 01/11/2013
------------------

- Django 1.6 compatibility (@niwibe & @meshy).
- Removing type flag from Version model.
- Using bulk_create to speed up revision creation.
- Including docs in source distribution (@pquentin & @fladi).
- Spanish translation (@alexander-ae).
- Fixing edge-case bugs in revision middleware (@pricem & @oppianmatt).


1.7.1 - 26/06/2013
------------------

-  Bugfixes when using a custom User model.
-  Minor bugfixes.


1.7 - 27/02/2013
----------------

-  Django 1.5 compatibility.
-  Experimantal Python 3.3 compatibility!


1.6.6 - 12/02/2013
------------------

-  Removing version checking code. It's more trouble than it's worth.
-  Dutch translation improvements.


1.6.5 - 12/12/2012
------------------

-  Support for Django 1.4.3.


1.6.4 - 28/10/2012
------------------

-  Support for Django 1.4.2.


1.6.3 - 05/09/2012
------------------

-  Fixing issue with reverting models with unique constraints in the admin.
-  Enforcing permissions in admin views.


1.6.2 - 31/07/2012
------------------

-  Batch saving option in createinitialrevisions.
-  Suppressing warning for Django 1.4.1.


1.6.1 - 20/06/2012
------------------

-  Swedish translation.
-  Fixing formating for PyPi readme and license.
-  Minor features and bugfixes.


1.6 - 27/03/2012
----------------

-  Django 1.4 compatibility.


1.5.2 - 27/03/2012
------------------

-  Multi-db support.
-  Brazillian Portuguese translation.
-  New manage_manually revision mode.


1.5.1 - 20/10/2011
------------------

-  Polish translation.
-  Minor bug fixes.


1.5 - 04/09/2011
----------------

-  Added in simplified low level API methods, and deprecated old low level API methods.
-  Added in support for multiple revision managers running in the same project.
-  Added in significant speedups for models with integer primary keys.
-  Added in cleanup improvements to patch generation helpers.
-  Minor bug fixes.


1.4 - 27/04/2011
----------------

-  Added in a version flag for add / change / delete annotations.
-  Added experimental deleterevisions management command.
-  Added a --comment option to createinitialrevisions management command.
-  Django 1.3 compatibility.


1.3.3 - 05/03/2011
------------------

-  Improved resilience of revert() to database integrity errors.
-  Added in Czech translation.
-  Added ability to only save revisions if there is no change.
-  Fixed long-running bug with file fields in inline related admin models.
-  Easier debugging for createinitialrevisions command.
-  Improved compatibility with Oracle database backend.
-  Fixed error in MySQL tests.
-  Greatly improved performance of get_deleted() Version manager method.
-  Fixed an edge-case UnicodeError.


1.3.2 - 22/10/2010
------------------

-  Added Polish translation.
-  Added French translation.
-  Improved resilience of unit tests.
-  Improved scaleability of Version.object.get_deleted() method.
-  Improved scaleability of createinitialrevisions command.
-  Removed post_syncdb hook.
-  Added new createinitialrevisions management command.
-  Fixed DoesNotExistError with OneToOneFields and follow.


1.3.1 - 31/05/2010
------------------

This release is compatible with Django 1.2.1.

-  Django 1.2.1 admin compatibility.


1.2.1 - 03/03/2010
------------------

This release is compatible with Django 1.1.1.

-  The django syncdb command will now automatically populate any
   version-controlled models with an initial revision. This ensures existing
   projects that integrate Reversion won't get caught out.
-  Reversion now works with SQLite for tables over 999 rows.
-  Added Hebrew translation.


1.2 - 12/10/2009
----------------

This release is compatible with Django 1.1.

-  Django 1.1 admin compatibility.


1.1.2 - 23/07/2009
------------------

This release is compatible with Django 1.0.4.

-  Doc tests.
-  German translation update.
-  Better compatibility with the Django trunk.
-  The ability to specify a serialization format used by the  ReversionAdmin
   class when models are auto-registered.
-  Reduction in the number of database queries performed by the Reversion
-  admin interface.


1.1.1 - 25/03/2010
------------------

This release is compatible with Django 1.0.2.

-  German and Italian translations.
-  Helper functions for generating diffs.
-  Improved handling of one-to-many relationships in the admin.
