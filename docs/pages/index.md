---
layout: default
title: Narveer Rathore | that lazy web developer
permalink: /
weight: 2
---
<style>
.avatar {
    width: 200px;
    border-radius: 50%;
    overflow: hidden;
    margin: 20px 0;
    border: 4px solid;
    border: 4px solid rgba(100, 100, 100, 1);
    border-left-color: azure;
    border-top-color: azure;
}
.avatar:hover {
    filter: opacity(0.5);
}
@media screen and (max-width: 600px) {
    .d-mob-none {
        display: none;
    }
}
</style>

<div class="text-center">
    <br />
    <h2 class="d-mob-none"><b>about me</b></h2>
    <img class="avatar" src="assets/image.jpg" alt="picture of narveer rathore" />
    <p>
    Hi, I am {{ site.author.name }} :wave:<br>
    <br /> I am a web developer at <a href="https://now.gg" target="_blank">now.gg</a><br /> and I believe that boredom can <br > do wonders.
    </p>
</div>
<div>
  {% include social.html %}
</div>
{% comment %}
<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills" source=site.data.other-skills %}
</div>
<div class="row">
{% include about/timeline.html %}
</div>
{% endcomment %}