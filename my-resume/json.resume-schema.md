---
description: This page was created while building my Json.Resume
layout: landing
---

# JSON.RESUME SCHEMA

<details>

<summary>Themes</summary>

[https://jsonresume.org/themes/](https://jsonresume.org/themes/)

[https://registry.jsonresume.org/themes](https://registry.jsonresume.org/themes)

[https://www.npmjs.com/search?ranking=maintenance\&q=jsonresume-theme](https://www.npmjs.com/search?ranking=maintenance\&q=jsonresume-theme)

### Want to develop your own?

Check out an example boilerplate theme -> [https://github.com/jsonresume/jsonresume-theme-boilerplate](https://github.com/jsonresume/jsonresume-theme-boilerplate).\
\
Here is an example of a more well done and modern theme -> [https://github.com/davcd/jsonresume-theme-actual](https://github.com/davcd/jsonresume-theme-actual).\
\
For an even better theme development environment, try this -> [https://github.com/kelyvin/jsonresume-theme-caffeine](https://github.com/kelyvin/jsonresume-theme-caffeine).\
\
In short, if you want to add a theme to the official list, you need to publish an NPM module named \`jsonresume-theme-{name}\`. That module needs to export a function called \`render\` that takes a \`resume.json\` and returns a plain HTML string.

#### Getting started

If you are using the registry to host your resume, you can easily test different themes by appending a query string e.g.

[https://registry.jsonresume.org/thomasdavis?theme=flat](https://registry.jsonresume.org/thomasdavis?theme=flat)

Or you can set the default theme for your resume on the registry by using the `--theme` option in the CLI tool e.g.

`resume publish --theme flat`

`###########Optional for local Development############################`

<pre class="language-shell" data-overflow="wrap" data-line-numbers><code class="lang-shell"><strong>// Install JSONResume CLI
</strong>sudo npm install -g resume-cli
sudo npm install
resume serve --theme 
Preview: http://localhost:4000
Press ctrl-c to stop</code></pre>

</details>

{% embed url="https://registry.jsonresume.org/esz3tt?theme=onepageresume" %}

{% tabs %}
{% tab title="Useful Links" %}
{% embed url="https://github.com/jsonresume/resume-schema" %}
{% endtab %}

{% tab title="Dirty little helpers" %}
{% embed url="https://resume.entwicklerprogramm.workers.dev/" %}
json Fetch from Cloudflare
{% endembed %}

{% hint style="info" %}
e.g. use Cloudflare for managing api fetch | put | get | option
{% endhint %}

{% embed url="https://dash.cloudflare.com/" %}
Use Workers on free Dev-Account !
{% endembed %}
{% endtab %}
{% endtabs %}
