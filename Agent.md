Automatic CSS (ACSS) Variables and CSS Methods
This document groups the ACSS variables and CSS methods (functions and mixins) found in the Automatic CSS documentation up to March 2026. The variables are organized by the purpose or system they belong to (e.g., typography, spacing, buttons). Each variable is briefly described and accompanied by a citation from the official documentation.
Typography
Variable	Purpose
--h1, --h2, … --h6	T‑shirt size–based variables for headings 1–6. They control font-size, line-height and max‑width for each heading[1].
--text-xxl, --text-xl, --text-lg, --text-md, --text-sm, --text-xs	T‑shirt size variables for text sizes, controlling font-size, line-height and max‑width for body text[1].
--heading-font-family, --heading-color, --heading-line-height, etc.	Global heading variables for customizing font family, color, line height and font weight of headings[1].
--text-font-family, --text-color, --text-line-height, etc.	Global text variables controlling base font family, color and line height of body text[1].
--h1-max-width, --text-max-width	Maximum widths for headings and text; useful for controlling line length[1].
--focus-color	Focus color variable used in accessibility classes; you can assign a new value to change the focus ring color on specific elements[2].
Spacing
Variable	Purpose
--space-xs, --space-s, --space-m, --space-l, --space-xl, --space-xxl	Global spacing variables used for margins, padding and gap sizes; follow a t‑shirt naming convention[3].
--section-space-xs, … --section-space-xxl	Section‑spacing variables used for top/bottom padding of sections[3].
Bridge variables (e.g., --space-xl-to-m, --section-space-xl-to-s)	Provide fluid transitions between two spacing sizes (e.g., extra‑large to medium) to create responsive spacing[4].
--gutter	Controls the gutter (horizontal spacing) between elements or columns[3].
Grid and Layout
Variable	Purpose
--grid-1, --grid-2, … --grid-12	Grid variables that set grid-template-columns values for 1–12 equal columns; use with CSS grid layouts[5].
--grid-1-2, --grid-2-1, etc.	Unbalanced grid variables used for layouts with different column spans (e.g., 1fr 2fr)[5].
--grid-gap	Gap value (space between grid items) for grid layouts[5].
--gap (Flex Grid recipe)	Locally scoped variable controlling the gap between items in a flexbox grid; defaults to var(--grid-gap, 1.5rem)[6].
--columns (Flex Grid recipe)	Number of columns in a flexbox grid; default 3[6].
--stretch (Flex Grid recipe)	Flag (1 = true) controlling whether unbalanced items stretch to fill space[6].
--content-width	Main content width variable; used to set max-width for containers and to calculate widths (e.g., calc(var(--content-width) * .75))[7].
--content-width-safe	Safe content width variable; uses max() to add responsive gutters and prevents content from touching screen edges[8].
--width-10, --width-20, … --width-90	Width variables corresponding to 10%–90% of the content width; available when Width Variables option is on[9].
--header-height	Fluid variable for header height; used for sticky offsets and scroll margins[10].
--sticky-offset	Offset for sticky elements; defines the gap between the element and the top of the viewport[11].
Buttons & Links
Variable	Purpose
--btn-background, --btn-background-hover	Background color and hover background for primary buttons[12].
--btn-text-color, --btn-text-color-hover	Text color variables for buttons and their hover state[12].
--btn-text-transform, --btn-text-decoration, --btn-letter-spacing	Control uppercase transform, decoration and letter spacing of button text[12].
--btn-line-height, --btn-font-size, --btn-font-weight, --btn-font-style	Typography variables for button text[12].
--btn-padding-block, --btn-padding-inline	Block and inline padding for buttons (replacing older --btn-pad-y/--btn-pad-x)[12].
--btn-min-width	Minimum width of buttons[12].
--btn-transition-duration	Duration of the button’s hover/focus transition[12].
--btn-border-color, --btn-border-color-hover	Border color variables for normal and hover states[12].
--btn-border-style, --btn-border-width	Border style and width of buttons[12].
--btn-radius	Corner radius for buttons[12].
--btn-outline-background-color, --btn-outline-border-hover, --btn-outline-border-width	Variables for outline buttons (background color, border color on hover, border width)[12].
--btn-outline-text-color, --btn-outline-text-color-hover	Text colors for outline buttons (normal and hover)[12].
--focus-color	A global focus color used by button and other focusable elements; can be overridden locally[2].
Transition variables: --transition-duration, --transition-timing, --transition-delay, and --transition	Provide consistent transition duration, easing function and delay for interactive elements[13]; used by .transition utility to apply a transition.
--hover-duration, --hover-timing	Default animation duration and easing for hover effects; fallback to the global transition values[14].
Borders & Dividers
Variable	Purpose
--radius	Global border radius applied to elements; can be overridden locally[15].
--border-size	Default border width in the global border system[15].
--border-style	Global border style (e.g., solid)[15].
--border-color-light, --border-color-dark	Light and dark border color variables[15].
--border	Shorthand variable combining width, style and color; use --border-light or --border-dark for theme‑specific borders[15].
--divider	Default divider style; includes width, style and color for horizontal/vertical dividers[16].
--divider-dark	Dark divider variant[16].
--divider-gap	Gap between elements when using .divider classes[16].
--divider-inline-size	Width of a vertical divider[16].
--divider-size	Height or width of a horizontal or vertical divider[16].
--divider-color-dark	Dark divider color for dark contexts[16].
--divider-style	Divider line style (e.g., solid, dashed)[16].
Inverted Radius Framework attributes: data-inverted-radius-1-position, data-inverted-radius-1-slice, data-inverted-radius-2-position, data-inverted-radius-2-slice	Attributes used to apply inverted corner radii; they control which corner(s) to invert and how much to slice the radius[17].
Color Scheme & Palette
Variable	Purpose
Semantic status colors: --warning, --info, --success, --danger	Provide base colors for status messaging. Each has partial variables like --{color}-hex, --{color}-hsl, --{color}-h, --{color}-s, --{color}-l, --{color}-rgb, --{color}-r, --{color}-g and --{color}-b to access specific channels[18].
Palette colors: --primary, --secondary, --tertiary, --accent, --base, --neutral	Main palette variables. When customizing or adding colors, declare variables following the pattern --my-color, --my-color-hex, --my-color-hsl, --my-color-h, --my-color-s, --my-color-l, --my-color-rgb, --my-color-r, --my-color-g, --my-color-b[19].
Contextual background variables: --body-bg-color, --bg-light, --bg-dark, --bg-ultra-light, --bg-ultra-dark	Provide contextual backgrounds for different sections or themes[20].
Contextual text variables: --text-light, --text-dark, --text-light-muted, --text-dark-muted	Provide light/dark text colors and muted variants[20].
--surface (light–dark)	Example of using the CSS light-dark() function to define a surface color that automatically switches between light and dark modes[21].
Color-scheme classes: .scheme--light, .scheme--dark	Utility classes to force the page to a specific color scheme, though not variables; they are part of the color scheme system[21].
Card Framework
Variable	Purpose
--card-padding	Padding for the inner content of cards[22].
--card-gap	Gap between content elements inside cards[22].
--card-radius	Border radius for cards[23].
Tokens prefixed --card-…	The framework uses --card-* tokens to manage other card styling aspects (e.g., backgrounds); they can be referenced directly in custom CSS[23].
Dimensions & Columns
Variable	Purpose
--col-count	Number of columns in the CSS columns recipe[24].
--col-min-width	Minimum width before columns stack[24].
--col-gap	Gap between columns (vertical separation)[24].
--row-gap	Vertical gap between rows inside columns[24].
--col-rule-style, --col-rule-width, --col-rule-color	Style, width and color of column dividers[24].
--col-width-s, --col-width-m, --col-width-l	Predefined minimum column widths for small, medium and large columns when using column recipes[24].
--col-rule-width-s, --col-rule-width-m, --col-rule-width-l	Predefined column rule widths for varying sizes[24].
Shadow & Filters
Variable	Purpose
--box-shadow-m, --box-shadow-l, --box-shadow-xl	Predefined box shadow variables used in box shadow classes; names change if custom shadow names are defined (e.g., --box-shadow-primary)[25].
Overlays & Effects
Variable	Purpose
--overlay-color	Default overlay color used by overlay utilities; controls background color of the overlay[26].
--overlay-z-index	Z‑index for overlays (default –1); can be overridden to move overlays above content[26].
Custom overlay variables: --overlay-[n]-bg-color, --overlay-[n]-background, --overlay-[n]-size, --overlay-[n]-position, --overlay-[n]-repeat, --overlay-[n]-attachment, --overlay-[n]-blur, --overlay-[n]-opacity, --overlay-[n]-blend-mode, --overlay-[n]-border-radius, --overlay-[n]-animation, --overlay-[n]-inset, --overlay-[n]-z-index	ACSS supports up to five custom overlays; these variables control each overlay’s background color/gradient, size, position, repeat behaviour, blur, opacity, blend mode, border radius, animation, whether it is inset, and its z‑index[27].
Effects (Hover, Entrance, Exit, Visible)
These variables are used to customize animation effects on hover, entrance, exit and when elements become visible. They allow fine‑grained control over distances, opacity, scale, blur and durations.
Hover Effects
Variable	Purpose
--hover-grow-amount	Scaling amount for the “grow” hover effect[28].
--hover-float-amount	Vertical translation distance for the “float” effect[28].
--hover-shadow	Shadow applied on hover; can be customized with any box-shadow value[29].
--hover-glow-color	Color of the glow around an element on hover[30].
--hover-glow-spread	Spread radius of the glow effect[30].
--hover-glow-opacity	Opacity of the glow effect[30].
Border ripple variables: --border-ripple-color, --border-ripple-width, --border-ripple-duration, --border-ripple-distance	Control the color, thickness, duration and travel distance of the border ripple animation on hover[31].
Border outline variables: --border-outline-color, --border-outline-width, --border-outline-duration	Adjust the color, thickness and duration of the border outline animation[31].
Border underline variables: --border-underline-color, --border-underline-width, --border-underline-duration	Set the color, thickness and duration of underlines drawn on hover[31].
Entrance Effects
Variable	Purpose
--enter-opacity-start	Starting opacity for fade‑in effects[32].
Movement distances: --enter-float-distance, --enter-sink-distance, --enter-slide-distance	Distances elements travel vertically (float/sink) or horizontally (slide) when entering[32].
--enter-scale-start	Initial scale value (e.g., 0.9) when using a “grow” entrance effect[33].
--enter-scale-shrink	Final scale when using a shrink effect[33].
--enter-blur-amount	Amount of blur applied at the beginning of an entrance animation[33].
--enter-parallax-distance	Vertical travel distance for parallax scrolling effect[34].
Exit Effects
Variable	Purpose
--exit-opacity-target	Target opacity for fade‑out effects[35].
--exit-float-distance, --exit-sink-distance, --exit-slide-distance	Travel distances for exiting movements[35].
--exit-blur-amount	Amount of blur applied during exit[36].
--exit-scale-grow	Final scale value for grow exit (element expands)[36].
--exit-scale-amount	Initial scale for shrink exit (element shrinks)[36].
On Visible Effects
Variable	Purpose
--visible-opacity-start	Starting opacity when an element becomes visible (intersection observer)[37].
--visible-float-distance, --visible-sink-distance, --visible-slide-distance	Distances for float, sink and slide animations on visibility[37].
--visible-scale-start, --visible-scale-shrink	Starting scale and shrink target when an element becomes visible[37].
--visible-blur-amount	Blur applied at start of the visible effect[38].
Easing Presets
Variable	Purpose
--ease-smooth, --ease-snappy, --ease-gentle, --ease-bouncy, --ease-elastic	Cubic‑bezier or linear easing presets for animations; recommended for different motion effects (e.g., smooth = general use, snappy = quick interactions)[39].
Gradient Fades & Sticky
Variable	Purpose
--fade-amount	Controls the intensity of gradient fades when using fade--{axis} classes or the fade() mixin[40].
--sticky-offset	Gap between sticky element and viewport top; used to adjust sticky element offset[11].
Forms (WS Form)
ACSS integrates with WS Form and automatically styles form components. While the documentation indicates that many styles come from variables, the relevant variables were not enumerated in the accessible sections due to context limit, so this document does not list them explicitly.
Elements
Blockquotes
The blockquote component exposes a comprehensive set of variables:
Variable	Purpose
--blockquote-padding, --blockquote-gap	Padding and gap within blockquotes[41].
--blockquote-border-width, --blockquote-border-style, --blockquote-border-color, --blockquote-border-radius	Controls border thickness, style, color and radius[41].
--blockquote-background	Background color or gradient for the blockquote[41].
--blockquote-box-shadow	Box shadow applied to the blockquote container[41].
--blockquote-max-inline-size	Maximum width of blockquote content[41].
Text variables: --blockquote-text-color, --blockquote-text-font-family, --blockquote-text-font-style, --blockquote-text-font-size, --blockquote-text-font-weight, --blockquote-text-line-height, --blockquote-text-align, --blockquote-text-transform	Control the typography of <p> elements inside a blockquote[41].
Footer variables: --blockquote-footer-padding, --blockquote-footer-margin-block, --blockquote-footer-font-family, --blockquote-footer-font-size, --blockquote-footer-font-style, --blockquote-footer-font-weight, --blockquote-footer-line-height, --blockquote-footer-text-transform, --blockquote-footer-color	Customize the <footer> element inside blockquotes[42].
Cite variables: --blockquote-cite-font-size, --blockquote-cite-font-weight, --blockquote-cite-font-style, --blockquote-cite-line-height, --blockquote-cite-text-transform, --blockquote-cite-color	Style <cite> elements (e.g., author attribution) inside blockquotes[42].
Ribbons
Variable	Purpose
--ribbon-offset	Distance of a ribbon from its host element’s corner[43].
--ribbon-width	Width of the ribbon[43].
--ribbon-padding	Padding inside the ribbon[43].
--ribbon-background-color	Background color for the ribbon[43].
--ribbon-text-color	Text color inside the ribbon[43].
--ribbon-text-size	Font size of ribbon text[43].
--ribbon-shadow	Box shadow applied to the ribbon[43].
Cards & Recipes
General Variables
Variable	Purpose
--card-padding, --card-gap, --card-radius	Provide padding, gap and border‑radius for card elements; part of the Card Framework[22].
--card-padding and --card-gap can be referenced directly in CSS to align custom elements with card spacing[22].	
Effects Mixins & Functions
ACSS includes SCSS mixins and functions for generating fluid values and performing mathematical operations. These are used inside the custom SCSS area of ACSS:
Name	Type	Purpose
calc()	CSS function	Standard CSS calc() function; ACSS encourages using it with variables for spacing, color channels and other computations[44].
fluid(min, max)	SCSS function	Generates a clamp() function that scales between min and max pixel values; used to create fluid typography or spacing[45].
ctr(px)	SCSS function	Converts a pixel value to rem based on the site’s root font size (use ctr(24) to convert 24 px to rem); assign result to SCSS variable then interpolate[46].
percent(expr)	SCSS function	Multiplies numbers and returns the result as a percentage (e.g., percent(5 * 5) returns 25%)[47].
pow(num, exp)	SCSS function	Raises a number to a power; e.g., pow($my-text-size, 3)[48].
rem(value)	SCSS function	Attaches the rem unit to a unitless number or variable; often used with viewport variables (e.g., rem($vp-max * .33))[49].
fade($axis, $amount)	SCSS mixin	Applies a gradient fade on either axis; uses the --fade-amount variable to control intensity[40].
clickable-parent	SCSS mixin	Extends the clickable area of a link to its parent container for better UX; requires specific HTML structure and ensures accessible focus states[50].
btn(style, prop)	SCSS mixin	Outputs a button of a specific style using the button variables; accepts style name and optional property set arguments[51].
breakpoint($bp) and other breakpoint mixins	SCSS mixins	Used to conditionally apply styles at specified breakpoints (not explicitly detailed here).
card-container, auto-grid, centering, content-grid	SCSS mixins	Provide structured layouts such as card containers, automatic grids and centering; mixins accept arguments for customizing gaps and alignment[51].
gradient-fades	SCSS mixin	Generates gradient fade classes like fade--{axis}; built around the --fade-amount variable[40].
Animation and Motion Methods
Method	Purpose
.transition utility or var(--transition)	Applies the global transition style (duration, timing, delay) defined by --transition-* variables[13].
.ease--{preset} classes	Apply one of the easing presets (--ease-smooth, --ease-snappy, etc.) to transitions and animations[39].
.hover--{effect} classes & variables	Hover effect classes (grow, float, shadow, glow, ripple, etc.) use the corresponding hover variables listed earlier to customize behavior[28].
.enter--{effect}, .exit--{effect}, .visible--{effect}	Entrance, exit and visibility effects that rely on the --enter-*, --exit-*, and --visible-* variables for customizing distance, opacity, blur and scale[32][36].
.sticky utility	Makes an element sticky using CSS position: sticky; the --sticky-offset variable defines the offset from the top[11].
Additional Notes
	WS Form and Forms: The ACSS documentation mentions comprehensive form styling for WS Form; variables likely control input padding, label spacing and colors, but they were not enumerated in the accessible sections.
	Accessibility: The reduce-motion class respects the user’s prefers-reduced-motion settings; the documentation instructs not to disable this by default (no variables associated). The focus classes rely on --focus-color which can be overridden per element[2].
	Mixins: Only a subset of mixins is described here. ACSS offers many mixins (e.g., Card Container, Auto Grid, Breakpoint, Icon) that generate utility classes based on variables. When customizing with SCSS, refer to the ACSS mixin documentation for full usage.

