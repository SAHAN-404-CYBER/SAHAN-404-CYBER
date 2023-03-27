<p align="center">
 <img width="100px" src="https://images.app.goo.gl/ZKgRc3dXZh3MxsVL6
 <h2 align="center">GitHub Readme Stats</h2>
 <p align="center">Get dynamically generated GitHub stats on your READMEs!</p>
</p>
  <p align="center">


Copy-paste this into your markdown content, and that is it. Simple!

Change the `?username=` value to your GitHub username.

```md
[![SAHAN GitHub stats](https://github-readme-stats.vercel.app/api?username=sahan)](https://github.com/SAHAN-404-CYBER/SAHAN-404-CYBER/blob/main/README.md)
```

> **Note**
> Available ranks are S+ (top 1%), S (top 25%), A++ (top 45%), A+ (top 60%), and B+ (everyone). The values are calculated by using the [cumulative distribution function](https://en.wikipedia.org/wiki/Cumulative_distribution_function) using commits, contributions, issues, stars, pull requests, followers, and owned repositories. The implementation can be investigated at [src/calculateRank.js](./src/calculateRank.js).

### Hiding individual stats

You can pass a query parameter `&hide=` to hide any specific stats with comma-separated values.

> Options: `&hide=stars,commits,prs,issues,contribs`

```md
![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&hide=contribs,prs)
```


### Adding private contributions count to total commits count

You can add the count of all your private contributions to the total commits count by using the query parameter `&count_private=true`.

> **Note**
> If you are deploying this project yourself, the private contributions will be counted by default. If you are using the public Vercel instance, you need to choose to [share your private contributions](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-settings-on-your-profile/showing-your-private-contributions-and-achievements-on-your-profile).

> Options: `&count_private=true`

```md
![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&count_private=true)
```

### Showing icons

To enable icons, you can pass `&show_icons=true` in the query param, like so:

```md
![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true)
```

### Themes

With inbuilt themes, you can customize the look of the card without doing any [manual customization](#customization).

Use `&theme=THEME_NAME` parameter like so :

```md
![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=radical)
```

#### All inbuilt themes

GitHub readme stats comes with several built-in themes (e.g. `dark`, `radical`, `merko`, `gruvbox`, `tokyonight`, `onedark`, `cobalt`, `synthwave`, `highcontrast`, `dracula`).

<img src="https://res.cloudinary.com/SAHAN-404-CYBER/image/upload/v1595174536/grs-themes_l4ynja.png" alt="GitHub Readme Stats Themes" width="600px"/>

You can look at a preview for [all available themes](./themes/README.md) or checkout the [theme config file](./themes/index.js) & **you can also contribute new themes** if you like :D

#### Responsive Card Theme

[![SAHAN-404-CYBER GitHub stats-Dark](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=dark#gh-dark-mode-only)](https://github.com/SAHAN-404-CYBER/github-readme-stats#gh-dark-mode-only)
[![SAHAN-404-CYBER GitHub stats-Light](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=default#gh-light-mode-only)](https://github.com/SAHAN-404-CYBER/github-readme-stats#gh-light-mode-only)

Since GitHub will re-upload the cards and serve them from their [CDN](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-anonymized-urls), we can not infer the browser/GitHub theme on the server side. There are, however, four methods you can use to create dynamics themes on the client side.

##### Use the transparent theme

We have included a `transparent` theme that has a transparent background. This theme is optimized to look good on GitHub's dark and light default themes. You can enable this theme using the `&theme=transparent` parameter like so:

```md
![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=transparent)
```

<details>
<summary>:eyes: Show example</summary>

![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=transparent)

</details>

##### Add transparent alpha channel to a themes bg_color

You can use the `bg_color` parameter to make any of [the available themes](./themes/README.md) transparent. This is done by setting the `bg_color` to a colour with a transparent alpha channel (i.e. `bg_color=00000000`):

```md
![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&bg_color=00000000)
```

<details>
<summary>:eyes: Show example</summary>

![SAHAN-404-CYBER GitHub stats](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&bg_color=00000000)

</details>

##### Use GitHub's theme context tag

You can use [GitHub's theme context](https://github.blog/changelog/2021-11-24-specify-theme-context-for-images-in-markdown/) tags to switch the theme based on the user GitHub theme automatically. This is done by appending `#gh-dark-mode-only` or `#gh-light-mode-only` to the end of an image URL. This tag will define whether the image specified in the markdown is only shown to viewers using a light or a dark GitHub theme:

```md
[![SAHAN-404-CYBER GitHub stats-Dark](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=dark#gh-dark-mode-only)](https://github.com/SAHAN-404-CYBER/github-readme-stats#gh-dark-mode-only)
[![SAHAN-404-CYBER GitHub stats-Light](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=default#gh-light-mode-only)](https://github.com/SAHAN-404-CYBER/github-readme-stats#gh-light-mode-only)
```

<details>
<summary>:eyes: Show example</summary>

[![SAHAN-404-CYBER GitHub stats-Dark](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=dark#gh-dark-mode-only)](https://github.com/SAHAN-404-CYBER/github-readme-stats#gh-dark-mode-only)
[![SAHAN-404-CYBER GitHub stats-Light](https://github-readme-stats.vercel.app/api?username=SAHAN-404-CYBER&show_icons=true&theme=default#gh-light-mode-only)](https://github.com/SAHAN-404-CYBER/github-readme-stats#gh-light-mode-only)


### Demo

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SAHAN-404-CYBER)](https://github.com/SAHAN-404-CYBER/github-readme-stats)

-   Compact layout

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SAHAN-404-CYBER&layout=compact)](https://github.com/SAHAN-404-CYBER/github-readme-stats)

- Hidden progress bars

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SAHAN-404-CYBER&hide_progress=true)](https://github.com/SAHAN-404-CYBER/github-readme-stats)

# Wakatime Week Stats

Change the `?username=` value to your [Wakatime](https://wakatime.com) username.

```md
[![willianrod's wakatime stats](https://github-readme-stats.vercel.app/api/wakatime?username=willianrod)](https://github.com/SAHAN-404-CYBER/github-readme-stats)
```

> **Note**:
> Please be aware that we currently only show data from Wakatime profiles that are public.

-   [GitHub Stats Card](#github-stats-card)
-   [GitHub Extra Pins](#github-extra-pins)
-   [Top Languages Card](#top-languages-card)
-   [Wakatime Week Stats](#wakatime-week-stats)
-   [Themes](#themes)
    -   [Responsive Card Theme](#responsive-card-theme)
-   [Customization](#customization)
    -   [Common Options](#common-options)
    -   [Stats Card Exclusive Options](#stats-card-exclusive-options)
    -   [Repo Card Exclusive Options](#repo-card-exclusive-options)
    -   [Language Card Exclusive Options](#language-card-exclusive-options)
    -   [Wakatime Card Exclusive Option](#wakatime-card-exclusive-options)
-   [Deploy Yourself](#deploy-on-your-own)
    -   [On Vercel](#on-vercel)
    -   [On other platforms](#on-other-platforms)
    -   [Keep your fork up to date](#keep-your-fork-up-to-date)

# GitHub Stats Card
