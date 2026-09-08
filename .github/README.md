<div id="top"></div>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![HACS Custom][hacs-shield]][hacs-url]

<div align="center">
  <h3 align="center">Vane</h3>
  <p align="center">
    A clean, minimal Home Assistant theme with matching light and dark modes.
    <br />
    <a href="https://github.com/JelleBuning/vane/issues">Report Bug</a>
    ·
    <a href="https://github.com/JelleBuning/vane/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#features">Features</a></li>
        <li><a href="#screenshots">Screenshots</a></li>
      </ul>
    </li>
    <li>
      <a href="#installation">Installation</a>
      <ul>
        <li><a href="#hacs-recommended">HACS (recommended)</a></li>
        <li><a href="#manual">Manual</a></li>
      </ul>
    </li>
    <li><a href="#customizing">Customizing</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

## About The Project

Vane is a Home Assistant frontend theme focused on a clean, minimal look with
first-class light and dark mode support.

### Features

* **Matching light & dark palettes** — one theme, two fully designed modes
* **Domain accent colors** — distinct, consistent colors for lights, covers,
  climate, and media players
* **Broad coverage** — styles core Home Assistant UI, Material (MDC)
  components, and popular custom cards like
  [Bubble Card](https://github.com/Clooos/Bubble-Card)
* **Zero configuration** — install it and pick it, no options to tune

### Screenshots

> TODO: add dashboard screenshots/GIFs here (light mode + dark mode). This is
> the single most important thing for people to actually try the theme —
> prioritize adding real screenshots before anything else.

## Installation

### HACS (recommended)

1. In Home Assistant, go to **HACS**.
2. Click the three-dot menu (top right) → **Custom repositories**.
3. Add `https://github.com/JelleBuning/vane` as category **Theme**.
4. Find **Vane** in HACS and install it.
5. Go to **Settings → System → General** and select **Vane** as your theme
   (or set it per-user in your profile).

### Manual

1. Copy `themes/vane.yaml` into your Home Assistant `config/themes/` directory.
2. Make sure `themes:` is enabled under `frontend:` in `configuration.yaml`:
   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```
3. Restart Home Assistant (or reload themes) and select **Vane** as your theme.

## Customizing

All colors live in a small set of `vn-*` variables per mode (`dark`/`light`)
at the top of `themes/vane.yaml`. Change a color there and it propagates
everywhere it's used — see [`CLAUDE.md`](CLAUDE.md) for how the file is
structured.

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place
to learn, inspire, and create. Any contributions you make are **greatly
appreciated**.

If you have a suggestion that would make this better, please fork the repo
and create a pull request. You can also simply open an issue with the tag
"enhancement". Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b features/feature-title`)
3. Commit your Changes (`git commit -m 'Added feature'`)
4. Push to the Branch (`git push origin features/feature-title`)
5. Open a Pull Request

<!-- LICENSE -->
## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/JelleBuning/vane.svg?style=for-the-badge
[contributors-url]: https://github.com/JelleBuning/vane/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/JelleBuning/vane.svg?style=for-the-badge
[forks-url]: https://github.com/JelleBuning/vane/network/members
[stars-shield]: https://img.shields.io/github/stars/JelleBuning/vane.svg?style=for-the-badge
[stars-url]: https://github.com/JelleBuning/vane/stargazers
[issues-shield]: https://img.shields.io/github/issues/JelleBuning/vane.svg?style=for-the-badge
[issues-url]: https://github.com/JelleBuning/vane/issues
[license-shield]: https://img.shields.io/github/license/JelleBuning/vane.svg?style=for-the-badge
[license-url]: https://github.com/JelleBuning/vane/blob/main/LICENSE
[hacs-shield]: https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=for-the-badge
[hacs-url]: https://github.com/hacs/integration
