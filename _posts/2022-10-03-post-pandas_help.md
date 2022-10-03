---
title: Pandas Help
last_modified_at: 2022-10-03
excerpt_separator: “<!—more—>”
categories:
  - Blog   
tags:  
  -  Python  
---

<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>Pandas</title><style>


ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
	empty-cells: show;
}
.simple-table td {
	height: 29px;
	min-width: 120px;
}

.simple-table th {
	height: 29px;
	min-width: 120px;
}

.simple-table-header-color {
	background: rgb(247, 246, 243);
	color: black;
}
.simple-table-header {
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	max-height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-opaquegray { background-color: rgba(255, 255, 255, 0.0375); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="c1f07c8d-bc5f-470f-aab6-c9bd0a6aded8" class="page mono"><header><div class="page-header-icon undefined"><span class="icon">🐼</span></div><h1 class="page-title">Pandas</h1></header><div class="page-body"><p id="e78f9166-6280-4899-8b24-689599c7dbd2" class="block-color-gray_background"><strong>Grouping</strong></p><ul id="5c0bd19f-1a61-45b0-9d44-849cf1596c02" class="block-color-gray_background toggle"><li><details open=""><summary>group by a category, count the totals, and sort descending</summary><pre id="562f2ca6-94dd-4f93-916e-11703bda8793" class="code code-wrap"><code>df.groupby(&#x27;col1&#x27;, as_index = False).size().sort_values(ascending=False)
lemurs.groupby(&#x27;taxon&#x27;, as_index = False).size().sort_values(by=&#x27;size&#x27;,ascending=False)</code></pre></details></li></ul><ul id="1483e721-4169-46df-9832-9e6dc8a696fd" class="block-color-gray_background toggle"><li><details open=""><summary>group by a column, then find the max value of another col for each value of the first col	</summary><pre id="1d336d64-6343-4ee6-b090-80fd7790a22f" class="code code-wrap"><code>df.groupby(&#x27;price&#x27;)[&#x27;points&#x27;].max().sort_index(ascending=False)</code></pre></details></li></ul><ul id="b6eb658c-0102-4af0-aac9-26ec8e7b94d6" class="block-color-gray_background toggle"><li><details open=""><summary>group by a col and find the mean of another col</summary><pre id="feebb32a-0309-4fa1-93ba-20d76b0b0f7e" class="code code-wrap"><code>df.groupby(&#x27;taster_name&#x27;)[&#x27;points&#x27;].agg(&quot;mean&quot;)</code></pre></details></li></ul><ul id="2fa755b3-b8aa-458d-8b63-3df826f81041" class="block-color-gray_background toggle"><li><details open=""><summary>groupby used like a histogram to obtain counts on sub-ranges of a variable</summary><pre id="8951f308-07c3-4617-9559-58580096b88e" class="code"><code>df.groupby(pd.cut(df.a, range(0, 1, 2))).size()</code></pre></details></li></ul><ul id="c87516bd-729c-4fe3-a3bf-e3633c509ccf" class="block-color-gray_background toggle"><li><details open=""><summary>find the max and min of a second col when grouping by one col	</summary><pre id="fe645c03-8af0-41d8-aeea-eacc0d3f3e78" class="code code-wrap"><code>df.groupby(&#x27;variety&#x27;)[&#x27;price&#x27;].agg([min, max])</code></pre></details></li></ul><ul id="75c83a87-c9b3-48f1-9e1f-1626f15cf517" class="block-color-gray_background toggle"><li><details open=""><summary>apply multiple functions to groupby cols</summary><pre id="8607df61-162f-4793-849d-41387fd32cb1" class="code"><code>df = pd.DataFrame(np.random.rand(4,4), columns=list(&#x27;abcd&#x27;))
df[&#x27;group&#x27;] = [0, 0, 1, 1]

df.groupby(&#x27;group&#x27;).agg({&#x27;a&#x27;:[&#x27;sum&#x27;, &#x27;max&#x27;], 
                         &#x27;b&#x27;:&#x27;mean&#x27;, 
                         &#x27;c&#x27;:&#x27;sum&#x27;, 
                         &#x27;d&#x27;: lambda x: x.max() - x.min()})</code></pre></details></li></ul><ul id="3e893d49-a183-4f3b-9239-f8591b613e4a" class="block-color-gray_background toggle"><li><details open=""><summary>find correlation between two columns	</summary><pre id="5398419a-d10b-4504-8435-bd8bf7890745" class="code"><code>df[&#x27;column1&#x27;].corr(df[&#x27;column2&#x27;])</code></pre></details></li></ul><ul id="c9364f40-75b7-4f3d-a72c-272315a54526" class="block-color-gray_background toggle"><li><details open=""><summary>chaining</summary><pre id="a9d78de1-62d2-4183-a95b-a085cd91252c" class="code code-wrap"><code>(autos
[cols]
.select_dtypes(int)
.describe()
)</code></pre></details></li></ul><ul id="e8c95d58-8dc9-4eec-8d1d-cb6e5babeb74" class="block-color-gray_background toggle"><li><details open=""><summary>find the index of a df	</summary><pre id="111f82d4-dc94-401e-bb34-1bfd878d937f" class="code"><code>df.index[_]</code></pre></details></li></ul><ul id="8d141212-bf8f-4307-8b67-24c8e91c77a9" class="block-color-gray_background toggle"><li><details open=""><summary>what are the names of the columns?	</summary><pre id="1c95190c-379d-4f2d-aa96-689d695260e0" class="code"><code>list(df.columns)
list(data.columns.values)</code></pre></details></li></ul><ul id="6a7dc9ab-4217-4512-b3bf-5f892da2fffd" class="block-color-gray_background toggle"><li><details open=""><summary>get the top 10 by category count</summary><pre id="3f7497ce-dc28-4660-ac34-0e3be61f617c" class="code code-wrap"><code>pd.value_counts(lemurs[&#x27;taxon&#x27;]).iloc[:10].index # names
pd.value_counts(lemurs[&#x27;taxon&#x27;]).iloc[:10] # names and counts</code></pre></details></li></ul><ul id="9bbf3944-c6e3-4d7f-b207-9ca48b760919" class="block-color-gray_background toggle"><li><details open=""><summary>within a column, count the total for each unique entry</summary><pre id="08913ade-5d2d-4bee-8cdd-d6e28b57ca78" class="code code-wrap"><code>mydf.mycol.value_counts(dropna=False)</code></pre></details></li></ul><p id="432b726d-900b-4a6f-a95c-e356edb9d7b1" class="">
</p><p id="72a69d4b-1090-4e53-a89c-c126b738b48c" class="block-color-teal_background"><strong>Strings</strong></p><ul id="6d0c0fac-d421-4900-9bf6-dbee553d626c" class="toggle"><li><details open=""><summary>replace or remove characters in a string</summary><pre id="9f5faf8b-fbeb-4331-aed7-bbe1d1558c2a" class="code code-wrap"><code>df[&#x27;PPI&#x27;].replace(&#x27;PPI/&#x27;,&#x27;&#x27;,regex=True,inplace=True)</code></pre></details></li></ul><p id="586b2a24-059e-4b5e-b679-47798bbbba41" class="">
</p><h3 id="eecdf6a1-700a-465c-8344-9aaf73faf3d8" class="block-color-yellow_background">Plots</h3><ul id="4787f906-ff62-4c30-9241-4fab9d29de63" class="block-color-yellow_background toggle"><li><details open=""><summary>make a line plot in seaborn	</summary><pre id="5ace634b-ea1e-4f86-8150-83fa1cf2e472" class="code"><code>sns.lineplot(data=financial_data) # will do multiple lines</code></pre></details></li></ul><ul id="3855bf28-53e0-49f8-a0a1-bcf57a5398ab" class="block-color-yellow_background toggle"><li><details open=""><summary>make a single line plot in seaborn</summary><pre id="35959be2-00b3-484d-8ee8-f7a0e9239991" class="code code-wrap"><code>sns.lineplot(data=df[&#x27;col_name&#x27;], label=&quot;This is the line&quot;)</code></pre></details></li></ul><ul id="a6fe4434-aaf7-4f73-8b96-7792837ecb06" class="block-color-yellow_background toggle"><li><details open=""><summary>make a barplot if the index is month</summary><pre id="d13edce4-c965-49f2-8845-0eca3e86651d" class="code"><code>sns.barplot(x=df.index, y=df[&#x27;col_name&#x27;])	

# You must select the indexing column with flight_data.index, 
# and it is not possible to use flight_data[&#x27;Month&#x27;] (which will return an error). 
# This is because when we loaded the dataset, 
# the &quot;Month&quot; column was used to index the rows. 
# We always have to use this special notation to select the indexing column.</code></pre></details></li></ul><ul id="5958c656-75da-454c-a99b-a2d3a407da8c" class="block-color-yellow_background toggle"><li><details open=""><summary>plot a histogram in seaborn	</summary><pre id="c2481e0b-a0f0-42e9-aaf2-fed0a3f35a6b" class="code code-wrap"><code>sns.histplot(data=lemurs, x=&quot;age_at_death_y&quot;)</code></pre></details></li></ul><ul id="02bac938-d89c-4399-90ce-5480f2c4f731" class="block-color-yellow_background toggle"><li><details open=""><summary>how to do a heatmap with seaborn	</summary><pre id="f405737d-aff2-4fd5-9659-eb4e0a0b22b6" class="code"><code>sns.heatmap(data=df, annot=True)</code></pre></details></li></ul><ul id="7d611bb6-9e36-47ef-b2cf-fa9fa67d07db" class="block-color-yellow_background toggle"><li><details open=""><summary>sort a bar or column graph</summary><pre id="ed5be65d-697d-449e-b75b-f499938fb97f" class="code"><code># How to sort col or bar graph
import pandas as pd
%matplotlib inline
a = pd.Series([4,8,6,7,8,3,9,7])
b = pd.Series([3,6,8,3,4,6,10,4])
a_b = a+b
df = pd.concat([a,b,a_b],axis=1,join=&#x27;inner&#x27;)
df.columns = [&#x27;a&#x27;,&#x27;b&#x27;,&#x27;c&#x27;]

df.sort_values(&#x27;c&#x27;, ascending=False)[[&#x27;a&#x27;,&#x27;b&#x27;]].plot.bar(stacked=True, rot=0)</code></pre></details></li></ul><ul id="c5e3275a-faa1-402b-b0e2-65afb4c2030e" class="block-color-yellow_background toggle"><li><details open=""><summary>plotly bar chart sort</summary><pre id="bb69bde7-59a6-4a5b-91f4-f48a34f3ffb0" class="code"><code>fig.update_layout(xaxis={&#x27;categoryorder&#x27;:&#x27;total descending&#x27;})
fig.show()</code></pre></details></li></ul><ul id="3c9532fd-60bd-440b-b990-86e798255b28" class="block-color-yellow_background toggle"><li><details open=""><summary>plotly bar chart show values</summary><pre id="4ae4b3d8-2763-4d72-a570-e4d692be4f79" class="code code-wrap"><code>fig = px.bar(df1, x=&#x27;Make&#x27;, y=&#x27;LowValue&#x27;, color=&#x27;Dimension&#x27;, barmode=&#x27;group&#x27;, text=&#x27;LowValue&#x27;)
fig.show()</code></pre></details></li></ul><ul id="9ac424ed-ebc1-4711-928e-50d4855f1af0" class="block-color-yellow_background toggle"><li><details open=""><summary>simple pie plot</summary><pre id="1e0b189f-d325-442b-b1ee-8be0383d2244" class="code code-wrap"><code>data[‘Age_Group’].value_counts().plot(kind=’pie’, figsize=(6,6))</code></pre></details></li></ul><ul id="a71850e0-76c5-451a-b215-92919e017f92" class="block-color-yellow_background toggle"><li><details open=""><summary>unstack and plot	</summary><pre id="314b55ae-77c5-49e5-acec-2946e6fd510e" class="code code-wrap"><code>(autos
.assign(country = autos2.make.apply(country))
.groupby([&#x27;year&#x27;, &#x27;country&#x27;])
.mean()
.unstack()
#.city08
#.plot()
#.legend(bbox_to_anchor(1,1))
)

# data  from https://github.com/mattharrison/datasets/tree/master/data</code></pre></details></li></ul><ul id="b285fc4a-ff1a-4824-9006-1dcbc363c193" class="block-color-yellow_background toggle"><li><details open=""><summary>how to do a scatterplot with a regression line	</summary><pre id="7028e2ba-ea60-46b1-b072-486c99ca3b42" class="code"><code>sns.regplot(x=df[&#x27;col_1&#x27;], y=df[&#x27;col_2&#x27;], hue=df[&#x27;col_3&#x27;]))</code></pre></details></li></ul><ul id="e9ea40d8-617e-4843-882b-c83b0d7f6fd9" class="block-color-yellow_background toggle"><li><details open=""><summary>do a scatterplot with 2 separate regression lines	</summary><pre id="cc04190d-cadb-42b8-ad72-143dd5571b73" class="code"><code>sns.lmplot(x=&quot;bmi&quot;, y=&quot;charges&quot;, hue=&quot;smoker&quot;, data=df)	
# note that the x and y are assigned differently</code></pre></details></li></ul><ul id="d6c13d53-2578-49a4-82a7-c61918d975bf" class="block-color-yellow_background toggle"><li><details open=""><summary>make a categorical scatterplot (swarm plot)	</summary><pre id="d9942516-33d7-4c0b-af02-0979fa1d89cf" class="code"><code>sns.swarmplot(x=df[&#x27;smoker&#x27;], y=df[&#x27;charges&#x27;])</code></pre></details></li></ul><ul id="a4176946-e76a-472c-b27a-2b218c467e25" class="block-color-yellow_background toggle"><li><details open=""><summary>remove extra text from graphs and plots</summary><pre id="73aaf918-1a52-421d-b18a-fd002e8a6288" class="code"><code># put &quot;;&quot; at the end of the line for the plots and the annoying text goes away</code></pre></details></li></ul><ul id="fde959c6-f9f4-4f41-b75a-71b67115c51f" class="block-color-yellow_background toggle"><li><details open=""><summary>the plotly bar graph is washed out</summary><pre id="c3d93d98-dff3-45be-b4fc-6c9dd32ebdf2" class="code code-wrap"><code># This is because of the bar outline, which can be removed by setting the marker.line.width attribute to 0:
fig.update_traces(dict(marker_line_width=0))
# https://plotly.com/python/discrete-color/#discrete-color-with-plotly-express</code></pre></details></li></ul><ul id="10a49150-cf74-4b25-888c-bd3749ee81b1" class="toggle"><li><details open=""><summary>donut chart in Plotly</summary><pre id="c09c3b17-9dfb-4946-aa68-9e3effb0c8d2" class="code code-wrap"><code>fig7 = go.Figure(data = go.Pie(values = values, 
                               labels = labels, hole = 0.4,
                               pull = [0,0.25,0,0],
                               marker_colors = colors ))
fig7.update_traces(hoverinfo=&#x27;label+percent&#x27;,
                   textinfo=&#x27;percent&#x27;, textfont_size=20)
fig7.update_layout(
                   title_text = &#x27;Population Economically Active&#x27;,
                   title_font = dict(size=25,family=&#x27;Verdana&#x27;, 
                                     color=&#x27;darkred&#x27;))
fig7.add_annotation(x= 0.5, y = 0.5,
                    text = &#x27;Year 2017&#x27;,
                    font = dict(size=20,family=&#x27;Verdana&#x27;, 
                                color=&#x27;black&#x27;),
                    showarrow = False)
fig7.show()</code></pre></details></li></ul><p id="8c86956f-e387-4837-bf04-7471981550bb" class="">
</p><p id="bd248f68-0bb4-4b70-a819-2609275ab5b7" class="">
</p><ul id="ab3f9782-2925-4cd5-acf1-71f2e2bb461b" class="toggle"><li><details open=""><summary>how to look at things that correlated with outcome col	</summary><pre id="bea1ad53-161a-4a6e-95a2-12bd4246e461" class="code"><code>df_corr=df.corr()
df_corr.loc[:,[&#x27;match&#x27;]].sort_values(&#x27;match&#x27;). 
# where &#x27;match is the outcome col</code></pre></details></li></ul><ul id="38964b10-f24f-469d-a2cb-9edba9ba7743" class="toggle"><li><details open=""><summary>there are spaces in the column names - &quot; Symbol &quot; vs &quot;Symbol&quot;	</summary><pre id="a55009c7-18a4-4db6-b471-b367e97a227a" class="code"><code>df.columns = df.columns.str.replace(&#x27; &#x27;, &#x27;&#x27;) # There are spaces in the names of some cols</code></pre></details></li></ul><ul id="3da38e98-9405-480e-b87c-7cd58cee846d" class="toggle"><li><details open=""><summary>the index is dates and doing an aggregate function leaves no names of the resultant cols	</summary><pre id="5bdc5074-31f0-4e8a-90b2-855a8f38b63b" class="code"><code>df.groupby(&#x27;Symbol&#x27;)[&#x27;Shares&#x27;].sum().reset_index().sort_values(by=[&#x27;Shares&#x27;], ascending = False)

groupby([&#x27;col1&#x27;, &#x27;col2&#x27;], as_index = False)</code></pre></details></li></ul><ul id="f5207f4e-c10e-44ac-b9bf-695f54af4297" class="toggle"><li><details open=""><summary>get unique values from a list	</summary><pre id="6c83aac4-4018-40da-a893-900e9c39227f" class="code"><code>def unique(list1):
    x = np.array(list1)
    print(np.unique(x))
tickers = unique(tickers)</code></pre></details></li></ul><ul id="aa3f517c-f299-4f3d-8543-daa18ca5f094" class="toggle"><li><details open=""><summary>how many rows and cols</summary><pre id="fd82e9f2-a721-4f03-94ce-a54bfa636bfb" class="code"><code>df.shape()</code></pre></details></li></ul><ul id="556a7601-5321-48f1-bbae-222818480b48" class="toggle"><li><details open=""><summary>show correlations in the df</summary><pre id="fbfcf6ee-634f-4faf-b45f-8a2d9233d76d" class="code"><code>df.corr()</code></pre><ul id="f4ce0cb2-e4d5-45d2-80d3-13465c62b064" class="toggle"><li><details open=""><summary>convert col to a list</summary><pre id="1a7a01f2-d6c6-479e-a08c-d77653fd5836" class="code"><code>tickers = []
for item in df[&#x27;Symbol&#x27;]:
    #results_df=results_df.append(item)
    tickers.append([item])</code></pre></details></li></ul></details></li></ul><ul id="b438f8e7-ae91-4b4e-9bf4-13d7236a0610" class="toggle"><li><details open=""><summary>get the data types</summary><pre id="820d2c34-7d90-457d-a1b0-75eab070abff" class="code"><code>df.dtypes</code></pre></details></li></ul><ul id="42c9257e-29f5-4548-b803-9926e0238e8e" class="toggle"><li><details open=""><summary>get info about the df</summary><pre id="036add5d-443c-4be2-8c27-c7dd315e885f" class="code"><code>df.info()</code></pre></details></li></ul><ul id="d01cf52b-4cc5-42df-b61f-ba4ede5bb44d" class="toggle"><li><details open=""><summary>where are built-in databases to experiment with in Pandas</summary><pre id="a3547a45-acaf-477d-be63-ec019108aadf" class="code"><code>sns.get_dataset_names()

df = sns.load_dataset(&quot;planets&quot;) 
df.head()
df.shape</code></pre></details></li></ul><ul id="21645e01-cc8a-4b3d-b47c-b64a63e31258" class="toggle"><li><details open=""><summary>create a df</summary><pre id="29dad88e-5e84-4480-a7cc-bb97c13e5259" class="code"><code># initialise data of lists.
data = {&#x27;Name&#x27;:[&#x27;Tom&#x27;, &#x27;nick&#x27;, &#x27;krish&#x27;, &#x27;jack&#x27;],
        &#x27;Age&#x27;:[20, 21, 19, 18]}
 
# Create DataFrame
df = pd.DataFrame(data)</code></pre></details></li></ul><h3 id="30c1891a-d514-439c-b88f-4e959ff00389" class="">Filter</h3><ul id="e37846cf-0a1f-46d9-a4e9-f8cfc8e88b76" class="toggle"><li><details open=""><summary>filter a df</summary><pre id="519bb048-5b87-4894-8ecf-a436f6b38929" class="code"><code># Filter

df.loc[df[&#x27;a&#x27;] &gt; 5]</code></pre></details></li></ul><ul id="f7c0c285-4427-480d-9af9-468a94d25ddf" class="toggle"><li><details open=""><summary>filter df if col contains a string</summary><pre id="17af2b8a-c032-4c80-b178-e48a6d39cbcc" class="code code-wrap"><code># Filter if contains string (or does not contain string)

a = pd.Series([&#x27;dog food&#x27;, &#x27;cat food&#x27;, &#x27;giraffe&#x27;])
b = pd.Series([&#x27;orange&#x27;,&#x27;zebra&#x27;, &#x27;apple&#x27;])

df = pd.concat([a,b],axis=1,join=&#x27;inner&#x27;)
df.columns = [&#x27;stuff&#x27;,&#x27;things&#x27;]

df.loc[df[&#x27;stuff&#x27;].str.contains(&#x27;food&#x27;)]

# df.loc[~df[&#x27;stuff&#x27;].str.contains(&#x27;food&#x27;)]  # for string does NOT contain</code></pre></details></li></ul><ul id="e88a2224-ad48-4236-9dbf-29767af5980a" class="toggle"><li><details open=""><summary>multiple filters</summary><pre id="e8b8b5b5-0774-4fdf-b8bb-a6624a12da7b" class="code code-wrap"><code># Multiple filters

df.loc[(df[&#x27;a&#x27;] &gt; 5) &amp; (df[&#x27;c&#x27;] != 12)]</code></pre></details></li></ul><ul id="89f45d53-1863-4a9b-8155-4b9d3844fad3" class="toggle"><li><details open=""><summary>filter by regex</summary><pre id="82de1c06-ec90-4c45-9e50-80ddad6446b5" class="code"><code># Filter by regex (here is for case insensitive - re.I flag - and starts with &#x27;g&#x27;)

import re
df.loc[df[&#x27;stuff&#x27;].str.contains(&#x27;^g[a-z]*&#x27;, flags=re.I, regex = True)]</code></pre></details></li></ul><ul id="8f463dff-7634-4302-ab7b-d3a3cd97e456" class="toggle"><li><details open=""><summary>filter and modify</summary><pre id="b7111f6a-88af-43c5-90df-743398f2512c" class="code code-wrap"><code># Filter and modify

df.loc[df[&#x27;stuff&#x27;] == &#x27;cat food&#x27;, &#x27;things&#x27; ]= &#x27;banana&#x27;</code></pre></details></li></ul><ul id="c535bd80-39a2-42ca-9e43-eb5104aca7c4" class="toggle"><li><details open=""><summary>filter by a series</summary><pre id="c27e81b0-60cf-47f0-b360-8023e096f42a" class="code code-wrap"><code>df[df[&#x27;category&#x27;].isin([&quot;1&quot;,&quot;0&quot;])]</code></pre></details></li></ul><ul id="f89c0a6f-c599-4b42-b902-d7bcee5920ea" class="toggle"><li><details open=""><summary>filter and modify multiple</summary><pre id="c8a3b737-93a7-4297-bfbf-de9c906926b9" class="code"><code># Filter and modify multiple

df.loc[df[&#x27;stuff&#x27;] == &#x27;cat food&#x27;, [&#x27;stuff&#x27;,&#x27;things&#x27; ]]= [&#x27;snail food&#x27;,&#x27;banana&#x27;]</code></pre></details></li></ul><ul id="0a214e07-d51e-45de-99c3-db8eea7d26e6" class="toggle"><li><details open=""><summary>filter with multiple external criteria</summary><pre id="8aa57ec8-de2c-42e2-9eb5-4a9f30f1e8d6" class="code"><code>np.random.seed(1)
# quick way to create a data frame for testing 
df_test = pd.DataFrame(np.random.randn(3, 4), columns=[&#x27;a&#x27;, &#x27;b&#x27;, &#x27;c&#x27;, &#x27;d&#x27;]) \
    .assign(target=lambda x: (x[&#x27;b&#x27;]+x[&#x27;a&#x27;]/x[&#x27;d&#x27;])*x[&#x27;c&#x27;])
df = df_test.copy()
cr1 = df[&quot;a&quot;] &gt; 0
cr2 = df[&quot;b&quot;] &lt; 0
cr3 = df[&quot;c&quot;] &gt; 0
cr4 = df[&quot;d&quot;] &gt;-1

df[cr1 &amp; cr2 &amp; cr3 &amp; cr4]</code></pre></details></li></ul><ul id="e06bd098-bdb0-4090-9275-ca75438b8de4" class="toggle"><li><details open=""><summary>creating complex filters using functions on rows</summary><pre id="fc56113a-432d-4042-a983-ebff8955a2ae" class="code"><code>df[df.apply(lambda x: x[&#x27;b&#x27;] &gt; x[&#x27;c&#x27;], axis=1)]</code></pre></details></li></ul><ul id="38be58e7-b2a5-4aa3-9fc0-93afaa495528" class="toggle"><li><details open=""><summary>exclude some categories</summary><pre id="03b34e28-5ac1-432e-80db-5fafdb1f5a9b" class="code code-wrap"><code>#expense[expense.category != &#x27;Income&#x27;]
expense[~expense.category.isin([&quot;Income&quot;, &quot;Transfer&quot;])]</code></pre></details></li></ul><p id="28d0c6c0-494d-4067-bf3d-fd7bfe4fcfeb" class="">
</p><ul id="7a359d11-08ae-46fd-92f0-1257cd5bed15" class="toggle"><li><details open=""><summary>pandas version of <strong>mutate</strong>, using <strong>assign</strong></summary><pre id="fa8320e2-0d0b-4dbb-90c4-14ab42b14d9e" class="code code-wrap"><code>#Using .assign you can make multiple
#operations that depend on the
#previous ones without the need
#of creating intermediate variables
import pandas as pd

df = pd.DataFrame({
    &#x27;name&#x27;: [&#x27;alice&#x27;,&#x27;bob&#x27;,&#x27;charlie&#x27;,&#x27;daniel&#x27;],
    &#x27;age&#x27;: [25,66,56,78]
})

df.assign(
    is_senior = lambda dataframe: dataframe[&#x27;age&#x27;].map(lambda age: True if age &gt;= 65 else False) 
).assign(
    name_uppercase = lambda dataframe: dataframe[&#x27;name&#x27;].map(lambda name: name.upper()),
).assign(
    name_uppercase_double = lambda dataframe: dataframe[&#x27;name_uppercase&#x27;].map(lambda name: name.upper()+&quot;-&quot;+name.upper())
)</code></pre></details></li></ul><ul id="060cdb4c-d2f4-4a53-8e53-7ccee0c9b50d" class="toggle"><li><details open=""><summary>rename columns</summary><pre id="3d140b73-52b8-4db5-9eb0-75b17ba2275d" class="code"><code>aapl_df = aapl_df.rename(columns = {&#x27;index&#x27;:&#x27;Date&#x27;})</code></pre></details></li></ul><ul id="9a844580-4ad5-463f-99b0-6babcaf41c4e" class="toggle"><li><details open=""><summary>excel sheet with spaces in column names</summary><pre id="fa5d75ca-a6a3-4d24-b508-88f874e3f2b4" class="code"><code>df.columns = [c.lower().replace(&#x27; &#x27;, &#x27;_&#x27;) for c in df.columns]</code></pre></details></li></ul><ul id="0b8aa9d6-69a3-4ecb-b97e-94402296ca82" class="toggle"><li><details open=""><summary>reset the index in place</summary><pre id="a885d5dc-571d-4465-a25b-24fe5c1055b5" class="code"><code>aapl_df.reset_index(inplace=True)</code></pre></details></li></ul><ul id="29e1d62a-a0fd-4c0f-a9df-8a5ea4bc47c9" class="toggle"><li><details open=""><summary>load basic modules</summary><pre id="01de134f-43b3-48ae-9edf-f218952fe335" class="code"><code>import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
import plotly.express as px
#import yfinance as yf</code></pre></details></li></ul><ul id="8dfff8d6-21db-4f93-80ad-50a1646d1313" class="toggle"><li><details open=""><summary>style the df</summary><pre id="51983380-f4cb-4ab6-8142-4f7a299e8aff" class="code"><code>df_out = (
  df.style.format({&quot;a&quot;:&quot;${:.2f}&quot;, &quot;target&quot;:&quot;${:.5f}&quot;})
 .hide_index()
 .highlight_min(&quot;a&quot;, color =&quot;red&quot;)
 .highlight_max(&quot;a&quot;, color =&quot;green&quot;)
 .background_gradient(subset = &quot;target&quot;, cmap =&quot;Blues&quot;)
 .bar(&quot;number&quot;, color = &quot;lightblue&quot;, align = &quot;zero&quot;)
 .set_caption(&quot;DF with different stylings&quot;)
) ; df_out</code></pre></details></li></ul><ul id="e5aff263-d3f8-401d-a07d-e52731521969" class="toggle"><li><details open=""><summary>col names to lower case</summary><pre id="70fbc12f-b6a8-464b-af2d-abd0d0be8eb8" class="code"><code>## Lower-case all DataFrame column names 
df = df_test.copy() ; df
df.columns = [&quot;A&quot;,&quot;BGs&quot;,&quot;c&quot;,&quot;dag&quot;,&quot;Target&quot;]
df.columns = map(str.lower, df.columns); df

# better
df.columns = df.columns.str.lower(); df</code></pre></details></li></ul><ul id="4e5d8140-b02f-4954-a9a2-8e444694b1e1" class="toggle"><li><details open=""><summary>calculate the % of missing values in each <strong>column</strong></summary><pre id="a369a125-e34f-4934-afb0-0d1e26fbc004" class="code"><code>&quot;&quot;&quot;Calculate the % of missing values in each column&quot;&quot;&quot;
df.isna().mean()</code></pre></details></li></ul><ul id="5879fe37-e08c-4178-8f5c-19156108c64e" class="toggle"><li><details open=""><summary>calculate % of missing values in each <strong>row</strong></summary><pre id="c65e3dac-934e-4a4c-a4af-dacfa3f3d2b9" class="code code-wrap"><code>&quot;&quot;&quot;Calculate the % of missing values in each row&quot;&quot;&quot;
rows = df.isna().mean(axis=1) ; df.head()</code></pre></details></li></ul><ul id="6db07662-c6de-4416-bfe6-f1ab490024ea" class="toggle"><li><details open=""><summary>use a local variable use inside a query of pandas using @</summary><pre id="7cdfaa47-a9bb-4ab8-842f-574e66010f85" class="code"><code>mean = df[&quot;a&quot;].mean()
df.query(&quot;a &gt; @mean&quot;)</code></pre></details></li></ul><ul id="7940cab1-40ba-4310-9a46-9d6980eadd43" class="toggle"><li><details open=""><summary>normalize a df</summary><pre id="768c057e-ecfd-4598-b0f7-bd45ee769435" class="code"><code># one liner to normalize a data frame
(df[[&quot;a&quot;,&quot;b&quot;]] - df[[&quot;a&quot;,&quot;b&quot;]].mean()) / (df[[&quot;a&quot;,&quot;b&quot;]].max() - df[[&quot;a&quot;,&quot;b&quot;]].min())</code></pre></details></li></ul><ul id="b4ee9025-28ca-4bf1-b4f6-717c03b81585" class="toggle"><li><details open=""><summary>exclude certain data type or include certain data types</summary><pre id="61d2ca1e-898e-4ac4-8630-aeb9e2396ac4" class="code"><code>df.select_dtypes(exclude=[&#x27;O&#x27;,&#x27;float&#x27;])
df.select_dtypes(include=[&#x27;int&#x27;])</code></pre></details></li></ul><ul id="35de418b-580d-44e9-af78-17185352f3ba" class="toggle"><li><details open=""><summary>apply and map</summary><pre id="7cba417d-46bf-4983-a78f-f45e0f0e11ca" class="code"><code># add 2 to row 3 and return the series
df[[&quot;a&quot;,&quot;b&quot;,&quot;c&quot;]].apply(lambda x: x[0]+2,axis=0)</code></pre></details></li></ul><ul id="82dc552f-a790-4f69-9a60-15308cec3719" class="toggle"><li><details open=""><summary>calculations with df columns that have missing values</summary><pre id="278dc3e4-e150-4597-81fa-4a93f3196b67" class="code"><code># In example below, swap in 0 for df[&#x27;col1&#x27;] cells that contain null 
df[&#x27;new3&#x27;] = np.where(pd.isnull(df[&#x27;b&#x27;]),0,df[&#x27;a&#x27;]) + df[&#x27;c&#x27;]</code></pre></details></li></ul><ul id="e4f8ad84-1435-42f9-87be-683dcfb8bdee" class="toggle"><li><details open=""><summary>replace</summary><pre id="66c4a42a-c3ba-409f-b86d-7cbba12048aa" class="code"><code>df[&quot;a&quot;].round(2).replace(0.87, 17, inplace=True)
df[&quot;a&quot;][df[&quot;a&quot;] &lt; 4] = 19</code></pre></details></li></ul><h3 id="f0555e11-c782-4871-85f4-388d281bc3c7" class="">Import and Export</h3><ul id="24b827ae-ed3d-4b2f-aa8e-ad82261f3bf6" class="toggle"><li><details open=""><summary>tricks with import/reading of data and dtypes</summary><pre id="3cc2b068-aa10-4060-b9f9-b3d6c1c6959c" class="code"><code>df_out = pd.read_csv(&quot;data.csv&quot;, index_col=0,
                 parse_dates=[&#x27;D&#x27;],
                 dtype={&quot;c&quot;:&quot;category&quot;, &quot;B&quot;:&quot;int64&quot;}).set_index(&quot;D&quot;)</code></pre></details></li></ul><ul id="2a709a6c-ec54-41db-a0f9-f1455e30ceef" class="toggle"><li><details open=""><summary>write colab file to csv</summary><pre id="8a15ad26-a990-49b2-8334-d458598ff111" class="code code-wrap"><code>df.to_csv(r&#x27;Path where you want to store the exported CSV file\File Name.csv&#x27;, index = False)</code></pre></details></li></ul><ul id="0c52ff10-4d77-4f8f-ab51-28b7b9c9ca86" class="toggle"><li><details open=""><summary>copy to clipboard</summary><pre id="19d10939-5890-413f-9f85-29ab800eca3f" class="code code-wrap"><code># Copy data to clipboard; like an excel copy and paste
df = pd.read_clipboard()</code></pre></details></li></ul><ul id="7b573f63-4194-4e56-9660-86ab7d53476f" class="toggle"><li><details open=""><summary>read table from website</summary><pre id="097ca889-d3dd-4e3e-ab9a-1236c505e749" class="code"><code>df = pd.read_html(url, match=&quot;table_name&quot;)</code></pre></details></li></ul><ul id="4764e00f-a70e-451b-a1bf-6eae53ec1b89" class="toggle"><li><details open=""><summary>read pdf into dataframe</summary><pre id="881d7b33-488d-4420-a5df-cbc01a9641db" class="code"><code>!pip install tabula
from tabula import read_pdf
df = read_pdf(&#x27;test.pdf&#x27;, pages=&#x27;all&#x27;)

df_out.head()</code></pre></details></li></ul><ul id="acb88d00-c160-4f8d-a35c-a35ee11b71f8" class="toggle"><li><details open=""><summary>read in multiple files</summary><pre id="cc01757e-c13f-4a76-8831-c695b8582baa" class="code"><code>import os
os.makedirs(&quot;folder&quot;,exist_ok=True,); df_test.to_csv(&quot;folder/first.csv&quot;,index=False) ; df_test.to_csv(&quot;folder/last.csv&quot;,index=False)

import glob
files = glob.glob(&#x27;folder/*.csv&#x27;)
dfs = [pd.read_csv(fp) for fp in files]
df_out = pd.concat(dfs)</code></pre></details></li></ul><ul id="10a289b4-51b5-4e86-8372-4aa2325ebe61" class="toggle"><li><details open=""><summary>read in a csv files with dates as first col</summary><pre id="3bd3aa95-b16e-494f-9df4-6cab5be0917c" class="code"><code>df = pd.read_csv(file_filepath, index_col=&quot;Date&quot;, parse_dates=True)</code></pre></details></li></ul><ul id="2b4a3408-9497-4cce-926f-a21c649e4bf9" class="toggle"><li><details open=""><summary>upload a file into google colab</summary><pre id="7538ba80-c929-4a96-93a0-3c00202c08e9" class="code"><code>from google.colab import files

uploaded = files.upload()

for fn in uploaded.keys():
  print(&#x27;User uploaded file &quot;{name}&quot; with length {length} bytes&#x27;.format(
      name=fn, length=len(uploaded[fn])))</code></pre></details></li></ul><p id="f647c0fa-b23d-4641-bf14-40b6b8d6e222" class="">
</p><ul id="17935b92-e9b7-41b7-91fc-54f8b842cf11" class="toggle"><li><details open=""><summary>create categories (<strong>has df recipe</strong>)</summary><pre id="ed2717ae-f08b-4b21-ba1a-7ffc9e0291c3" class="code"><code>import pandas as pd
from pandas.api.types import CategoricalDtype

np.random.seed(1)
# quick way to create a data frame for testing 
df_test = pd.DataFrame(np.random.randn(3, 4), columns=[&#x27;a&#x27;, &#x27;b&#x27;, &#x27;c&#x27;, &#x27;d&#x27;]) \
    .assign(target=lambda x: (x[&#x27;b&#x27;]+x[&#x27;a&#x27;]/x[&#x27;d&#x27;])*x[&#x27;c&#x27;])

print(&quot;Let&#x27;s create our own categorical order.&quot;)
cat_type = CategoricalDtype([&quot;bad&quot;, &quot;good&quot;, &quot;excellent&quot;], ordered = True)
df[&quot;cats&quot;] = df[&quot;cats&quot;].astype(cat_type)

print(&quot;Now we can use logical sorting.&quot;)
df = df.sort_values(&quot;cats&quot;, ascending = True)

print(&quot;We can also filter this as if they are numbers.&quot;)
df[df[&quot;cats&quot;] &gt; &quot;bad&quot;]</code></pre></details></li></ul><ul id="70561f9a-6672-4d91-a2f9-7b7b4377594f" class="toggle"><li><details open=""><summary>multiple column assignments</summary><pre id="57245d25-3c44-4190-a254-212cfad993a7" class="code"><code>df_out = (df.assign(stringed = df[&quot;a&quot;].astype(str),
            ounces = df[&quot;b&quot;]*12,#                                     this will allow yo set a title
            galons = lambda df: df[&quot;a&quot;]/128)
           .query(&quot;b &gt; -1&quot;)
           .style.set_caption(&quot;Average consumption&quot;)) ; df_out</code></pre></details></li></ul><ul id="92893ba5-16c7-403e-9eee-8b816a4fb95c" class="toggle"><li><details open=""><summary>chaining with line continuation (but parens are better)</summary><pre id="d5d6e2b5-ee22-4abf-b3a2-1c67afdf59d2" class="code"><code># with line continuation character
df_out = df.dropna(subset=[&quot;b&quot;,&quot;c&quot;],how=&quot;all&quot;) \
.loc[df[&quot;a&quot;]&gt;0] \
.round(2) \
.groupby([&quot;target&quot;,&quot;b&quot;]).max() \
.unstack() \
.fillna(0) \
.rolling(1).sum() \
.reset_index() \
.stack() \
.ffill().bfill() 

df_out</code></pre></details></li></ul><ul id="a2295e85-a967-41de-9859-162c8af9ae53" class="toggle"><li><details open=""><summary>unnest or explode a column</summary><pre id="0e142a45-dbee-48fa-8946-9439fe4b85be" class="code"><code># Create it
df = df_test.head()
df[&quot;g&quot;] = [[str(a)+lista for a in range(4)] for lista in [&quot;a&quot;,&quot;b&quot;,&quot;c&quot;]]; df

# explode it
df_out = df.explode(&quot;g&quot;); df_out.iloc[:5,:]</code></pre></details></li></ul><ul id="5d10bb13-3195-4af6-8bfb-f38e0f0e0e04" class="toggle"><li><details open=""><summary>find duplicate records</summary><pre id="c4ac9a30-b748-41b9-970b-a6d4572172f1" class="code"><code>df_out = df[df.duplicated([&#x27;a&#x27;, &#x27;b&#x27;], keep=False)] ; df_out</code></pre></details></li></ul><ul id="bd5947c9-ad0c-45ae-88c8-a13df55376f6" class="toggle"><li><details open=""><summary>set df column values based on other column values</summary><pre id="afedf66d-d792-45d5-bb04-3d7869e69486" class="code"><code>df.loc[(df[&#x27;a&#x27;] &gt;1 ) &amp; (df[&#x27;c&#x27;] &lt;0), [&#x27;target&#x27;]] = np.nan ;df</code></pre></details></li></ul><ul id="9875c287-7bcd-4d6b-81e5-c039417a7617" class="toggle"><li><details open=""><summary>function to detect outliers</summary><pre id="d9ecb5d2-caae-4f53-9b60-103efe01c9a3" class="code"><code>def outlier_detect(data,col,threshold=3,method=&quot;IQR&quot;):
  
    if method == &quot;IQR&quot;:
      IQR = data[col].quantile(0.75) - data[col].quantile(0.25)
      Lower_fence = data[col].quantile(0.25) - (IQR * threshold)
      Upper_fence = data[col].quantile(0.75) + (IQR * threshold)
    if method == &quot;STD&quot;:
      Upper_fence = data[col].mean() + threshold * data[col].std()
      Lower_fence = data[col].mean() - threshold * data[col].std()   
    if method == &quot;OWN&quot;:
      Upper_fence = data[col].mean() + threshold * data[col].std()
      Lower_fence = data[col].mean() - threshold * data[col].std() 
    if method ==&quot;MAD&quot;:
      median = data[col].median()
      median_absolute_deviation = np.median([np.abs(y - median) for y in data[col]])
      modified_z_scores = pd.Series([0.6745 * (y - median) / median_absolute_deviation for y in data[col]])
      outlier_index = np.abs(modified_z_scores) &gt; threshold
      print(&#x27;Num of outlier detected:&#x27;,outlier_index.value_counts()[1])
      print(&#x27;Proportion of outlier detected&#x27;,outlier_index.value_counts()[1]/len(outlier_index))
      return outlier_index, (median_absolute_deviation, median_absolute_deviation)


    para = (Upper_fence, Lower_fence)
    tmp = pd.concat([data[col]&gt;Upper_fence,data[col]&lt;Lower_fence],axis=1)
    outlier_index = tmp.any(axis=1)
    print(&#x27;Num of outlier detected:&#x27;,outlier_index.value_counts()[1])
    print(&#x27;Proportion of outlier detected&#x27;,outlier_index.value_counts()[1]/len(outlier_index))
    
    return outlier_index, para
    

index,para = pv.outlier_detect(df,&quot;a&quot;,threshold=0.5,method=&quot;IQR&quot;)
print(&#x27;Upper bound:&#x27;,para[0],&#x27;\nLower bound:&#x27;,para[1])</code></pre></details></li></ul><ul id="a1930046-e691-40cd-9139-b49ad084bdd5" class="toggle"><li><details open=""><summary>split rows</summary><pre id="96b549c4-d031-4e0a-b1f9-30ebac7fd4cc" class="code code-wrap"><code>s = pd.Series([&quot;this is a regular sentence&quot;, &quot;https://docs.p.org&quot;, np.nan])
s.str.split()</code></pre></details></li></ul><ul id="4b4e29b7-b4d7-4d52-9a01-e0e27fd4e0b3" class="toggle"><li><details open=""><summary>creates new columns with the different split values (instead of lists)</summary><pre id="741261a6-71b7-4ce1-a33e-d07f042833fb" class="code"><code>s.str.split(expand=True)</code></pre></details></li></ul><ul id="bb6fb74b-0aa7-4ad1-aa63-210034f38f23" class="toggle"><li><details open=""><summary>remove all the characters after &amp;# (including &amp;#) for column - col_1</summary><pre id="8e58f7fc-56e3-4aca-900d-43db28dcef93" class="code code-wrap"><code>df[col_name].replace(&#x27; &amp;#.*&#x27;, &#x27;&#x27;, regex=True, inplace=True)</code></pre></details></li></ul><ul id="69e1b7fd-b54b-4519-a307-70526c55aca7" class="toggle"><li><details open=""><summary>tidy data (long format)</summary><ol type="1" id="a36b199f-67be-4f21-8928-32abab42c811" class="numbered-list" start="1"><li>each variable forms a column</li></ol><ol type="1" id="4f88e07d-6153-493d-a9ac-bb0798a8152c" class="numbered-list" start="2"><li>each observation forms a row</li></ol><ol type="1" id="dcdfc6cb-6dff-48da-9610-d6143ca7c641" class="numbered-list" start="3"><li>each type of observational unit forms a table</li></ol><figure id="5a473677-8b0b-477d-882b-9a599686d063"><a href="https://pandas.pydata.org/pandas-docs/stable/user_guide/reshaping.html" class="bookmark source"><div class="bookmark-info"><div class="bookmark-text"><div class="bookmark-title">Reshaping and pivot tables - pandas 1.3.0 documentation</div><div class="bookmark-description">Data is often stored in so-called &quot;stacked&quot; or &quot;record&quot; format: For the curious here is how the above was created: To select out everything for variable we could do: But suppose we wish to do time series operations with the variables. A better representation would be where the are the unique variables and an of dates identifies individual observations.</div></div><div class="bookmark-href"><img src="https://pandas.pydata.org/pandas-docs/stable/_static/favicon.ico" class="icon bookmark-icon"/>https://pandas.pydata.org/pandas-docs/stable/user_guide/reshaping.html</div></div><img src="https://pandas.pydata.org/pandas-docs/stable/_images/reshaping_pivot.png" class="bookmark-image"/></a></figure></details></li></ul><ul id="e67ce497-aabc-41fa-8568-dc7caab73612" class="toggle"><li><details open=""><summary>drop a row if nas in one col</summary><pre id="8538a1a7-f30b-4870-9d66-ee76c2310601" class="code"><code># col_list is a list of column names to consider for nan values.
df.dropna(subset=[col_list])  </code></pre></details></li></ul><h3 id="10ef0bad-0bc9-43c4-842a-b1dae06baf84" class="">Dates</h3><ul id="7f3f963f-1c35-4f61-93ec-ef97e8a30a7b" class="toggle"><li><details open=""><summary>read csv with dates as date format</summary><pre id="38b26a4b-c465-40de-9f1f-1088d7093ffe" class="code code-wrap"><code>df.pd.read_csv(&#x27;data/data2.csv&#x27;, parse_dates = [&quot;Date&quot;])</code></pre></details></li></ul><ul id="47927f92-97bf-4f59-b4be-15f3855f8121" class="toggle"><li><details open=""><summary>get year and month from date</summary><pre id="ba3a42e9-17b8-4efd-a9c0-8d97a22dacef" class="code"><code>estate[&#x27;Month&#x27;] = estate[&#x27;Date&#x27;].dt.strftime(&#x27;%b&#x27;)
estate[&#x27;Year&#x27;] = estate[&#x27;Date&#x27;].dt.strftime(&#x27;%Y&#x27;)</code></pre></details></li></ul><ul id="3801d569-af67-403e-8df3-486537efa2e4" class="toggle"><li><details open=""><summary>convert a date [YYYY-MM_DD] from string to datetime object, with some blank or nan cells</summary><pre id="ea38fdb8-a91d-416c-a59c-d0fbf6a78539" class="code code-wrap"><code>lemurs[&#x27;conv_dob&#x27;] = pd.to_datetime(lemurs[&#x27;estimated_dob&#x27;], errors=&#x27;coerce&#x27;).dt.date</code></pre></details></li></ul><p id="c846f9fd-3a91-401a-a1f9-6ab9b4717472" class="">
</p><ul id="45aeb896-28b4-4707-84b6-f3ca2c011f41" class="toggle"><li><details open=""><summary>what does the <strong>transform</strong> do</summary><pre id="6d1afcbb-0222-4e5f-8c7f-6564873b7a6a" class="code code-wrap"><code># Python’s Transform function returns a self-produced dataframe with transformed values after applying the function specified in its parameter. This dataframe has the same length as the passed dataframe.

#[Link for full explanation](https://www.analyticsvidhya.com/blog/2020/03/understanding-transform-function-python/)

#creating a dataframe
df=pd.DataFrame(np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]]), columns=[&#x27;a&#x27;, &#x27;b&#x27;, &#x27;c&#x27;])
#applying the transform function
df.transform(func = lambda x : x * 10)

# Transform comes in handy during feature extraction. As the name suggests, we extract new features from existing ones. Let’s understand the importance of the transform function with the help of an example.

data = pd.DataFrame({
&#x27;C&#x27; : [random.choice((&#x27;a&#x27;,&#x27;b&#x27;,&#x27;c&#x27;)) for i in range(1000000)],
&#x27;A&#x27; : [random.randint(1,10) for i in range(1000000)],
&#x27;B&#x27; : [random.randint(1,10) for i in range(1000000)]
})

data[&#x27;N3&#x27;] = data.groupby([&#x27;C&#x27;])[&#x27;A&#x27;].transform(&#x27;mean&#x27;)

# The above does the same as below, but quicker
data.groupby(&#x27;C&#x27;)[&quot;A&quot;].mean()
mean =data.groupby(&#x27;C&#x27;)[&quot;A&quot;].mean().rename(&quot;N&quot;).reset_index()
df_1 = data.merge(mean)</code></pre></details></li></ul><ul id="d8f8e4d7-cb27-4458-b623-6986cb962332" class="toggle"><li><details open=""><summary>apply decimal point precision</summary><pre id="3ecf3293-b628-4d20-819f-4472447f1563" class="code code-wrap"><code># Generally apply 3 decimal point precision
pd.options.display.float_format = &quot;{:.3f}&quot;.format</code></pre></details></li></ul><ul id="1aff69ba-8b4d-4147-a692-11639a614d63" class="toggle"><li><details open=""><summary>make a user-defined function</summary><pre id="644ee386-5cc8-409d-b572-b7e6f427afc2" class="code code-wrap"><code>def myfunc(x,y):
	return x + y</code></pre></details></li></ul><ul id="022603c9-1253-44aa-8884-451b73ad398f" class="toggle"><li><details open=""><summary><strong>append</strong> one identical (header-wise) dataframe to another</summary><pre id="5c8a178c-5da5-4e77-b904-7858f54336f5" class="code code-wrap"><code>import pandas as pd

df_1 = pd.DataFrame(
	[[&#x27;Somu&#x27;, 68, 84, 78, 96],
	[&#x27;Kiku&#x27;, 74, 56, 88, 85],
	[&#x27;Ajit&#x27;, 77, 73, 82, 87]],
	columns=[&#x27;name&#x27;, &#x27;physics&#x27;, &#x27;chemistry&#x27;,&#x27;algebra&#x27;,&#x27;calculus&#x27;])

df_2 = pd.DataFrame(
	[[&#x27;Amol&#x27;, 72, 67, 91, 83],
	[&#x27;Lini&#x27;, 78, 69, 87, 92]],
	columns=[&#x27;name&#x27;, &#x27;physics&#x27;, &#x27;chemistry&#x27;,&#x27;algebra&#x27;,&#x27;calculus&#x27;])

frames = [df_1, df_2]

#append dataframes
df = df_1.append(df_2, ignore_index=True)

#print dataframe
print(&quot;df_1\n------\n&quot;,df_1)
print(&quot;\ndf_2\n------\n&quot;,df_2)
print(&quot;\ndf\n--------\n&quot;,df)</code></pre><p id="abb9db0d-dc65-4189-a760-cd19e1a5a4fe" class="">
</p><p id="98799499-508c-4c49-90aa-3789c4704a0c" class="">
</p></details></li></ul><ul id="98482500-2360-4115-9f9b-4a485ed7ad8e" class="toggle"><li><details open=""><summary>change the order of columns</summary><pre id="ff9364c6-8ced-43bc-b928-e510e50c974b" class="code code-wrap"><code>df[[&#x27;date&#x27;, &#x27;amount&#x27;, &#x27;payee&#x27;]]</code></pre></details></li></ul><ul id="96d95e27-265b-4218-8c8c-21fff3c24a1d" class="toggle"><li><details open=""><summary>google colab visualize df as a <strong>datatable</strong></summary><pre id="ff3070c1-51d3-4015-a4c0-8e9bf02b7606" class="code code-wrap"><code>%load_ext google.colab.data_table
df
%unload_ext google.colab.data_table</code></pre></details></li></ul><ul id="8477d6a7-a532-4354-ba78-c604e6149d49" class="toggle"><li><details open=""><summary>round the result</summary><pre id="db7f48ca-481c-423e-82a0-f32e92175c1a" class="code code-wrap"><code>round(lemurs[&#x27;age_at_death_y&#x27;].mean(), ndigits=2)</code></pre></details></li></ul><ul id="fd1b5dfb-46a4-4b19-b178-27e6a3471ffa" class="toggle"><li><details open=""><summary>find all items in one series that are not in another</summary><pre id="0498736c-cc46-424a-9bc7-a2e13f0da355" class="code code-wrap"><code># Input
ser1 = pd.Series([1, 2, 3, 4, 5])
ser2 = pd.Series([4, 5, 6, 7, 8])

# Solution
ser1[~ser1.isin(ser2)]</code></pre></details></li></ul><h2 id="796f3b5b-e058-464b-83df-706c667c5263" class=""><details open=""><summary>Cheatsheets</summary></details></h2><div class="indented"><figure id="66aa8118-39ae-446e-a8e5-9e96498ea340"><div class="source"><a href="Pandas%20c1f07c8dbc5f470faab6c9bd0a6aded8/PandasPythonForDataScience.pdf">https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1c695dbe-6cce-4d8b-95a2-f9550246e9ca/PandasPythonForDataScience.pdf</a></div></figure><figure id="b0ff917f-0229-4f60-aa7e-ccfd506c67c4"><div class="source"><a href="Pandas%20c1f07c8dbc5f470faab6c9bd0a6aded8/Python_Seaborn_Cheat_Sheet.pdf">https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cdacfb32-f5f2-4874-bce6-30bc3fdf0208/Python_Seaborn_Cheat_Sheet.pdf</a></div></figure><figure id="5c10b0c4-b96b-44f7-8afd-d6c035f75d8b"><div class="source"><a href="Pandas%20c1f07c8dbc5f470faab6c9bd0a6aded8/plotly_python_cheat_sheet.pdf">https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6eb467a8-a271-41cd-9586-ae3f891f8f7e/plotly_python_cheat_sheet.pdf</a></div></figure><figure id="1f1d305f-a537-43fc-a636-916e2306c264"><div class="source"><a href="Pandas%20c1f07c8dbc5f470faab6c9bd0a6aded8/Pandas_Cheat_Sheet.pdf">https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fad6ece6-25de-4196-805e-161077fe356a/Pandas_Cheat_Sheet.pdf</a></div></figure></div><p id="784e5afd-1ac9-46d9-82bb-49d88796fbd4" class="">selective replace with dict</p><pre id="5e6a2112-f2b0-4e23-a8a9-414b808f0c1e" class="code code-wrap"><code>import pandas as pd
import numpy as np


data = {&#x27;Merchant&#x27;:[&#x27;henhouse&#x27;, &#x27;hair joint&#x27;, &#x27;starbucks&#x27;, &#x27;amc&#x27;], &#x27;Category&#x27;:[&#x27;grocery&#x27;, &#x27;dog&#x27;, &quot;coffeeshop&quot;, &quot;dog&quot;]}
df = pd.DataFrame(data)
mydict =  {&quot;hair joint&quot;: &quot;personal&quot;, &#x27;amc&#x27;: &quot;entertainment&quot;}
df

for key, value in mydict.items():
    for x in range(4):
        if key in df[&#x27;Merchant&#x27;][x]:
            df[&#x27;Category&#x27;][x]=value
            print (value)</code></pre><div id="26b387f7-9f8a-4f0a-bde9-d89a3eacf678" class="column-list"><div id="7529139a-e530-448f-adec-3dffc3d32ae1" style="width:50%" class="column"></div><div id="9a33e71e-c6d7-4630-9eb8-b0de241ab2be" style="width:50%" class="column"></div></div><div id="d3153c18-321f-46f4-9e28-9e6003fe2849" class="column-list"><div id="eaa861f4-23f3-44c1-bf70-f56f29febdf3" style="width:50%" class="column"></div><div id="b7466469-2532-456f-a257-ccc4f24587cb" style="width:50%" class="column"></div></div><div id="1e946875-55b7-440a-b5b2-7064a7e179de" class="column-list"><div id="0960ed1c-b616-4314-9145-5f3c642b9f66" style="width:50%" class="column"></div><div id="ca5fc411-d3c2-4912-91ba-acdf21403c48" style="width:50%" class="column"></div></div><div id="0361dd97-27bb-45f3-88cd-41d8a90e94db" class="column-list"><div id="c218c493-7794-4917-a398-b9ad9a900bea" style="width:50%" class="column"></div><div id="42b16025-7632-4281-b781-9c777f1aa47d" style="width:50%" class="column"></div></div><p id="cc2ccfb8-cafe-488a-bcc5-13468b6d7561" class="">
</p></div></article></body></html>
