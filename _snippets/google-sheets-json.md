---
title: Google Sheets JSON Data
layout: snippet
comments: false
---

## {{ page.title }}

### HTML Table Code
<pre><code class="html">
&lt;section class="table-responsive" id="specDetails"&gt;
&lt;h2&gt;Specification Details&lt;/h2&gt;
  &lt;table id="datadetails"&gt;
  &lt;/table&gt;
&lt;script id="spec-template" type="text/template"&gt;
&#123;&#123;#entry&#125;&#125;
  &lt;tr&gt;
      &lt;td class="col1"&gt;&#123;&#123;gsx$desc1.$t&#125;&#125;&lt;/td&gt;
      &lt;td class="bd col2"&gt;&#123;&#123;gsx$data1.$t&#125;&#125;&lt;/td&gt;
      &lt;td class="col3"&gt;&#123;&#123;gsx$desc2.$t&#125;&#125;&lt;/td&gt;
      &lt;td class="bd col4"&gt;&#123;&#123;gsx$data2.$t&#125;&#125;&lt;/td&gt;
      &lt;td class="col5"&gt;&#123;&#123;gsx$desc3.$t&#125;&#125;&lt;/td&gt;
      &lt;td class="bd col6"&gt;&#123;&#123;gsx$data3.$t&#125;&#125;&lt;/td&gt;
  &lt;/tr&gt;
&#123;&#123;/entry&#125;&#125;
&lt;/script&gt;
&lt;/section&gt;
</code></pre>

### Javascript Code
<pre><code class="javascript">
$(function () {  
  $.getJSON("https://spreadsheets.google.com/feeds/list/1UaWeCOYaX6LUaxw-3EMkcxDd_tJcHVbivQzbou7XETI/1/public/values?hl=en_US&alt=json", function( data) {
    var template = $('#spec-template').html();
    var info = Mustache.to_html(template, data.feed);
    $('#datadetails').html(info);
    });
    });
    </code></pre>

### CSS code
<pre><code class="css">
#specDetails {
  height: 100%;
}
#specDetails h2 {
  margin: 70px 0 5px 20px;
}
#specDetails #datadetails {
  margin: 0 20px 0 20px;
}
#specDetails .col1,
#specDetails .col3,
#specDetails .col5 {
  width: 11%;
}
#specDetails .col2,
#specDetails .col4,
#specDetails .col6 {
  width: 22%;
}
#specDetails td {
  text-align: right;
  font-size: .9em;
  padding: 4px 4px 4px 4px;
  border: 1px solid #bbb;
}
#specDetails td.bd {
  font-weight: 600;
  text-align: center;
}
</code></pre>

-- end of document --
