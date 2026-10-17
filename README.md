<a href="https://www.amiradio.rs/"><img src="media/cover.jpg" alt="Radio AMI, home page on a laptop and a phone" width="100%"></a>

# Radio AMI

News portal for a radio station from Kikinda: 15,029 articles moved from WordPress, a live player that keeps playing between pages and a local info service.

**[amiradio.rs](https://www.amiradio.rs/)** · [Case study (in Serbian)](https://svilenkovic.rs/radovi/radio-ami) · [Srpski](README.sr.md)

> [!NOTE]
> Client project. The source code belongs to the client and stays in a private repository. This page describes what I built and how.

<table>
  <tr><td><b>Client</b></td><td>Reks DOO Kikinda, Radio AMI 89.7</td></tr>
  <tr><td><b>Industry</b></td><td>Local radio station and news portal</td></tr>
  <tr><td><b>Location</b></td><td>Kikinda, Serbia</td></tr>
  <tr><td><b>Type</b></td><td>News portal with an editorial panel (PWA)</td></tr>
  <tr><td><b>My role</b></td><td>Redesign, development, migration, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>PHP 8.3, MariaDB, Redis, Icecast, nginx, PWA</td></tr>
</table>

## About the project

Radio AMI broadcasts from Kikinda on 89.7 MHz and publishes news from the town and the villages around it. The old site ran on WordPress and held more than fifteen thousand articles. The station needed a faster portal that kept every one of them, kept the old links working and put what local readers look for every day (power and water cuts, job ads, the doctors' schedule) right next to the news.

I wrote the portal in plain PHP 8.3 with MariaDB and a Redis cache, without WordPress or plugins, and moved 15,029 articles with their images, sections and dates. In all, 1,348 old addresses redirect permanently to the new ones, so a link shared on social networks years ago still opens the same story. The live player sits in the header and does not stop when a reader opens another page; the stream goes through an Icecast relay on my server.

## What I built

- 15,029 articles and 1,348 old addresses moved from WordPress, with permanent redirects
- A live player in the header that keeps playing between pages, an Icecast relay and M3U and PLS playlists
- Info service pages for power, water, heating and jobs, plus the theatre programme and a monthly doctors' schedule you can open by day
- A separate editorial panel installed as its own PWA, with banner ads and view and click counts for each banner
- A public PWA added from the /aplikacija/ page, a newsletter with double opt-in and pages for shows and video
- Mobile PageSpeed 96, with accessibility, best practices and SEO at 100, measured on 17 October 2026

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 96 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, lab test of the live site, October 2026. Security headers: 6 of 6. HTML validator: no errors. axe accessibility check: no violations. Structured data: `BroadcastService`, `NewsMediaOrganization`, `RadioStation`.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Radio AMI, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Radio AMI, home page on a phone"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Info service with the latest notice, an ad and the weather in Kikinda">
<sub>Info service with the latest notice, an ad and the weather in Kikinda</sub>

<img src="media/inner-2.webp" alt="Doctors' schedule: pick a day, or see the whole month in one table">
<sub>Doctors' schedule: pick a day, or see the whole month in one table</sub>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
