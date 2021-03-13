# Module 03 - Search & Browse

[< Previous Module](../modules/module02.md) - **[Home](../README.md)** - [Next Module>](../modules/module04.md)

## Prerequisites

* An Azure account with an active subscription.
* An Azure Azure Purview account (see [module 01](../modules/module01.md)).
* An Azure Purview catalog with some assets (see [module 02](../modules/module02.md)).

## Introduction

Once sources have been registered and scanned, the underlying data catalog will begin to populate with assets that represent real-world objects (e.g. a table in an Azure SQL Database, a Power BI report, etc.) The surfacing of these assets via Azure Purview's search experience helps empower data consumers to find data assets that matters to them.

## Table of Contents

1. [Search Catalog](#1-search-catalog)
2. [Update an Asset](#2-update-an-asset)
3. [Browse Assets](#3-browse-assets)

<div align="right"><a href="#module-03---search--browse">↥ back to top</a></div>

## 1. Search Catalog

1. Open Purview Studio and from the **Home** screen, type the asterik character (**\***) into the search bar and hit **Enter**.

    ![Search Wildcard](../images/03-search-wildcard.png)

2. Filter the search results by **Classification** (e.g. Country/Region) and click the hyperlinked asset name to view the details (e.g. QueriesByState).

    ![Filter by Classification](../images/03-search-filter.png)

<div align="right"><a href="#module-03---search--browse">↥ back to top</a></div>

## 2. Update an Asset

1. Click **Edit** to modify the asset details.

    ![Edit Asset](../images/03-asset-edit.png)

2. Update the **Description** by copying and pasting the sample text below.

    > This dataset was curated from the Bing search logs (desktop users only) over the period of Jan 1st, 2020 – (Current Month - 1). Only searches that were issued many times by multiple users were included. The dataset includes queries from all over the world that had an intent related to the Coronavirus or Covid-19. In some cases this intent is explicit in the query itself (e.g., “Coronavirus updates Seattle”), in other cases it is implicit , e.g. “Shelter in place”.

    ![Update Description](../images/03-asset-description.png)

3. Assign a **Classification** (e.g. World Cities) using the drop-down menu.

    ![Update Classification](../images/03-asset-classification.png)

4. Navigate to the **Schema** tab and update the **column descriptions** using the sample text below.

    | Column Name  | Description |
    | --- | --- |
    | Date | `Date on which the query was issued.` |
    | Query | `The actual search query issued by user(s).` |
    | IsImplicitIntent | `True if query did not mention covid or coronavirus or sarsncov2 (e.g, “Shelter in place”). False otherwise.` |
    | State | `State from where the query was issued.` |
    | Country | `Country from where the query was issued.` |
    | PopularityScore | `Value between 1 and 100 inclusive. 1 indicates least popular query on the day/State/Country with Coronavirus intent, and 100 indicates the most popular query for the same geography on the same day.` |

    ![Update Schema](../images/03-asset-schema.png)

5. Navigate to the **Contacts** tab and set someone within your organization to be an **Expert** and an **Owner**. Click **Save**.

    ![Update Contacts](../images/03-asset-contacts.png)

6. To see other assets within the same path, navigate to the **Related** tab.

    ![Related Assets](../images/03-asset-related.png)

<div align="right"><a href="#module-03---search--browse">↥ back to top</a></div>

## 3. Browse Assets

While the search experience is ideal for keyword based discovery, Purview Studio allows users to also navigate the catalog by source.

1. Open Purview Studio and from the **Home** screen, click **Browse assets**.

    ![Browse Assets](../images/03-home-browse.png)

2. Select a **source** (e.g. Azure Data Lake Storage Gen2).

    ![ADLS Gen2](../images/03-browse-adls.png)

3. Select an **account** (e.g. storage2486).

    ![ADLS Gen2 Account](../images/03-browse-account.png)

4. Select a **container** (e.g. raw).

    ![ADLS Gen2 Container](../images/03-browse-container.png)

<div align="right"><a href="#module-03---search--browse">↥ back to top</a></div>

## Summary

This module provided an overview of how to search, browse, and update an asset.