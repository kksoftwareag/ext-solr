.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. raw:: latex

    \newpage

.. raw:: pdf

   PageBreak

.. _conf-tx-solr-settings:

Extbase Integration Configuration
=======================

To use the Observation of Changes in Extbase Models
add the following code to your ext_localconf.php

.. code-block:: php

    $domainObjectObserverRegistry = \TYPO3\CMS\Core\Utility\GeneralUtility::makeInstance(
        \ApacheSolrForTypo3\Solr\IndexQueue\DomainObjectObserverRegistry::class
    );

    $domainObjectObserverRegistry->register(
        \GeorgRinger\News\Domain\Model\News::class
    );