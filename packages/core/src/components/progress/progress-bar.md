---
parent: components
---

@# Progress

Blueprint provides two ways to indicate progress: a horizontal progress bar and a circular spinner.

@## Progress bars

Progress bars can indicate determinate progress towards the completion of a task or an indeterminate
loading state.

@### CSS API

Set the current progress of the bar via a `width` style rule on the inner `.pt-progress-meter`
element. This is a very simple CSS-only component, and input validation for `width` values is
limited: values above `100%` appear as 100% progress and values below `0%` appear as 0%.

Omitting `width` will result in an "indeterminate" progress meter that fills the entire bar.

Markup:
<div class="pt-progress-bar {{.modifier}}">
<div class="pt-progress-meter" style="width: 25%"></div>
</div>
<div class="pt-progress-bar pt-intent-primary {{.modifier}}">
<div class="pt-progress-meter" style="width: 50%"></div>
</div>
<div class="pt-progress-bar pt-intent-success {{.modifier}}">
<div class="pt-progress-meter" style="width: 75%"></div>
</div>
<div class="pt-progress-bar pt-intent-danger {{.modifier}}">
<div class="pt-progress-meter" style="width: 100%"></div>
</div>

.pt-no-stripes   - No stripes
.pt-no-animation - No animation

@### JavaScript API

The `ProgressBar` component is available in the __@blueprintjs/core__ package.
Make sure to review the [general usage docs for JS components](#components.usage).

A `ProgressBar` is a simple stateless component that renders the appropriate HTML markup.
It supports a `value` prop between 0 and 1 that determines the width of the progress meter.
Omitting `value` will result in an "indeterminate" progress meter that fills the entire bar.

Note that the CSS modifiers described in the [CSS API](#components.progress.bar.css)
are supported via the `className` prop.

@interface IProgressBarProps

@reactExample ProgressExample