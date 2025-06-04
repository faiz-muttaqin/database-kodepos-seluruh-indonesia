Indonesian Postal Code Database 
===================

Tools
-------------------
* DB - MySql

Query
--------------------
``` sql
SELECT
	kelurahan,
	kecamatan,
	kabupaten,
	provinsi
FROM
	tbl_kodepos
WHERE
	kodepos = ?
```

History
--------------------
**Aug 2015 -** List of postalcodes are provided from PT Pos Indonesia (http://www.posindonesia.co.id/), with 81.248 kodepos data. File name = `tbl_kodepos.sql`

**Dec 2021 -** Grabbing kodepos data from BPS website (https://sig.bps.go.id/bridging-kode/index), resulting in 69.498 kodepos data. File name = `tbl_kodepos_bps.sql`


Q&A
--------------------
**Q :** Why number of `kodepos` data from PT Pos and BPS is different?

**A :** 
1. PT Pos Indonesia (official postal service):

Maintains official postal routing data.

Focuses on mail delivery efficiency, not necessarily administrative boundaries.

One kodepos might cover several kelurahan or one kelurahan might have multiple kodepos if needed for routing purposes (e.g., different delivery areas or clusters).

2. BPS (Central Bureau of Statistics):

Uses kodepos primarily for statistical and demographic purposes.

Tries to assign one kodepos per kelurahan/desa in line with administrative boundaries.

May rely on surveys, local government data, and not always align with PT Pos's data.

##

**Q :** Which data is the correct one?

**A :** 
PT Pos Indonesia is the official authority for postal codes.

For purposes like:

Mail delivery → Use PT Pos data.

Official address formatting → Use PT Pos.

Administrative statistics or GIS mapping → BPS data may be preferred (with caution).

##


**Q :** Why some `kelurahan` can have more than one `kodepos` in BPS data?

**A :** 
Several reasons:

1. Inconsistent local data collection: BPS might have received conflicting data from multiple sources.

2. Large kelurahan area: If a kelurahan spans a wide or diverse geography, it may include multiple postal zones.

3. Administrative changes: New kelurahan boundaries or split areas may lead to overlapping or transitional kodepos.

4. Legacy data: Some entries might include outdated or previous kodepos due to slow updates in administrative records.



Disclaimer
--------------------
```
This data is provided "as is" without any guarantee whatsoever. 
Feel free to fork, tinker, add, remove, change, or do whatever you want to it. 
```
