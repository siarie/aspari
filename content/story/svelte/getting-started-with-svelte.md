---
title: "Getting Started With Svelte 3"
date: 2019-08-12T10:14:55+07:00
tags: [
	sveltejs,
]
categories: [
	svelte,
	javascript
]
draft: true
series: "svelte"
---



# Apa itu Svelte?
Pada dasarnya Svelte merupakan *javascript framework* sama seperti React atau Vue. Tetapi ada beberapa perbedaan

<pre data-enlighter-language="js" data-enlighter-linenumbers="true" >
$('#loading-example-btn').click(function () {
  var btn = $(this)
  btn.button('loading')
  $.ajax(...).always(function () {
    btn.button('reset')
  });
});
</pre>