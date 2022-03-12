# Before and while installing ReviOS

## What is the difference between the versions? What to choose?

As of this moment (2022-02-18), there are 3 versions of ReviOS that are supported: `22.02`, `21.01` and `1709`. No other versions are supported.

Usually every other released version is based on the same Windows version, with newer updates and tweaks. Like in odd numbered months, Windows 10, in even numbered months Windows 11.

### Revios 11 22.02

Based on the latest Windows 11.

[Changelog](https://www.revi.cc/revios/download/changelog#h.odb11cheqkzw)

[Download](https://www.revi.cc/revios/download#h.kwa7bvvnrtc9)

Alternative download links not available right now, this page will be updated as soon as links are out.

### ReviOS 10 22.01

Based on the latest Windows 10.

[Changlelog](https://www.revi.cc/revios/download/changelog#h.t081ow81wszv)

[Download](https://www.revi.cc/revios/download#h.vxvav5mpn4w)

[Alternative download links](https://www.revi.cc/revios/download#h.ry3n13gw38ew)

### ReviOS 1709

Based on an older release of Windows 10, not many software supports it anymore.

[Changelog](https://www.revi.cc/revios/download/changelog#h.rfvq0n3k2uk7)

[Download](https://www.revi.cc/revios/download/archive-downloads#h.ski2fzvfamkj)

Alternative download links on the [official Discord server's](https://discord.gg/962y4pU) [download channel](https://discord.com/channels/619835916139364383/658369065110339640/859328905336979476).


If you are looking for a version:

- more gaming, less latency and less bloatware oriented, choose `1709`
- more compatible with latest programs, choose `22.02` or `22.01`

**Faceit only works on 22.02 and 22.01 versions.** [Details below](#which-version-do-i-need-for-faceit).

---

## What is the system requirement for ReviOS?

It is the same as the stock Windows versions have, although ReviOS uses less RAM.


| Total RAM Capacity | Max Usage                       | Actually Available Amount |
| ------------------ | ------------------------------- | ------------------------- |
| 2 GB               | 1.1 GB down to 0.9, 1.4 GB peak | 600 MB to 1.1 GB          |
| 4 GB               | 0.8 GB                          | 3.2 GB                    |
| 8 GB               | 1 GB                            | 7 GB                      |
| 16 GB              | 1 GB                            | 15 GB                     |
| 24 GB              | 1.3 GB                          | 22.7 GB                   |

Tested on a fresh installation of [ReviOS 10 22.01](#revios-10-2201), in VirtualBox, on AMD Ryzen 5900X.

Credit to Stasium#0001


---

## Which version do I need for Faceit?

As of this moment (2022-02-18), Faceit only works on the `22.02` and `22.01` versions.

If you are using one of these versions, and still cannot use Faceit, since the release of that version probably another update was released by Microsoft, which is required by Faceit. New build of ReviOS will be released soon.

---

## Where are the older versions?

[On the website, under Archive Downloads](https://www.revi.cc/revios/download/archive-downloads).

---

## How to install ReviOS?

[The tutorial is here](https://youtu.be/w4Wn25d02iY).

---

## Can I install ReviOS on a MacBook?

Yes, you can. Follow [this guide](https://jensd.be/1011/windows/install-windows-10-on-a-macbook-air-2019-2020-with-t2-chip), with the ReviOS iso of course.

---

## Downloads are not working / Google Drive: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded

For the latest version the alternative downloads are on the [website](https://www.revi.cc/revios/download), and direct links for the specific versions [above](#what-is-the-difference-between-the-versions-what-to-choose).

For other, older version, there are mirror download links on the [official Discord server's](https://discord.gg/962y4pU) [download channel](https://discord.com/channels/619835916139364383/658369065110339640).

---

## Driver missing when installing ReviOS

Try plugging the flash drive into another USB port. If sill not working, try using [Ventoy](https://www.ventoy.net/) instead of Rufus.
