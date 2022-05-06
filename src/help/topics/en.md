# Help (English)

This document will guide you through the features of Dark Reader.

- [FAQ](#faq)
- [Contacts](#contacts)
- [Top section](#top-section)
- [Filter settings](#filter-settings)
- [Custom site settings](#custom-site-settings)
- [Site list](#site-list)
- [More tab](#more-tab)
- [Theme generation modes](#theme-generation-modes)
- [Bottom section](#bottom-section)
- [Using the Developer tools](#using-dev-tools)


<h2 id="top-section">Top section</h2>

<img src="https://user-images.githubusercontent.com/49388020/166393538-919777f5-be25-49d8-9ef2-f7df8a1c8333.png" />


- **On/Off** switch enables or disables the extension.
- **Auto** switches setting depending on system darkmode. 
- **Toggle site** button (where url is listed) adds the current site into the ignore list (or removes it from there).
- Note: If the toggle button is greyed-out, it means that browser restricts injecting scripts into current page.


<h2 id="filter-settings">Theme settings</h2>

<img src="https://user-images.githubusercontent.com/49388020/167062722-fcd7d9b1-84ce-44db-8c57-9aa777ca2271.png" />

Adjust the scheme, mode, brightness, contrast, sepia, and saturation ("grayscale") settings. This can be used to better suit your screen parameters and the lighting in the room.

Click "See all options" for the full list of settings: 

<img src="https://user-images.githubusercontent.com/49388020/167062964-aef45377-a3dd-416f-a563-9fc94bb2c0cc.png" />



<h2 id="custom-site-settings">Custom site settings</h2>

<img src="https://user-images.githubusercontent.com/49388020/167063520-a8b43982-7165-4ff0-9e47-d0472ce1ce48.png" />

The dropdown options when you click **Theme for all websites** determine whether the above theme settings should be applied to all websites, the current website, or if you like a new theme profile you can use for a subset of websites. 

<h2 id="theme-generation-modes">Theme generation modes</h2>

<img src="https://user-images.githubusercontent.com/49388020/167065896-cec00bf3-a754-494e-8d91-1081b08626b1.png" />

</br>

<figure>
    <img src="https://user-images.githubusercontent.com/49388020/167066233-31c0ff39-6e03-4942-ba22-1d76f32238bb.png">
    <figcaption>Filter+ vs. Static vs. Dynamic mode</figcaption>
</figure>

- **Filter** is the initial Dark Reader mode based on CSS filters.
It *inverts the whole page* and *reverts some parts* back.
Requires GPU resources.
It is *fast* and powerful, but has several issues:
it disables text sub-pixel rendering,
inverts already dark parts into light,
causes lags on large pages,
and fails to render some pages in Firefox.
- **Filter+** is the same as Filter, but is based on custom SVG filters
and *handles colors better* making images less dull.
Works poorly in Firefox.
- **Static** rapidly generates a basic stylesheet.
- **Dynamic** deeply analyzes website stylesheets, background images, and vector graphics.
Requires some resources on initial page load,
but produces *the best* visual results.
The work on this mode is in progress,
but it already works well for many modern websites.

<h2 id="settings-list">Settings list</h2>

<img src="https://user-images.githubusercontent.com/49388020/167064092-eb612c6d-efee-4209-a4ad-d12e7fc09a9f.png" />
</br>
<img src="https://user-images.githubusercontent.com/49388020/167064362-cb318645-8811-4dd0-81ba-62fd278da4b0.png" />

Clicking on settings will take you to the settings menu. Here you can toggle Dark Reader, access the site list, access dev tools and more. 



<h2 id="site-list">Site list</h2>

<img src="https://user-images.githubusercontent.com/49388020/167065046-8946607b-4d6f-43d4-931d-e0576023e374.png" />
</br>
<img src="https://user-images.githubusercontent.com/49388020/167065322-d6160ff6-6230-4a78-9121-34af907ec24e.png" />


- Add sites to the Site list to exclude them from Dark Reader site manipulations. 
- Possible patterns for values are `google.com, mail.google.com, google.*, google.com/maps` etc.
- Clicking the **Toggle site** button (in [Top section](#top-section)) adds the current site into this list.
- You can also toggle whether to use Dark Reader on PDFs and restricted sites.



<h2 id="bottom-section">Bottom section</h2>

<img src="https://user-images.githubusercontent.com/49388020/167066568-7efd098b-f8e5-4af3-9b8b-1dfc7c46372b.png" />

- Access **Settings** and read the **Help** documentation on this page.
- **Donate** – if you like the extension, please consider supporting the active development of Dark Reader.
Crowdfunding is powered by Open Collective, which currently uses Stripe for handling payments.
- **Blog** – Click the preview link on the bottom to read release notes and important events.



<h2 id="using-dev-tools">Using the Developer tools</h2>

If you are familiar with CSS selectors, you can help by suggesting a fix for filtering a website.
Read how to use the developer tools [here](https://github.com/darkreader/darkreader#how-to-contribute).


<h2 id="faq">FAQ</h2>

#### The extension asks for permissions to read website data

The extension needs these permissions to be able to analyze and modify website appearence,
determine if a website is disabled by your settings or to use site-specific rules.
We do not insert ads and do not collect any data or send it anywhere.
The extension is fully open-source and has no obfuscated code.
Our monetization is transparent and is based on users' donations.

#### The extensions store page and settings pages remain white

The extension has no access to these pages.

#### New tab page and browser theme remain white

The extension cannot change the appearence of a new tab or browser (though in Firefox it can since version 60).
We recommend installing a dark theme or new tab extension from extensions store.

#### Screen flashes white when opening a new tab or navigating to a website

Before loading a website, Chrome shows the theme background color by default.
We recommend installing a dark theme from the store.

#### The extension doesn't work at all

If you have similar dark mode extensions installed, disable them, then reload tabs.
Click Dark Reader icon, check if top-right button is set to **On** and that **Toggle site** is not excluding the current site.
Open **Site list** tab, check that **Not invert listed** is selected.
If nothing helps, something terrible has happened, e-mail us.

#### The website is displayed incorrectly or works slowly

Please send the website address, a screenshot, your OS and browser versions to our e-mail.
We will try to investigate the reason, at least for a popular website.
Also try changing **theme generation mode** or try using **Light mode**.
Check that the website is not listed under **Site list** tab.

#### The extension doesn't work in incognito mode

Open **chrome://extensions** page, find **Dark Reader**, click **Allow in incognito**.

#### The extension doesn't work for local files

Open **chrome://extensions** page, find **Dark Reader**, click **Allow access to file URLs**.

#### Entire website is not displayed in Filter mode

If you are using Chrome for Mac OS, update Mac OS up to 10.13, this should update your video drivers.
If you are using Firefox, this is most likely a browser bug, use another mode for such websites.


<h2 id="contacts">Contacts</h2>

For any questions e-mail to [darkreaderapp@gmail.com](mailto:darkreaderapp@gmail.com)
