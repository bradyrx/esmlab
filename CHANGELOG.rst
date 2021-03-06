==================
Changelog history
==================

Esmlab v2019.3. (2019-03)
==============================

Features
--------

- Enable computing significance metrics (p-value) for ``weighted_corr`` (:pr:`90`) `Riley Brady`_


Esmlab v2019.3.16 (2019-03-16)
==============================

Features
--------

- Add statistics functions for DataArray and Dataset to ``statistics.py`` module (:pr:`97`) `Anderson Banihirwe`_

Functions added:
  - ``weighted_mean``
  - ``weighted_sum``
  - ``weighted_std``
  - ``weighted_covariance``
  - ``weighted_correlation``

Bug Fixes
---------

- Increase rtol for float32 weights in ``statistics.py`` module (:pr:`81`) `Michael Levy`_
- Remove duplicate call to ``statistics._get_weights_and_dims`` (:pr:`88`) `Sudharsana K J L`_
- Fix bugs in ``utils.time.time_manager`` add tests for climatology corner cases (:pr:`100`) `Matthew Long`_

  - Allow ``climatology.compute_ann_mean`` to work if time is encoded
  - Make sure ``time:calendar`` is preserved in ``climatolog.compute_ann_mean``


Esmlab v2019.2.28 (2019-02-28)
==============================

Features
---------

- Add function to flexibily compute weights and dimensions to use in statistical operations (:pr:`74`) `Anderson Banihirwe`_

- Add ``time_manager`` class to support managing the time coordinate of datasets (:pr:`75`) and (:pr:`76`) `Matthew Long`_


Bug Fixes
----------

- Remove hard-coded ``tb_name=time_bound`` in ``compute_time_var`` (:pr:`72`) `Anderson Banihirwe`_

Documentation
---------------

- Add release procedure to documentation (:pr:`78`) `Anderson Banihirwe`_


Trivial/Internal Changes
-------------------------

- Use `esmlab-data <https://github.com/NCAR/esmlab-data>`_ in tests (:pr:`67`) `Anderson Banihirwe`_
- Update continuous integration workflow (:pr:`68`) `Anderson Banihirwe`_



Esmlab v2019.2.1 (2019-02-12)
==============================

- Add ``time_bound`` to output of ``compute_ann_mean`` (:pr:`51`) `Matthew Long`_
- Add xarray alignment option to prevent using mismatching coordinates (:pr:`54`) `Anderson Banihirwe`_
- Add regridding functionality (:pr:`56`) `Matthew Long`_
- Handle ``time_bound`` on data read with ``decode_times=True`` (:pr:`59`) `Matthew Long`_
- Add interface to esmlab-data (:pr:`61`) `Anderson Banihirwe`_


Esmlab v2019.2.0 (2019-02-02)
==============================

- Rename ``compute_ann_climatology`` to ``compute_ann_mean`` (:pr:`33`) `Anderson Banihirwe`_
- Don't add ``NaNs`` for ``_FillValue`` (:pr:`34`) `Anderson Banihirwe`_
- Change time handling for ``compute_mon_climatology`` and ``compute_ann_mean`` (:pr:`37`) `Matthew Long`_
- Add slice_mon_clim_time argument to ``compute_mon_climatology`` (:pr:`37`) `Matthew Long`_
- Drop ``time_bound`` variable from ``compute_ann_mean`` (:pr:`43`) `Matthew Long`_




.. _`Anderson Banihirwe`: https://github.com/andersy005
.. _`Matthew Long`: https://github.com/matt-long
.. _`Michael Levy`: https://github.com/mnlevy1981
.. _`Riley Brady`: https://github.com/bradyrx
.. _`Sudharsana K J L`: https://github.com/sudharsana-kjl
