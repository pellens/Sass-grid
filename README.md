# Sass-grid
A Sass based grid system - columns &amp; percentage. Created in Belgium by [Gert Pellens](http://twitter.com/gpellens). A **demo** can be found in `index.html`.

##1. Installation

* Import Sass files in your Sass setup...
* Define your grid settings in *grid.scss*
* Compile Sass files

##2. Examples

###2.1 Column based grid

    <div class="row">

        // Basic markup
        <div class="col-6">6 columns wide</div>
        <div class="col-6">6 columns wide</div>

        // With viewport classes
        <div class="col-6 col-tablet-8">6 columns wide, 8 columns on tablet viewport</div>
        <div class="col-6 col-tablet-4">6 columns wide, 4 columns on tablet viewport</div>

    </div>

###2.2 Percentage based grid

    <div class="row">

        // Basic markup
        <div class="grid-50">50% wide</div>
        <div class="grid-50">50% wide</div>

        // With viewport classes
        <div class="grid-50 tablet-100">50% wide, 100% on tablet viewport</div>
        <div class="grid-50 tablet-100">50% wide, 100% on tablet viewport</div>

    </div>

###2.3 Pushing a grid-element

You can push a grid element by the width of a column:

	// Column based push
	<div class="col-6 col-push-3">6 columns wide, pushed 3 columns to the right</div>

	// Percentage based push
	<div class="grid-50 push-25">50% wide, pushed 25% to the right</div>

##3. Customize

Since every client or project has it's *own requirements*, we have to take this into account when setting up the gridsystem. You can customize:
* viewport breakpoints
* breakpoint titles
* number of columns
* gutter width
* container width

###3.1 Viewports

Define your own viewport names and sizes in *grid.scss*:

    $viewports_width : '960px', '800px', '600px', '400px';
    $viewports_title : 'desktop', 'tablet', 'phablet', 'mobile';

See the table of generated classes at the end of this document...


###3.2 Number of columns

Define the number of columns for your column based grid:

	$columns : 12; // 12 as default

###3.3 Gutter of columns

To define spaces (gutters) between the column based gridelements, we adjust the amount as following:

	$grid_gutter : 2%;

###3.4 Maximum container width

Define your maximum container width in which your grid will deliver it's awesomeness:

	$max_width : 1200px;

##4. Generated classes

| Class  | Values | Example | Viewport | Type |
|--------|--------|---------|-------------|---|
| grid-* | 1 - 100 | grid-50 | Default | Percentage |
| desktop-* | 1 - 100 | desktop-25 | < 960px | Percentage |
| tablet-* | 1 - 100 | tablet-50 | < 800px | Percentage |
| phablet-* | 1 - 100 | phablet-75 | < 600px | Percentage |
| mobile-* | 1 - 100 | mobile-100 | < 400px | Percentage |
| grid-push-* | 1 - 100 | grid-50 | Default | Percentage (push to right) |
| desktop-push-* | 1 - 100 | desktop-25 | < 960px | Percentage (push to right) |
| tablet-push-* | 1 - 100 | tablet-50 | < 800px | Percentage (push to right) |
| phablet-push-* | 1 - 100 | phablet-75 | < 600px | Percentage (push to right) |
| mobile-push-* | 1 - 100 | mobile-100 | < 400px | Percentage (push to right) |
| col-* | 1 - $columns | col-8 | Default | Column |
| col-desktop-* | 1 - $columns | col-desktop-6 | < 960px | Column |
| col-tablet-* | 1 - $columns | col-tablet-6 | < 800px | Column |
| col-phablet-* | 1 - $columns | col-phablet-12 | < 600px | Column |
| col-mobile-* | 1 - $columns | col-mobile- 12 | < 400px | Column |
| col-push-* | 1 - $columns | col-push-3 | Default | Column  (push to right)|
| col-desktop-push-* | 1 - $columns | col-desktop-push-1 | < 960px | Column  (push to right)|
| col-tablet-push-* | 1 - $columns | col-tablet-push-2 | < 800px | Column  (push to right)|
| col-phablet-push-* | 1 - $columns | col-phablet-push-1 | < 600px | Column  (push to right)|
| col-mobile-push-* | 1 - $columns | col-mobile- push-2 | < 400px | Column  (push to right)|
