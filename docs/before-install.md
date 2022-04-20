# Before and while installing ReviOS

## What is the difference between the versions? What to choose?

As of this moment (2022-04-19), there are only 2 versions of ReviOS that are supported: `10 22.04`, `11 21.04`. No other versions are supported.

=== "ReviOS 10 22.04"

    Based on the latest Windows 10.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.odb11cheqkzw){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.vxvav5mpn4w){target=_blank}

    Alternative download links on the [official Discord server's](https://discord.gg/962y4pU){target=_blank} [download channel](https://discord.com/channels/619835916139364383/658369065110339640/963477645859901491){target=_blank}.


=== "Revios 11 22.04"

    Based on the latest Windows 11.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.5m29vb11epyy){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.kwa7bvvnrtc9){target=_blank}

    Alternative download links on the [official Discord server's](https://discord.gg/962y4pU){target=_blank} [download channel](https://discord.com/channels/619835916139364383/658369065110339640/965855822372569099){target=_blank}.


**Faceit only works on 10 22.04 and 11 22.04 versions.** [Details below](#which-version-do-i-need-for-faceit).

---

## What is the system requirement for ReviOS?

Refer to our website's section about this, although it's the same as the stock Windows have, but ReviOS usually uses less RAM, and fewer processes run. The Windows 11 versions of ReviOS have the Secure Boot and TPM requirements disabled.

???+ note "TPM and Secure Boot on Windows 11"
    If you play games or use anti-cheats that require Secure Boot and TPM, you still need to enable those fuctions.

### ReviOS RAM usage

| Total RAM Capacity | Max Usage                       | Actual Available Amount |
| ------------------ | ------------------------------- | ------------------------- |
| 2 GB               | 1.1 GB down to 0.9, 1.4 GB peak | 600 MB to 1.1 GB          |
| 4 GB               | 0.8 GB                          | 3.2 GB                    |
| 8 GB               | 1 GB                            | 7 GB                      |
| 16 GB              | 1 GB                            | 15 GB                     |
| 24 GB              | 1.3 GB                          | 22.7 GB                   |

Tested on a fresh installation of ReviOS 10 22.01, in VirtualBox, on AMD Ryzen 5900X.

Credit to [Stasium#0001](https://stasium.dev/){target=_blank}.


---

## Which version do I need for Faceit?

As of this moment (2022-04-19), Faceit only works on the `10 22.04` and `11 22.04` versions.

If you are using one of these versions, and still cannot use Faceit, since the release of that version probably another update was released by Microsoft, which is required by Faceit. New build of ReviOS will be released soon. 

---

## Where are the older versions?

On the website, under [Archive Downloads](https://www.revi.cc/revios/download/archive-downloads){target=_blank}.

---

## How to install ReviOS?

The tutorial is [here](install.md).

---

## Can I install ReviOS on a MacBook?

Yes, you can. Follow [this guide](https://jensd.be/1011/windows/install-windows-10-on-a-macbook-air-2019-2020-with-t2-chip){target=_blank}, with the ReviOS iso of course.

---

## Downloads are not working / Google Drive: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded

Check our [official Discord server's](https://discord.gg/962y4pU){target=_blank} [download channel](https://discord.com/channels/619835916139364383/658369065110339640){target=_blank} and [website](https://www.revi.cc/revios/download){target=_blank} for alternative download links.

---

## Driver missing when installing ReviOS

Try plugging the flash drive into another USB port. If still not working, try using [Ventoy](https://www.ventoy.net/){target=_blank} instead of Rufus.
