artTemplate-for-seajs
=====================

Improvement for the usage in seajs.

artTemplate
------------

JavaScript Template Engine  
Simple use please look for [artTemplate].

Updated
-------

New feature: Add the option that you can append the template in the html element where you want.  
Example: 

    art.render2({template name}, {element}?, {data}?);
    
Element and data are optional.

Usage
-----
    
You can just start use the template like below.

    // require the artTemplate
    var art = require('plugin-template');
    // render the home.tpl file
    art.render2('home');
    
For this version, the plugin is just simple.  
It fixed the path where the \*.tpl place in.  
{base}/views/{\*.tpl}

If you want to pass some params, you should use.

**home.tpl**  
The code is from [artTemplate].

    <ul>
      <% for (var i = 0; i < list.length; i ++) { %>
        <li>索引： <%=i + 1%> - 内容：<%=list[i]%></li>
      <% } %>
    </ul>
    
**home.js**  

    define('home', [], function (require) {
      var art = require('plugin-template');
      art.render2('home', {
        list: ['文艺', '博客', '摄影', '电影', '民谣', '旅行', '吉他']
      });
    });

[artTemplate]: https://github.com/aui/artTemplate