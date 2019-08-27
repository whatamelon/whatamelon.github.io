---
layout: main
title: Seungho Hong
main: true
subtitle: seungho hong git blog main
description: seungho hong git blog background , intro , main
---
<style>

main,
footer>.footer_wrap,
.nav-container {
  margin: 0px 0px 0px 0px;
  max-width: 100%;
  width: 100%;
    @media (max-width: $break-small) {
        width: 88%;
    }
}
canvas {
    height:1080px;
    position:relative;
}
.in {
    position:absolute;
    max-width:1000px;
    left:25%;
    top:20%;
    z-index:1;
}

section.skill {
    margin-left:33%;
    li.skill_name {
        display: inline-block;
        font-family: SCDREAM,SCDREAM;
        padding: 4px 14px;
        border-radius: 100px;
        border: solid 1px $grey-2;
        font-size: 16px;
        margin: 0 8px 14px 0;
    }
}

</style>

<div id="particles">
    <!-- <canvas class="pg-canvas" style="display: block; width:100%; height:100%;"></canvas> -->
</div>

<div class="in">
<img src="./img/logo.png"/>

<section class="skill">
<ul>
<li class="skill_name">
<a href="{{ '/develop' | prepend: site.baseurl }}" {% if current[1] == "develop" %} class="active"{% endif %} >Develop</a>
</li>
<li class="skill_name">
<a href="{{ '/blog' | prepend: site.baseurl }}" {% if current[1] == "blog" %} class="active"{% endif %} >Blog</a>
</li>
<li class="skill_name">
<a href="{{ '/about' | prepend: site.baseurl }}" {% if current[1] == "about" %} class="active"{% endif %} >Who am I ?</a>
</li>
</ul>
</section>

</div>



<!--<div class="intro-link">
            <a class="transition" href="http://ridicorp.com/" target="_blank">
                RIDI
            </a>
            <div class="underline-mask transition"></div>
            <div class="underline"></div>
        </div>. -->
    
