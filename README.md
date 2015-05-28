# named-media-queries

Named media queries based on Bootstrap breakpoints.

| Name         | What      | Description             |
| ---          | ---       | ---                     |
| `portrait`   | <= 480px  | phone (portrait)        |
| `phone`      | <= 768px  | phone (incl. landscape) |
| `mobile`     | <= 992px  | phone + tablet          |
| `nondesktop` | <= 1200px | phone + tablet + laptop |
| `tablet`     | 768px+    | tablet + desktop        |
| `laptop`     | 992px+    | desktop (small)         |
| `desktop`    | 1200px+   | desktop (big)           |

## Reference

```
                   xs          sm          md                lg
                   480         768         992               1200
             '     '     '     '     '     '     '     '     '     '     '
                   '           '           '                 '
portrait    <——————^           '           '                 '
phone       <——————————————————^           '                 '
mobile      <——————————————————————————————^                 '
nondesktop  <————————————————————————————————————————————————^
tablet                         ^————————————————————————————————————————>
laptop                                     ^————————————————————————————>
desktop                                                      ^——————————>
```

## Sass

```
@import 'named-media-queries';
@media #{$phone} {
  div { color: blue; }
}
```

## Vim

Tab completion snippets are available in this repo.

```scss
Plug 'SirVer/ultisnips'
Plug 'rstacruz/named-media-queries'
```

In a CSS file, type `@tablet` `⇥` to activate your snippets.

## Recommended use

* `phone` (<= 768px) and `tablet` (768px+) is likely your main breakpoint where your layout will change.
* Use `portrait` (<= 480px) for any overrides that you may need for small screens.
* Use `laptop` (992px+) to increase whitespace and column widths on bigger screens.
* The rest of the queries are kinda useless, lol.
