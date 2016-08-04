# Sass-grid
A Sass based grid system - columns &amp; percentage. Created in Belgium by [Gert Pellens](http://twitter.com/gpellens). A **demo** can be found in `index.html`.

##Installation

* Import Sass files in your Sass setup...
* Define your grid settings in *grid.scss*
* Compile Sass files

##1. Column based grid

    <div class="row">
        <div class="col-6">6 columns wide</div>
        <div class="col-6">6 columns wide</div>
    </div>

##2. Percentage based grid

    <div class="row">
        <div class="grid-50">50% wide</div>
        <div class="grid-50">50% wide</div>
    </div>

##3. Customize

Since every client or project has it's *own requirements*, we to take this into account when setting up the gridsystem. You can choose the viewport breakpoints, number of columns, gutters and container width.

###3.1 Viewports

Define your own viewport names and sizes in *grid.scss*:

    $viewports_width : '960px', '800px', '600px', '400px';
    $viewports_title : 'desktop', 'tablet', 'phablet', 'mobile';

###3.2 Number of columns

Define the number of columns for your column based grid:

	$columns : 12; // 12 as default

###3.3 Gutter of columns

To define spaces (gutters) between the column based gridelements, we adjust the amount as following:

	$grid_gutter : 2%;

###3.4 Maximum container width

Define your maximum container width in which your grid will deliver it's awesomeness:

	$max_width : 1200px;
