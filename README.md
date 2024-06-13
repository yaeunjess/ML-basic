# ML-basic

<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>CIFAR-100 Classification</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	padding-inline-start: 0;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

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

.page-description {
    margin-bottom: 2em;
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

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI Variable Display", "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI Variable Display", "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI Variable Display", "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI Variable Display", "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI Variable Display", "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
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
.select-value-color-uiBlue { background-color: rgba(35, 131, 226, .07); }
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-transparentGray { background-color: rgba(227, 226, 224, 0); }
.select-value-color-translucentGray { background-color: rgba(255, 255, 255, 0.0375); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }
.select-value-color-pageGlass { background-color: undefined; }
.select-value-color-washGlass { background-color: undefined; }

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
	
</style></head><body><article id="d3382ef4-b9e0-4ad6-83da-b70348718c90" class="page sans"><header><div class="page-header-icon undefined"><span class="icon">2️⃣</span></div><h1 class="page-title">CIFAR-100 Classification</h1><p class="page-description"></p></header><div class="page-body"><ul id="36cdaa2a-358c-4f02-bd2b-f05964e6adbb" class="toggle"><li><details open=""><summary>발표 흐름</summary><ol type="1" id="c6c7eb8a-263c-42af-8bd8-324c86485a2a" class="numbered-list" start="1"><li>모델 : EfficientNet</li></ol><ol type="1" id="2e9dc78f-c4ed-44b4-b4e4-b4151f43349a" class="numbered-list" start="2"><li>기법<ul id="cf75aa45-41cd-42cd-b0c8-6f5ca4ad90c8" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-default"><del><strong>stochastic depth</strong></del></mark><mark class="highlight-default"><strong> </strong></mark><mark class="highlight-default">: 성능 미미함</mark></li></ul><ul id="be76c8fa-0c57-4f10-bfb0-28122565da46" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-default"><del><strong>앙상블 - 보팅</strong></del></mark><mark class="highlight-default"><strong> : </strong></mark><mark class="highlight-default">과적합일어난 거를 앙상블 하면 더 좋든지 </mark></li></ul><ul id="557a8b06-fe44-4684-95f6-a98f24bc63b2" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-default"><del><strong>progressive learning</strong></del></mark><mark class="highlight-default"> : 실험 힘듦 오래걸림, 실제 논문에서 발표된 학습시간은 350 에포크 가량으로 이번 과제에 적용하기에는 학습 시간 및 총 5회 학습 진행해야된다는 점 감안하여 부적절하다고 판단. 테스트를 진행했을 때는 학습시간을 적게 하여 진행하려 했으나 정확도가 안 나온다.</mark></li></ul><ul id="e4a01f6c-1116-4251-b242-7846a0f21d65" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-default"><strong>scheduler-stepLR()</strong></mark><mark class="highlight-default"> : 성능 좋음, 값이 빠르게 수렴하는걸 도와줌</mark></li></ul><ul id="a78d768d-eab8-48ca-a048-617ddb8fef27" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-default"><strong>데이터 증강</strong></mark><ul id="1878bca2-e304-4de0-b254-c2025edda8b0" class="bulleted-list"><li style="list-style-type:circle"><mark class="highlight-default"><strong>crop</strong></mark></li></ul><ul id="71934c4c-ab6f-489c-9de8-d263c6a34967" class="bulleted-list"><li style="list-style-type:circle"><mark class="highlight-default"><strong>flip</strong></mark></li></ul><ul id="35be27af-c90e-4c2f-957e-8c1391443539" class="bulleted-list"><li style="list-style-type:circle"><mark class="highlight-default"><strong>rotation</strong></mark></li></ul><ul id="889c8d19-262c-4c94-9530-f6eaa7d6670e" class="bulleted-list"><li style="list-style-type:circle"><mark class="highlight-default"><strong>cutmix-0.5</strong></mark></li></ul><ul id="36421b1b-0912-4c8d-83a6-1d6b703694dd" class="bulleted-list"><li style="list-style-type:circle"><mark class="highlight-default"><del><strong>선형 보간법</strong></del></mark></li></ul><ul id="e24ae1a4-6280-42c7-9d40-660085dbd26c" class="bulleted-list"><li style="list-style-type:circle"><del><mark class="highlight-default"><strong>colorjitter</strong></mark></del><mark class="highlight-default"><strong> : </strong></mark><mark class="highlight-default">고유의 색이 물체의 중요한 특징일 경우 성능이 더 안 좋아질 수 있음</mark></li></ul></li></ul><ul id="90943111-6ab3-4c52-8c9e-810ea2b304ef" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-default"><strong>적절한 Hyperparameter </strong></mark><ul id="e0a96872-67c6-4c79-b34b-23c28eab9a81" class="bulleted-list"><li style="list-style-type:circle"><mark class="highlight-default">learning rate 크게 했더니 성능 감소 확인</mark></li></ul><ul id="4fd9dbc3-8270-4a1c-95f9-6c80b025ecda" class="bulleted-list"><li style="list-style-type:circle">batch size : 32, 64는 성능 차이 컸음, m모델 64 &lt; s모델 128</li></ul><ul id="8ce6e5a9-6d49-4bda-b372-9aa7d9854f58" class="bulleted-list"><li style="list-style-type:circle">weight_decay : overfitting 방지로 넣었음</li></ul><ul id="6c69094e-6b8f-43fd-9f65-e2d93f41cd39" class="bulleted-list"><li style="list-style-type:circle">seed로 nparray 랜덤으로 뽑기</li></ul><div id="102f7af7-0d83-4345-ab6e-15d52d41ee1c" class="column-list"><div id="a2a2ce9e-ac38-457b-829f-3979040a58f2" style="width:50%" class="column"><figure id="dec4aca1-62a1-4bac-9f34-dcfbaf9b5a04" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled.png"><img style="width:240px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled.png"/></a></figure></div><div id="3818b11a-26a8-443c-a85c-5cdfd8c52141" style="width:50%" class="column"><figure id="d16f5650-4db8-47e0-8ce8-94c2384b772e" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%201.png"><img style="width:240px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%201.png"/></a></figure></div></div></li></ul></li></ol><ol type="1" id="93d30ad1-594e-41f1-a355-63cbf9958a61" class="numbered-list" start="3"><li>성능</li></ol></details></li></ul><hr id="145fbdd8-7552-41f9-b3da-94b4280539e6"/><h2 id="a677c1d0-f85a-44b0-9f02-3ffa385a1812" class="">1. 모델</h2><h3 id="408d0428-db72-4868-8286-403263ddb0a2" class="block-color-blue_background"><del><mark class="highlight-default"><strong>Ensemble - Bagging</strong></mark></del></h3><p id="0f9eac82-4042-4638-9557-417b9eff00ce" class="">단일 알고리즘 기반의 모델을 다른 데이터를 기반으로 학습시켜 모델의 결과를 결합한다.</p><figure id="4e3617fd-fe0f-4b86-9eb2-73c3fa3ba2d8" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%202.png"><img style="width:384px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%202.png"/></a></figure><p id="c54729f2-3e57-44cf-96f7-50b4bf0a0fba" class="">여러개의 CNN구조  만들고 augment만 다르게 하여서 학습 후 합쳐서 결과 도출</p><figure id="7f0f3b19-552e-40c8-bbc4-a800f81bb492" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%203.png"><img style="width:624px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%203.png"/></a></figure><h3 id="395dbe4c-777c-4d32-af39-574541397116" class="block-color-blue_background">EfficientNetV2</h3><p id="d1bac9de-c3e6-4717-858e-e9db74bf0136" class=""><mark class="highlight-blue"><em><strong>모델 선정 이유</strong></em></mark></p><ul id="62fb95cc-60eb-4078-a4fb-6c78ac803855" class="bulleted-list"><li style="list-style-type:disc">기존 EfficientNet을 개선한 EfficientNetV2로 선정 </li></ul><ul id="7c0d4b02-e437-440d-985f-438847157489" class="bulleted-list"><li style="list-style-type:disc">파라미터 수가 비교적 적고 학습 속도 개선 데이터 확인하여 모델 선정.</li></ul><ul id="90ae3c3e-85a7-4a60-b87b-d6eac767be08" class="bulleted-list"><li style="list-style-type:disc">이때 EfficientNetV2는 기존 EfficientNet의 MBConv를 개선하여 fused MBConv를 1~3 stage에서 사용</li></ul><figure id="33a58b2b-07e7-4430-b237-1aa4c93360f4" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%204.png"><img style="width:384px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%204.png"/></a></figure><ul id="5d95c609-bd5c-4be4-9679-51920d411101" class="bulleted-list"><li style="list-style-type:disc">또한 기존 EfficientNet의 compound scailing으로 모든 스테이지를 동일하게 scailing up 하였지만</li></ul><ul id="f098328f-60ce-49a8-a451-a2d6ea028b50" class="bulleted-list"><li style="list-style-type:disc">이를 개선하고자 non-uniform scaling strategy를 사용하여 stage가 증가할 수록 layer가 증가하는 정도를 높인 방법을 제안함.</li></ul><p id="efc1c423-2b27-4074-a8fe-6029b1a5caf0" class=""><mark class="highlight-blue"><em><strong>모델 적용</strong></em></mark></p><ul id="0b55de44-f5e2-4483-938b-8dd9aa355bde" class="bulleted-list"><li style="list-style-type:disc">여러 자료를 통해 정확도가 더 높으며 training 시간이 적다는 것을 참고하여 테스트 모델로 사용하게 됨.</li></ul><ul id="01a238a7-f04f-4978-ae3b-32b755ee4443" class="bulleted-list"><li style="list-style-type:disc">모델은 s,m,l 사이즈 모두 테스트 진행했음.</li></ul><ul id="fa9b2426-855b-43b3-82c6-1fc22bc870e5" class="bulleted-list"><li style="list-style-type:disc">imagenet1k에 대해 pretrain된 모델 이용하여 학습 진행했음.</li></ul><hr id="a04c0a33-e222-4567-94ce-5f271587153e"/><h2 id="dc96ea9c-a1bd-48dd-b40b-38bae0ee746e" class="">2. 기법</h2><h3 id="c333eb90-4fb6-4016-b6c1-3cc18d21b717" class="block-color-blue_background">적절한 Hyperparameter가 성능에 제일 중요했다!</h3><ul id="f9fd4cff-1cf9-488b-a69f-7c8617f7eaab" class="bulleted-list"><li style="list-style-type:disc">loss function : <code>CrossEntropyLoss()</code></li></ul><ul id="30a76cde-a781-49f4-84ca-45306b2743ca" class="bulleted-list"><li style="list-style-type:disc">optimizer : <code>AdamW()</code>,  Adam 옵티마이저의 변형으로 weight decay를 적용하는 것이 특징임. </li></ul><ul id="8d95426e-61da-462c-aeb7-6b9d0c6416e6" class="bulleted-list"><li style="list-style-type:disc">n_epochs = <code>25</code></li></ul><ul id="2c82db08-35e2-4570-a70c-e641e0a6fbe9" class="bulleted-list"><li style="list-style-type:disc">batch_size = <code>128</code> </li></ul><ul id="243ec438-d31e-4b9c-b689-e2eb199895e7" class="bulleted-list"><li style="list-style-type:disc">scheduler : <code>StepLR()</code> , step size마다 gamma 비율로 lr을 감소시킴.</li></ul><ul id="e07ed212-c230-42a4-ac0f-3d0e07d1f795" class="bulleted-list"><li style="list-style-type:disc">learning_rate : 초기 <code>0.0004</code> 에서 epoch <code>10</code> 간격으로 gamma, <code>0.9</code>가 곱해짐</li></ul><div id="b7f54edc-5a9b-40e2-b72a-6044b37a50af" class="column-list"><div id="ce75b8d6-fac6-4fb2-94a6-06be3d4c6e64" style="width:50%" class="column"><figure id="44004ad2-253f-4416-a340-ff8c6416d930" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled.png"><img style="width:240px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled.png"/></a></figure></div><div id="588832d7-e54d-4bbc-829f-a39430184c66" style="width:50%" class="column"><figure id="c5fc8c13-ad82-4178-9f1b-c5e4041933a8" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%201.png"><img style="width:240px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%201.png"/></a></figure></div></div><ul id="f8327326-9af9-4fb7-87a5-9ce56d23ccb2" class="bulleted-list"><li style="list-style-type:disc">weight_decay : <code>0.001</code>, overfitting 방지로 넣었음.</li></ul><script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="769260f2-8b75-46e4-b68f-f5fa513ef11d" class="code"><code class="language-Python">criterion = nn.CrossEntropyLoss()
optimizer = optim.AdamW(model_to_train.parameters(), lr=0.0004, weight_decay= 0.001)
scheduler = StepLR(optimizer, step_size=10, gamma=0.9)</code></pre><p id="241701c1-e276-483d-bc68-9455ef0708cc" class="">
</p><h3 id="df091ee5-3098-4c48-8d53-b806a3c0f1e4" class="block-color-blue_background"><mark class="highlight-default"><strong>데이터 증강</strong></mark></h3><ol type="1" id="4ec3df62-f001-4d36-bc6f-272251bd56da" class="numbered-list" start="1"><li><strong><del>선형 보간법, Bilinear Interpolation</del></strong><br/><br/><del><code>transforms.Resize((224, 224), interpolation=Image.BILINEAR)</code></del><p id="daac8896-bcb9-4e44-a683-833706b20aa2" class=""> 보간법이란 화소 값을 할당 받지 못한 영상(예 영상의 빈 공간)의 품질은 안 좋을 수밖에 없는데, 이때 빈 화소에 값을 할당하여 좋은 품질의 영상을 만드는 방법을 의미합니다.</p><p id="1ff56c08-59cb-4e88-9ef5-858c38ca4506" class=""> 선형 보간법은 두 축에 대해 선형 보간을 수행합니다. 주변 4개의 픽셀을 사용하여 가중 평균을 계산하여 값을 결정합니다. 확대 및 축소 모두에 사용할 수 있으며, Nearest Neighbor에 비해 부드러운 이미지를 생성합니다.</p><div id="6ed6966c-2246-4e1f-8e1f-eb130c6f9f76" class="column-list"><div id="ba3b0e3e-29d2-4df9-b28d-785a2a8a78c1" style="width:50%" class="column"><figure id="c1c77783-74fc-4628-99b8-677abad05a6e" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%205.png"><img style="width:853px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%205.png"/></a><figcaption>선형 보간법 적용 전</figcaption></figure></div><div id="2321eb48-5c2e-401d-919d-9b6fcdee0c1a" style="width:50%" class="column"><figure id="1f491838-4dad-4dbe-a3aa-55a0ffaa3b07" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%206.png"><img style="width:827px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%206.png"/></a><figcaption>선형 보간법 적용 후</figcaption></figure></div></div><figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="2387466f-080e-4512-bba5-b6f5cbc919bd"><div style="font-size:1.5em"><span class="icon">💡</span></div><div style="width:100%">성능이 더 안좋았음.<br/>Bilinear Interpolation을 적용했을 때 기존 Default 값인 Nearest에 비해서 해상도가 더 좋아졌다고 판단하였음. 따라서 이를 적용하여 테스트를 진행하였지만 생각보다 성능 향상이 미미하며 효과가 없다고 판단하여 이를 배제.<br/></div></figure></li></ol><ol type="1" id="d5b21b3a-4fac-45b1-8e49-44b6a2a3d9ac" class="numbered-list" start="2"><li><del><code>ColorJitter()</code></del> : 이미지의 밝기, 채도 등등 컬러 관련 여러 속성들을 임의로 변경한다.<figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="24bc7b54-8c35-4bc5-a249-00b2ce5f0897"><div style="font-size:1.5em"><span class="icon">💡</span></div><div style="width:100%">성능이 더 안 좋았음. <br/>개체를 구분함에 있어서 색깔이 중요한 특징일 경우, 이를 적용하는 게 모델 성능에 더 좋지 않을 거라고 생각.<br/>그러나, 파라미터 수정을 잘 한다면 효과는 있을 것이지만 파라미터 수정을 정확히 하지 않은 경우 오히려 악영향을 끼칠 것.<br/>이유는 아래와 같이 다람쥐 같은 동물의 경우는 개체 인식에 색이 중요한 영향을 끼친 게 원인이라고 판단.<br/></div></figure><figure id="68549283-1d26-4929-b512-1336fa2c7d52" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%207.png"><img style="width:684px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%207.png"/></a></figure></li></ol><ol type="1" id="ff64abaf-c13d-4f96-b025-a1270506b732" class="numbered-list" start="3"><li><code>RandomRotation()</code> : 이미지를 랜덤하게 rotation 한다.<figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="20a1182f-be92-4a88-9318-bc37f812f677"><div style="font-size:1.5em"><span class="icon">💡</span></div><div style="width:100%">일반화 성능에 도움이 될 거라 예상하여 적용.적용 후 0.5% 가량 정확도 상승했으나 이는 오차 범위 이내로 효과가 올랐을 가능성이 있음.</div></figure><div id="f7ee355e-ffd5-4145-87e1-5246dd889dc5" class="column-list"><div id="ca54e44e-bc06-4c19-885c-ffc775f3181a" style="width:50%" class="column"><figure id="1671e004-5e59-4bb5-80e5-ec01dcc330d4" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%208.png"><img style="width:726px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%208.png"/></a></figure></div><div id="cfb2af4c-6b2d-49a0-a41d-6e33ec84db1b" style="width:50%" class="column"><figure id="79dd1242-dec3-4faa-a5af-b67e33511eca" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%209.png"><img style="width:104px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%209.png"/></a></figure></div></div></li></ol><ol type="1" id="6314b634-8125-4b5a-bbef-1529e713d43b" class="numbered-list" start="4"><li><code>RandomHorizontalFlip()</code> : 50프로 확률로 수평으로 뒤집는다. 즉 좌우반전이다. <figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="8bfe0207-fcc1-438e-93a3-3ae923edbed7"><div style="font-size:1.5em"><span class="icon">💡</span></div><div style="width:100%">개체를 구분함에 있어 위/아래의 정보가 중요한 특징일 경우, 모델 성능에 좋지 않을것라고 생각함.<br/>상하반전은 적용하지 않고, 좌우반전을 적용함.<br/></div></figure></li></ol><ol type="1" id="4e6b1cd3-71ca-414b-b472-2216cbd9ac5c" class="numbered-list" start="5"><li><code>RandomCrop()</code> : (width, height)의 잘라낼 크기를 설정하면, 그 크기만큼 랜덤으로 잘라낸다. <p id="8b20fb0e-caf8-44a3-b844-703953846e78" class="">padding_mode = reflect으로 설정하여 아래와 같이 데이터 증강했다. 노이즈 추가를 통해 모델을 일반화시키려 했다. </p><div id="722445f9-d659-40af-9660-9029f1c03fb5" class="column-list"><div id="9e27b634-e679-4d6e-8cd7-161be4f1b36c" style="width:50%" class="column"><figure id="d55cc71d-09f3-4291-a55d-766f1a5ad1fb" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2010.png"><img style="width:834px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2010.png"/></a></figure></div><div id="4ebd5f63-9279-4073-8ce6-4ec2af3fab16" style="width:50%" class="column"><figure id="2b90f9df-9abb-48d5-882d-907a1999079e" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2011.png"><img style="width:317px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2011.png"/></a></figure></div></div></li></ol><ol type="1" id="1ee88255-1d8f-4858-8209-16f3ac5cd6b4" class="numbered-list" start="6"><li><code>cutmix</code> : 하나의 이미지 안에 두개의 레이블을 가진 이미지를 적당한 비율로 배치하여, 두개의 레이블이 하나의 이미지에 비율에 맞게 배치되는 방식이다. (mixup과 cutout의 특징을 합친 방법)<p id="8018ad88-934a-4401-9dc2-fde56a42edf1" class="">아래 제일 오른쪽 이미지를 보면, 고양이 얼굴 : 강아지 몸 = 0.4 : 0.6 비율로 구성되어 있다.</p><figure id="681a7484-49a8-4482-8a1c-a4971b906383" class="image" style="text-align:center"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2012.png"><img style="width:576px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2012.png"/></a></figure><p id="7cc21f9a-d197-409d-bb5b-ec7818bfae31" class="">
</p><figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="651a319b-1024-4a66-b7bf-450e2ee8c1af"><div style="font-size:1.5em"><span class="icon">💡</span></div><div style="width:100%">적용 후 2% 가량 정확도 상승.</div></figure></li></ol><p id="06113b64-d7e3-4121-92b5-2589b4baa35c" class="">
</p><h3 id="60fbad46-ac0a-4a5f-a282-b04bc6329086" class="block-color-blue_background"><del><mark class="highlight-default"><strong>stochastic depth</strong></mark></del></h3><ul id="5fd34f66-83a8-4b88-a6f9-e21d2aa69464" class="bulleted-list"><li style="list-style-type:disc">layer의 개수를 overfitting 없이 늘리는 역할 가능 </li></ul><ul id="c0999eb0-5e28-45b1-bf81-9c4041f3a056" class="bulleted-list"><li style="list-style-type:disc">drop out과 유사</li></ul><ul id="b15ead4f-36e8-47d4-ba6b-c6f8081db6d8" class="bulleted-list"><li style="list-style-type:disc">기존의 drop out이 network의 weight에 집중했다면 stochastic depth는 network의 depth를 학습단계에서 random하게 줄이는 것</li></ul><p id="8eb17b8f-f703-40bc-977b-6da4b71c8767" class="">deep network의 vanishing gradient, diminishing feature 문제 해결</p><p id="a17867e4-a9b6-4c90-ac48-2598539140f8" class="">diminishing feature: multiplication과 convolution 연산을 거치며 feature가 손실되는 것</p><figure id="275d3d9b-bf76-4828-9dc2-3e8dd695f396" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2013.png"><img style="width:737px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2013.png"/></a></figure><figure id="e92e1416-d6e5-462f-8015-a1228f38bed5" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2014.png"><img style="width:708px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2014.png"/></a></figure><p id="284ba208-2156-4f30-b5f5-33868444ec26" class="">
</p><p id="0f3e5689-4c9e-4bf5-a4cb-96613599f15b" class="">stochastic depth는CIFAR-10과 같이 비교적 작은 데이터셋에서 network를 복잡하게 만들었을 때 test 정확도의 향상을 기대할 수 있다. </p><p id="5de1ef82-190a-4d2b-87b3-153338c731ae" class="">결론 : 쉬운 데이터, deep network 사용시 효과적</p><figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="8fb540bd-0aef-4915-937e-ca995c2405f9"><div style="font-size:1.5em"><span class="icon">💡</span></div><div style="width:100%">성능 차이 미미함. 쉬운 데이터가 아니기 때문이라고 예측. </div></figure><p id="6ce4ff74-4a3d-4375-bc24-58d547358e6b" class="">
</p><h3 id="df44307e-d694-4d80-aee8-d96f4916caaf" class="block-color-blue_background"><del><mark class="highlight-default">Progressive learning with adaptive regularization</mark></del></h3><p id="38a42568-1906-46a3-b1da-40030a70a697" class="">🔗논문 설명 : <a href="https://rauleun.github.io/EfficientNetV2">https://rauleun.github.io/EfficientNetV2</a></p><ul id="f9b7a8fa-5ff0-4dd8-b3e5-fd1dc537d62d" class="bulleted-list"><li style="list-style-type:disc">Progressive learning은 모델의 크기를 줄이기 위함이 아닌 <strong>데이터의 크기, 특히 이미지 자체의 해상도를 줄이는 학습 방법을 제안하면서 등장한 EfficientNet V2에 쓰인 학습 방법</strong>이다. </li></ul><ul id="699a9bdb-ddf0-4699-885e-1056b1611ffe" class="bulleted-list"><li style="list-style-type:disc">기존 EfficientNet을 개선한 EfficientNet V2는 줄어든 크기의 입력 이미지로도 좋은 성능을 얻을 수 있다. </li></ul><figure id="42305a74-ba4d-4827-85bd-3da1af8bf115" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2015.png"><img style="width:432px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2015.png"/></a></figure><ul id="f60ee986-f121-4d56-b89d-19dd178fbec7" class="bulleted-list"><li style="list-style-type:disc">작은 크기의 이미지로 학습할 때는 정보량이 많지 않아 충분히 학습이 가능하기 때문에, regularization의 강도를 줄여야 한다. 반면 큰 크기의 이미지로 학습할 때는 정보량이 많아 overfitting이 발생할 수 있기 때문에 regularization의 강도를 키워서 학습해야 한다. 이를 <strong>progressive learning with adaptive regularization</strong>이라 한다.</li></ul><figure id="fa3d7dce-058d-41f1-b233-fbb81218256e" class="image" style="text-align:center"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2016.png"><img style="width:480px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2016.png"/></a></figure><figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="390d66ba-e393-4c65-ae9d-b42311f3e519"><div style="font-size:1.5em"><span class="icon">💡</span></div><div style="width:100%">실험 힘듦, 오래걸림, 실제 논문에서 발표된 학습시간은 350 에포크 가량으로 이번 과제에 적용하기에는 학습 시간 및 총 5회 학습 진행해야된다는 점 감안하여 부적절하다고 판단함. 테스트를 진행했을 때는 학습시간을 적게 하여 진행하려 했으나 정확도가 안 나온다.</div></figure><p id="64cdeb6a-4922-418c-ac7b-2db63a1b7ad4" class="">
</p><hr id="89657956-98ac-41b2-98cd-1fbf5db69f47"/><h2 id="374aefb0-d3fe-4265-a889-9c5ae92d12ae" class="">3. 성능</h2><figure id="1c97eb46-f294-414e-b28f-1254648b48cc" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2017.png"><img style="width:720px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2017.png"/></a></figure><figure id="65f65dbf-b694-4f9e-9e19-6835ad6793bb" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2018.png"><img style="width:720px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2018.png"/></a></figure><figure id="3c1617df-e43e-4ca7-8131-cb6171ae7e8f" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2019.png"><img style="width:720px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2019.png"/></a></figure><figure id="9c7454f8-221d-4bcf-b3f6-30eb103a221a" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2020.png"><img style="width:720px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2020.png"/></a></figure><figure id="5a6ffae0-c9f1-47e0-9d12-a804ee891f2c" class="image"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2021.png"><img style="width:720px" src="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/Untitled%2021.png"/></a></figure><p id="006c99e6-a23c-4c59-bbc1-54e094f6c403" class="">5회 평균 정확도 : 0.8667</p><p id="94099b08-b79b-4fbc-88d7-08b911a83b5a" class="">
</p><figure id="94bb328a-0cb9-4367-9fd0-258e32046cd1"><div class="source"><a href="CIFAR-100%20Classification%20d3382ef4b9e04ad683dab70348718c90/7%25EC%25A1%25B0_2%25EC%25A3%25BC%25EC%25B0%25A8_%25EC%25BD%2594%25EB%2593%259C.py">7조_2주차_코드.py</a></div></figure></div></article><span class="sans" style="font-size:14px;padding-top:2em"></span></body></html>