[1] Typography Variables | Automatic CSS Documentation
https://docs.automaticcss.com/typography/typography-variables
[2] Focus Classes | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/accessibility/focus-classes
[3] [4] Spacing Variables | Automatic CSS Documentation
https://docs.automaticcss.com/spacing/spacing-variables
[5] Grid Variables | Automatic CSS Documentation
https://docs.automaticcss.com/grids/grid-variables
[6] Flex Grids (Flexbox Grids) | Automatic CSS Documentation
https://docs.automaticcss.com/flexbox/flex-grids%23locally-scoped-variables
[7] Content Width | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/dimension/content-width
[8] Content Width (Safe) | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/dimension/content-width-safe
[9] Width Utilities | Automatic CSS Documentation
https://docs.automaticcss.com/dimension/width-utilities
[10] Header Height | Automatic CSS Documentation
https://docs.automaticcss.com/dimension/header-height
[11] Sticky | Automatic CSS Documentation
https://docs.automaticcss.com/effects/sticky%23global-sticky-offset
[12] Button Variables | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/buttons-links/button-variables
[13] Transition | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/buttons-links/transition
[14] [28] [29] [30] [31] Hover Effects | Automatic CSS Documentation
https://docs.automaticcss.com/effects/hover-effects
[15] Global Border System | Automatic CSS Documentation
https://docs.automaticcss.com/borders-dividers/global-border-system
[16] Global Divider System | Automatic CSS Documentation
https://docs.automaticcss.com/borders-dividers/global-divider-system
[17] Inverted Radius Framework | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/borders-dividers/inverted-radius-framework
[18] Semantic Colors | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/colors/semantic-colors
[19] Palette Setup | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/colors/palette-setup
[20] Background & Text Assignments | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/colors/background-text-assignments
[21] Modern Color Scheme Workflow | Automatic CSS Documentation
https://docs.automaticcss.com/color-scheme/modern-color-scheme-workflow
[22] [23] Card Framework | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/cards/card-framework
[24] CSS Columns | Automatic CSS Documentation
https://docs.automaticcss.com/columns/css-columns
[25] Box Shadow Classes | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/shadow-filters/box-shadow-classes
[26] Basic Overlays | Automatic CSS Documentation
https://docs.automaticcss.com/overlays/overlay-classes
[27] Custom Overlays | Automatic CSS Documentation
https://docs.automaticcss.com/overlays/custom-overlays
[32] [33] [34] Entrance Effects | Automatic CSS Documentation
https://docs.automaticcss.com/effects/entrance-effects%23starting-opacity
[35] [36] Exit Effects | Automatic CSS Documentation
https://docs.automaticcss.com/effects/exit-effects%23fade-target
[37] [38] On Visible | Automatic CSS Documentation
https://docs.automaticcss.com/effects/visible-effects%23starting-opacity
[39] Easing Presets | Automatic CSS Documentation
https://docs.automaticcss.com/effects/easing-presets
[40] Gradient Fades | Automatic CSS Documentation
https://docs.automaticcss.com/effects/gradient-fades%23fade-utility-classes
[41] [42] Blockquotes | Automatic CSS Documentation
https://docs.automaticcss.com/elements/blockquotes%23main-blockquote-variables
[43] Ribbons | Automatic CSS Documentation
https://docs.automaticcss.com/elements/ribbons%23customizing-your-ribbon
[44] Calc() | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/functions/calc
[45] fluid() Function | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/functions/fluid-function
[46] ctr() Function | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/functions/ctr
[47] percent() Function | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/functions/percent-function
[48] pow() Function | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/functions/pow-function
[49] rem() Function | Automatic CSS Documentation
https://docs.automaticcss.com/3.0/functions/rem-function
[50] Clickable Parent | Automatic CSS Documentation
https://docs.automaticcss.com/mixins/clickable-parent
[51] Automatic CSS Documentation
https://docs.automaticcss.com/mixins/what-are-mixins
