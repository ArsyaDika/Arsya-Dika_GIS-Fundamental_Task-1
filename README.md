# Healthcare Accessibility in Semarang City (QGIS)

Which parts of Semarang are still too far from a hospital or a community health center (puskesmas)? This QGIS buffer analysis maps the gaps in healthcare reach across the city and **proposes where new facilities would help most**.

Task 1 of the WebGIS Developer bootcamp (GIS Fundamental).

![Final map](docs/peta-final.jpg)

## Questions

1. How are hospitals and community health centers (puskesmas) distributed across districts?
2. Which areas are not reached, judging by service distance?
3. Where would a new health facility make sense?

## Method (QGIS)

1. Align the CRS of all data to EPSG:3857.
2. Clip the Central Java hospital and puskesmas points to the Semarang City boundary.
3. Buffer the service distances: hospitals 3,000 m, puskesmas 1,500 m, then merge.
4. Join attributes by location to count facilities per district.
5. Difference: the city boundary minus the service areas, which leaves the underserved area.
6. Digitize proposed new facility points inside the underserved area, close to the road network.

## Data

| Data | Source |
|---|---|
| City and district boundaries | Bootcamp geodatabase |
| Central Java hospitals 2025, puskesmas | Central Java Province Geoportal |
| Road network | OpenStreetMap (Overpass Turbo) |

## Repository contents

| File | Contents |
|---|---|
| `Peta Jumlah Fasilitas Kesehatan ... _final bgt.qgz` | Final QGIS project |
| `Merged Faskes_kota smg.json` | Health facility points after clip and merge |
| `Jumlah Faskes Per Kecamatan.json` | Facility count per district |
| `Area yg tidak terlayani RS dan Puskesmas.json` | Difference result (underserved area) |
| `Titik Lokasi.json` | Proposed new facility points |
| `Peta Final.pdf` | Map layout |
| `Laporan Analisa Singkat_Task 1_GIS Fundamental.pdf` | Short analysis report (Indonesian) |

## Tools

QGIS · OpenStreetMap · GeoJSON

## Author

**Arsya Dika** · [GitHub](https://github.com/ArsyaDika)

------------------

# Keterjangkauan Fasilitas Kesehatan Kota Semarang (QGIS)

Analisis buffer untuk menemukan wilayah Kota Semarang yang belum terjangkau rumah sakit dan puskesmas, lalu mengusulkan lokasi fasilitas kesehatan baru.

Tugas 1 bootcamp WebGIS Developer (GIS Fundamental).

![Peta final](docs/peta-final.jpg)

## Pertanyaan

1. Bagaimana sebaran rumah sakit dan puskesmas per kecamatan?
2. Wilayah mana yang belum terjangkau berdasarkan jarak layanan?
3. Di mana lokasi yang layak untuk fasilitas kesehatan baru?

## Metode (QGIS)

1. Samakan CRS semua data ke EPSG:3857.
2. Clip titik rumah sakit dan puskesmas Jawa Tengah ke batas Kota Semarang.
3. Buffer jarak layanan: rumah sakit 3.000 m, puskesmas 1.500 m, lalu merge.
4. Join attributes by location untuk menghitung jumlah fasilitas per kecamatan.
5. Difference: batas kota dikurangi area layanan, sehingga tersisa area tidak terlayani.
6. Digitasi titik usulan fasilitas baru di area tidak terlayani, dekat jaringan jalan.

## Data

| Data | Sumber |
|---|---|
| Batas kota dan kecamatan | Geodatabase bootcamp |
| Rumah sakit Jawa Tengah 2025, puskesmas | Geoportal Provinsi Jawa Tengah |
| Jaringan jalan | OpenStreetMap (Overpass Turbo) |

## Isi repo

| File | Isi |
|---|---|
| `Peta Jumlah Fasilitas Kesehatan ... _final bgt.qgz` | Proyek QGIS final |
| `Merged Faskes_kota smg.json` | Titik faskes hasil clip dan merge |
| `Jumlah Faskes Per Kecamatan.json` | Jumlah faskes per kecamatan |
| `Area yg tidak terlayani RS dan Puskesmas.json` | Hasil difference |
| `Titik Lokasi.json` | Titik usulan fasilitas baru |
| `Peta Final.pdf` | Layout peta |
| `Laporan Analisa Singkat_Task 1_GIS Fundamental.pdf` | Laporan singkat |

## Tools

QGIS · OpenStreetMap · GeoJSON

## Penulis

**Arsya Dika** · [GitHub](https://github.com/ArsyaDika)
