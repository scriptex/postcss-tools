# PostCSS Tools

Placeholders and Mixins for PostCSS

## Placeholders

```css
@define-placeholder clearfix {
	content: '';
	line-height: 0;
	display: table;
	clear: both;
}
```

Usage: `@extend clearfix;`

---

```css
@define-placeholder notext {
	white-space: nowrap;
	text-indent: 100%;
	text-shadow: none;
	overflow: hidden;
}
```

Usage: `@extend notext;`

---

```css
@define-placeholder appearanceNone {
	-webkit-appearance: none;
	-moz-appearance: none;
	appearance: none;
}
```

Usage: `@extend appearanceNone;`

---

```css
@define-placeholder centered {
	display: block;
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	margin: auto;
}
```

Usage: `@extend centered;`

## Mixins

```css
@define-mixin chevron $dimensions,
	$borderWidth,
	$borderColor,
	$margin,
	$rotation,
	$origin,
	$transitionDuration {
	content: '';
	width: $dimensions;
	height: $dimensions;
	display: inline-block;
	vertical-align: middle;
	border-width: $borderWidth;
	border-style: solid;
	border-color: $borderColor;
	margin: $margin;
	transform: rotate($rotation);
	transform-origin: $origin;
	transition: transform $transitionDuration;
}
```

Usage: `@mixin chevron 10px, 0 0 1px 1px, #fff, 0, -45deg, 50% 50%, 0s;`

---

```css
@define-mixin triangle $borderWidth, $borderColor, $margin {
	width: 0;
	height: 0;
	display: inline-block;
	vertical-align: middle;
	border-width: $borderWidth;
	border-style: solid;
	border-color: $borderColor;
	margin: $margin;
}
```

Usage: `@mixin triangle 5px, #fff transparent transparent transparent, 4px 5px 0 0;`

---

```css
@define-mixin letterspacing $tracking {
	letter-spacing: calc($tracking / 1000)em;
}
```

Usage: @mixin letterspacing 32; // 32 is the tracking set in Photoshop

## LICENSE

MIT
