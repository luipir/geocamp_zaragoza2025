---
marp: true
title: Free geocoding in the cloud
subtitle: Setup OvertureMap based geocoding with WhereAbouts engine
date: 2025-09-17
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')

footer: |
    Luigi Pirelli - http://www.geobeyond.it


header: |
    <img src="./images/geo-logo-blue.svg" class="footer-img" alt="Footer Logo">


style: |
  h1, h2, h3, h4, h5 {
    text-align: center;
  }
  /* Center bullet lists vertically, left-align text 
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100%;
  }
  ul li, ol li {
    text-align: left;
  }*/
  .small-text {
    font-size: 0.75rem;
  }
  footer {
    /* Unset default placing inherited from the built-in theme */
    left: auto;
    right: auto;
    top: auto;
    bottom: auto;
    display: flex;
    align-items: center;
    gap: 10px;

    /* Place to right-bottom */
    right: 10px;
    bottom: 10px;
  }
  .footer-img {
    height: 62px;
    vertical-align: middle;
    margin-left: 8px;
  }
  header {
    position: absolute;
    top: 10;
    left: 10;
    width: 100vw;
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 10px 30px 10px 30px;
    background: transparent;
    z-index: 1000;
    box-sizing: border-box;
  }
  .header-img {
    height: 48px;
    vertical-align: middle;
  }
---
<!-- _paginate: hide -->
<style scoped>section{text-align:center;}</style>

# Free geocoding in the cloud
**GeoCamp Zaragoza 2025**

---
<style scoped>
  section{font-size:28px;}
  footer {display: none;}
</style>

## Who am I
![bg right:30% w:200](https://media.licdn.com/dms/image/v2/C4E03AQHVqbkFaZ_b2w/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1517757088359?e=1760572800&v=beta&t=-nBOnXiMmgbThzUrBrqVbZXxCvMl4fNABaW_Q1ClMQI)

- Luigi Pirelli
  - Since 2006 in QGIS/GRASS
  - QGIS Core developer and Plugin developer/trainer
  - Founder of GFOSS.it - Italian OSGEO Local Chapter
  - Founder of QGIS.es- Spanish QGIS user group
  - Now collaborating with
    - *GeoBeyond* www.geobeyond.it
    - *SaVE* - Electric Vehicle hacker ;)
  - https://www.linkedin.com/in/luigipirelli/

---

<style scoped>
  section{font-size:19px;}
  footer {display: none;}
</style>

## GeoBeyond since 2011

![bg right:60% w:700](./images/geobeyond_technologies_transparent.png)

- Services
  - Spatial Data Infrastructure
  - Access management configuration
- Client
  - [Rome Municipality](https://geoportale-preprod.comune.roma.it/georoma/#/)
  - [Politecnico di Milano](https://www.polimi.it/)
  - [ARPA Veneto](https://www.arpa.veneto.it/)
  - [Almaviva](https://www.almaviva.it/en_GB)
  - [NRCAN](https://natural-resources.canada.ca/) (<a class="small-text">Natural Resource Canada</a>)
  - and more...
- Enterprise support in:
  - GeoNode
  - pygeoapi (steering commettee)

---

## Goal

Official Italian portal DB update

- Geocode addresses <-------
- Fix addresses via field review
- Merge new or update addresses
- Update central DB

---

<style scoped>footer {display: none;}</style>

## Need geocoding

- QGIS plugin to geocode addresses
- integrate different geocoder via dynamic factories
- Free and Libre geocoder from OvertureMaps

---
<style scoped>
  section{font-size:21px;}
  footer {display: none;}
</style>

## OvertureMaps ?

- [OvertureMaps](https://overturemaps.org/) as source of  geocoding
- feed from different sources among them OSM
- No API at all

---

<style scoped>
  section{text-align:center;}
  footer {display: none;}
</style>

## No API then locally use WhereAbouts

- - [DuckDB](https://duckdb.org/) based.... DUCKDB????
- In process not only spatial DB
- DuckDB thedn could be natevely cloud
- BUT no cloud actually.... or not?

---

## no more local now cloud

- How to in https://github.com/ajl2718/whereabouts/issues/13
- Extract data from OvertureMap
- Populate WhereAbout DuckDB
- Put DB somewhere (my PR https://github.com/ajl2718/whereabouts/pull/16)
- Geocode!

---

## Questions?

---

<style scoped>
  section{
    font-size:30px;
    text-align: center;
  }
</style>

**Contacts**
  Luigi Pirelli
    luigi.pirelli@geobeyond.it
    https://www.linkedin.com/in/luigipirelli/
  Geobeyond
    info@geobeyond.it
    [www.geobeyond.it](http://www.geobeyond.it)
