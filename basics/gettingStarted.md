# Configuring Your Environment

To get started with reverse engineering (RE) websites, you’ll often need to bypass detection mechanisms that websites use to spot scrapers or automated browsers. One way to tackle this is by using an undetected browser.

In this guide, we’ll configure **[Librewolf](https://librewolf.net/)**—a privacy-focused browser that’s already equipped with useful patches—and make a few tweaks to make it fully undetectable for scraping tasks.

----------

## Step 1: Installing Librewolf

Head over to [librewolf.net](https://librewolf.net/) and download the version compatible with your operating system. Follow the installation instructions to set it up.

----------

## Step 2: Modifying `about:config`

Once Librewolf is installed, open the browser and type `about:config` into the address bar. You’ll see a page with advanced configuration settings.

Change the following settings to enhance stealth:

-   **`librewolf.console.logging_disabled`** → `true`  
    _(Disables console logging to prevent detection.)_
-   **`librewolf.debugger.force_detach`** → `true`  
    _(Ensures debugging tools are detached, avoiding detection.)_
-   **`webgl.disabled`** → `false`  
    _(Enables WebGL for rendering compatibility.)_
-   **`privacy.resistFingerprinting`** → `false`  
    _(Disables anti-fingerprinting measures that can raise suspicion.)_
-   **`devtools.toolbox.host`** → `window`  
    _(Changes devtools host to avoid triggering detection flags.)_
-   **`devtools.source-map.client-service.enabled`** → `false`  
    _(Disables source map service to prevent devtools-based checks.)_

----------

## Step 3: Congratulations!

You now have a browser configured to bypass many common detection methods. This setup allows you to navigate websites without arbitrary restrictions.

Want to test your new browser? Visit this [DevTools Detector Demo](https://blog.aepkill.com/demos/devtools-detector/) to confirm it’s working undetected.

Happy scraping! 🚀