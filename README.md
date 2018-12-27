<center><img src="logo.png"></center>

# World's Smallest Grid System

<b>microGRID NR</b> is <b style="font-sizex: 16px;">standalone</b>, <b style="font-sizex: 16px;">world's smallest</b> and <b style="font-sizex: 16px;">depedencies free</b> grid system.<br>
Size of gzipped version is just <b style="font-sizex: 20px;">184 bytes</b>.<br>
For example gzipped <code>bootstrap-grid.min.css</code> (Bootstrap 4.1.3) is <span style="color:red;"><b>3195 bytes</b></span>.

## Size Comparision
Let's compare gzipped size of <b>microGRID NR</b> (<b>184 bytes</b>) with another grid systems.

- GRD (503 bytes) <b style="color:red; font-sizex:18px;">~ 173% more</b>
- Simplegrid (644 bytes) <b style="color:red; font-sizex:18px;">~ 250% more</b>
- 960gs (1105 bytes) <b style="color:red; font-sizex:18px;">~ 500% more</b>
- Flexboxgrid (1591 bytes) <b style="color:red; font-sizex:18px;">~ 1636% more</b>
- Bootstrap's 4.1.3 Grid System (3195 bytes) <b style="color:red; font-sizex:18px;">~ 812% more</b>

## Browsers Support
<b>microGRID NR</b> is cross browsers compatible.

## Features
- Lightest in the world - just 184 bytes gzipped (&lt;0.9% of gzipped Bootstrap 3 CSS)
- Single viewport grid system (12 columns)
- Full-width and fixed-width containers
- Built-in column gutters (default: 15px)
- Row wrappers with negative gutters
- Classes naming similar to well known Bootstrap classes (row, container, container-fluid, col, xs-1 ... xs-12)
- Contains only essential & most used features to speedup Your application
- Optimized for best gzip compression
- No javascript, fallbacks or depedencies - just pure CSS
- Cross browsers compatible
- Minified and ready to use
- Easy migration to standard (responsive) microGRID - soon

## Documentation
### Installation
<pre>
&lt;head&gt;
	&lt;link href="microgrid-nr.min.css" rel="stylesheet"&gt;
&lt;/head&gt;
</pre>

I also recommend to set box-sizing CSS property for all HTML elements (<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing" target="_BLANK">Read more about box-sizing property</a>).
<pre>
&lt;head&gt;
	&lt;style&gt;*{box-sizing:border-box}&lt;/style&gt;
	&lt;link href="microgrid-nr.min.css" rel="stylesheet"&gt;
&lt;/head&gt;
</pre>

### Elements
Elements naming and structure is same or similar like in Bootstrap 3.

#### Containers
Containers must contains only <code>row</code> elements.<br>
Only single <code>container</code> or <code>container-fluid</code> per page is allowed.

##### Fixed Width Containers
<pre>
&lt;div class="container"&gt;&lt;/div&gt;
</pre>
By default, <code>container</code> has 100% width.<br>
You can change it to custom value.

##### Full Width Containers
<pre>
&lt;div class="container-fluid"&gt;&lt;/div&gt;
</pre>

#### Rows
Rows must be placed inside <code>container</code> or <code>container-fluid</code> element.<br>
Rows will contain only <code>col</code> elements.
<pre>
&lt;div class="row"&gt;&lt;/div&gt;
</pre>

#### Columns
Columns must be ALWAYS placed inside <code>row</code> element.
<pre>
&lt;div class="col [viewport]-6"&gt;&lt;/div&gt;
</pre>
Example:<br>
<pre>
&lt;div class="col xs-6"&gt;&lt;/div&gt;
</pre>

#### Offsets
There is no built-in classes for columns offset's at the moment.<br>
If You need to make column offset, please use empty column(s) as pseudo-offsets, like in following example.
<pre>
&lt;!-- Pseudo-offset BEGIN --&gt;
	&lt;div class="col xs-6"&gt;&lt;/div&gt;
&lt;!-- Pseudo-offset END &gt;
&lt;!-- Column BEGIN --&gt;
	&lt;div class="col xs-6"&gt;This column has pseudo-offset&lt;/div&gt;
&lt;!-- Column END &gt;
</pre>

#### Full Example
<pre>
&lt;html&gt;
&lt;head&gt;
	&lt;style&gt;*{box-sizing:border-box}&lt;/style&gt;
	&lt;link href="microgrid-nr.min.css" rel="stylesheet"&gt;
&lt;/head&gt;
&lt;body&gt;
	&lt;div class="container-fluid"&gt;
    	&lt;div class="row"&gt;
    		&lt;div class="col xs-4"&gt;A&lt;/div&gt;
    		&lt;div class="col xs-8"&gt;B&lt;/div&gt;
  		&lt;/div&gt;
    	&lt;div class="row"&gt;
    		&lt;div class="col xs-12"&gt;
    			&lt;div class="col xs-4"&gt;C&lt;/div&gt;
    			&lt;div class="col xs-4"&gt;D&lt;/div&gt;
       			&lt;div class="col xs-4"&gt;E&lt;/div&gt;
            &lt;/div&gt;
  		&lt;/div&gt;
     	&lt;div class="row"&gt;
    		&lt;div class="col xs-8"&gt;F&lt;/div&gt;
    		&lt;div class="col xs-4"&gt;G&lt;/div&gt;
  		&lt;/div&gt;
	&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

#### Viewports
<b>microGRID (NR)</b> supports only single viewport (xs).<br>
If You want to develop multiple viewports application, You can use/migrate-to standard (fully responsive) version of microGRID (soon).
