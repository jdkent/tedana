Usage
=====

tedana minimally requires:

#. acquired echo times (in milliseconds), and
#. functional datasets equal to the number of acquired echoes.

But you can supply many other options, viewable with ``tedana -h`` or
``t2smap -h``.

Run tedana
----------
This is the full tedana workflow, which runs multi-echo ICA and outputs
multi-echo denoised data along with many other derivatives.
To see which files are generated by this workflow, check out the workflow
documentation: :py:func:`tedana.workflows.tedana_workflow`.

.. argparse::
   :ref: tedana.workflows.tedana._get_parser
   :prog: tedana
   :func: _get_parser

Run t2smap
----------
This workflow uses multi-echo data to optimally combine data across echoes and\
to estimate T2* and S0 maps or time series.
To see which files are generated by this workflow, check out the workflow
documentation: :py:func:`tedana.workflows.t2smap_workflow`.

.. argparse::
   :ref: tedana.workflows.t2smap._get_parser
   :prog: t2smap
   :func: _get_parser
