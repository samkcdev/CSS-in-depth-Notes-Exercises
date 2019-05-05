# Cascade and Specificity

<p>Cascade are set of rules followed by the browser to dertermine which style has to be applied to an HTML element</p>
<p>When browser has to determine which style has to be applied to an HTML element, since there can be more than one stylesheet and there can be conflicts, it follows the below three rules:</p>

<ul>
<li><b>Stylesheet Origin:</b>Source of the styles user-agent style or our style</li>
<li><b>Selector Specificity:</b> Which selectors should take precedence</li>
<li><b>Source Order:</b> Order in which the styles are written in the stylesheet</li>
</ul>

### Stylesheet Origin

The browser applies its own style is called User-agent styles. The style applied by us is called Author styles.
So author styles always overides the user agent styles.
So the origin is first always the
User agent styles which will overwritten by
author styles and author styles with !important always overrides the both

### Selector Specficity

<p>Browser evaluates specificity in two ways: </p>
Inline style or style applied to a selector.
<b>Inline style</b> overide the selector style until we apply !important to that, so inline style has more specificity.
<b>Selector Specificity</b>
ID will have more weightage than the class
So we can we specificity weightage like this
1 0 0 means id and no class and no tags-so this will have more weightage
0 1 0 means no id and one class and no tags-after that this will come
0 0 1 means no id, no class and one tag-only after the above all this will be considered
