# userstyles

User styles for Mikroways' internal tools. They are applied with
[Stylus](https://add0n.com/stylus.html), which is available for Firefox and
Chrome.

| Style | For |
|---|---|
| `redmine-dark.user.css` | Dark mode for [proyectos.mikroways.net](https://proyectos.mikroways.net) |

## Install

Open the raw URL of the style in the browser and Stylus offers to install it:

```
https://raw.githubusercontent.com/juanpsm/userstyles/main/redmine-dark.user.css
```

It works the same in Firefox and Chrome. Both end up pointing at this same URL,
so a change here reaches both.

## Edit

Clone, edit, and **bump `@version`**. Stylus compares that version against the
one it has installed and, if it did not go up, it fetches nothing even though
the file changed. The message it shows is `up-to-date: version is unchanged`,
which sends you looking for the problem in the wrong place, because the file
did change.

```bash
git clone git@github.com:juanpsm/userstyles.git
# edit, bump @version
git commit -am "redmine dark: ..."
git push
```

Then, in each browser: Stylus icon, *Manage*, and *Check for update* on the
style. It also updates on its own, following the interval set in Stylus's
options.

## Try a change without publishing it

On the page you want to see, open DevTools and paste the body of the
`@-moz-document` block into a `<style>` tag. That is enough to iterate on the
color of something. Be careful not to read a computed property in the same call
that injects the style: it returns the old value.
