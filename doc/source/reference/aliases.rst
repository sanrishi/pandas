{{ header }}

.. _api.typing.aliases:

======================================
pandas typing aliases
======================================

**************
Typing aliases
**************

.. currentmodule:: pandas.api.typing

The typing declarations in ``pandas/_typing.py`` are considered private, and used
by pandas developers for type checking of the pandas code base.  For users, it is
highly recommended to use the ``pandas-stubs`` package that represents the officially
supported type declarations for users of pandas.
They are documented here for users who wish to use these declarations in their
own python code that calls pandas or expects certain results.

.. warning::

    Note that the definitions and use cases of these aliases are subject to change without notice in any major, minor, or patch release of pandas.

Each of these aliases listed in the table below can be found by importing them from :py:mod:`pandas.api.typing.aliases`.

==================================== ================================================================
Alias                                Meaning
==================================== ================================================================
``AggFuncType``                        Type of functions that can be passed to :meth:`agg` methods
``AlignJoin``                          Argument type for ``join`` in :meth:`DataFrame.join`
``AnyAll``                             Argument type for ``how`` in :meth:`dropna`
``AnyArrayLike``                       Used to represent :class:`ExtensionArray`, ``numpy`` arrays, :class:`Index` and :class:`Series`
``ArrayLike``                          Used to represent :class:`ExtensionArray`, ``numpy`` arrays
``AstypeArg``                          Argument type in :meth:`astype`
``Axes``                               :py:type:`AnyArrayLike` plus sequences (not strings) and ``range``
``Axis``                               Argument type for ``axis`` in many methods
``CSVEngine``                          Argument type for ``engine`` in :meth:`DataFrame.read_csv`
``ColspaceArgType``                    Argument type for ``colspace`` in :meth:`DataFrame.to_html`
``CompressionOptions``                 Argument type for ``compression`` in all I/O output methods except :meth:`DataFrame.to_parquet`
``CorrelationMethod``                  Argument type for ``correlation`` in :meth:`corr`
``DropKeep``                           Argument type for ``keep`` in :meth:`drop_duplicates`
``Dtype``                              Types as objects that can be used to specify dtypes
``DtypeArg``                           Argument type for ``dtype`` in various methods
``DtypeBackend``                       Argument type for ``dtype_backend`` in various methods
``DtypeObj``                           Numpy dtypes and Extension dtypes
``ExcelWriterIfSheetExists``           Argument type for ``if_sheet_exists`` in :class:`ExcelWriter`
``ExcelWriterMergeCells``              Argument type for ``merge_cells`` in :meth:`to_excel`
``FilePath``                           Type of paths for files for I/O methods
``FillnaOptions``                      Argument type for ``method`` in various methods where NA values are filled
``FloatFormatType``                    Argument type for ``float_format`` in :meth:`to_string`
``FormattersType``                     Argument type for ``formatters`` in :meth:`to_string`
``FromDictOrient``                     Argument type for ``orient`` in :meth:`DataFrame.from_dict`
``HTMLFlavors``                        Argument type for ``flavor`` in :meth:`pandas.read_html`
``IgnoreRaise``                        Argument type for ``errors`` in multiple methods
``IndexLabel``                         Argument type for ``level`` in multiple methods
``InterpolateOptions``                 Argument type for ``interpolate`` in :meth:`interpolate`
``JSONEngine``                         Argument type for ``engine`` in :meth:`read_json`
``JSONSerializable``                   Argument type for the return type of a callable for argument ``default_handler`` in :meth:`to_json`
``JoinHow``                            Argument type for ``how`` in :meth:`pandas.merge_ordered` and for ``join`` in :meth:`Series.align`
``JoinValidate``                       Argument type for ``validate`` in :meth:`DataFrame.join`
``MergeHow``                           Argument type for ``how`` in :meth:`merge`
``MergeValidate``                      Argument type for ``validate`` in :meth:`merge`
``NaPosition``                         Argument type for ``na_position`` in :meth:`sort_index` and :meth:`sort_values`
``NsmallestNlargestKeep``              Argument type for ``keep`` in :meth:`nlargest` and :meth:`nsmallest`
``OpenFileErrors``                     Argument type for ``errors`` in :meth:`to_hdf` and :meth:`to_csv`
``Ordered``                            Return type for :py:attr:`ordered` in :class:`CategoricalDtype` and :class:`Categorical`
``ParquetCompressionOptions``          Argument type for ``compression`` in :meth:`DataFrame.to_parquet`
``QuantileInterpolation``              Argument type for ``interpolation`` in :meth:`quantile`
``ReadBuffer``                         Additional argument type corresponding to buffers for various file reading methods
``ReadCsvBuffer``                      Additional argument type corresponding to buffers for :meth:`pandas.read_csv`
``ReadPickleBuffer``                   Additional argument type corresponding to buffers for :meth:`pandas.read_pickle`
``ReindexMethod``                      Argument type for ``reindex`` in :meth:`reindex`
``Scalar``                             Types that can be stored in :class:`Series` with non-object dtype
``SequenceNotStr``                     Used for arguments that require sequences, but not plain strings
``SliceType``                          Argument types for ``start`` and ``end`` in :meth:`Index.slice_locs`
``SortKind``                           Argument type for ``kind`` in :meth:`sort_index` and :meth:`sort_values`
``StorageOptions``                     Argument type for ``storage_options`` in various file output methods
``Suffixes``                           Argument type for ``suffixes`` in :meth:`merge`, :meth:`compare` and :meth:`merge_ordered`
``TakeIndexer``                        Argument type for ``indexer`` and ``indices`` in :meth:`take`
``TimeAmbiguous``                      Argument type for ``ambiguous`` in time operations
``TimeGrouperOrigin``                  Argument type for ``origin`` in :meth:`resample` and :class:`TimeGrouper`
``TimeNonexistent``                    Argument type for ``nonexistent`` in time operations
``TimeUnit``                           Time unit argument and return type for :py:attr:`unit`, arguments ``unit`` and ``date_unit``
``TimedeltaConvertibleTypes``          Argument type for ``offset`` in :meth:`resample`, ``halflife`` in :meth:`ewm` and ``start`` and ``end`` in :meth:`pandas.timedelta_range`
``TimestampConvertibleTypes``          Argument type for ``origin`` in :meth:`resample` and :meth:`pandas.to_datetime`
``ToStataByteorder``                   Argument type for ``byteorder`` in :meth:`DataFrame.to_stata`
``ToTimestampHow``                     Argument type for ``how`` in :meth:`to_timestamp` and ``convention`` in :meth:`resample`
``UpdateJoin``                         Argument type for ``join`` in :meth:`DataFrame.update`
``UsecolsArgType``                     Argument type for ``usecols`` in :meth:`pandas.read_clipboard`, :meth:`pandas.read_csv` and :meth:`pandas.read_excel`
``WindowingRankType``                  Argument type for ``method`` in :meth:`rank` in rolling and expanding window operations
``WriteBuffer``                        Additional argument type corresponding to buffers for various file output methods
``WriteExcelBuffer``                   Additional argument type corresponding to buffers for :meth:`to_excel`
``XMLParsers``                         Argument type for ``parser`` in :meth:`DataFrame.to_xml` and :meth:`pandas.read_xml`
==================================== ================================================================
