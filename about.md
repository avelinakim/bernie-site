---
layout: page
title: About
permalink: /about/
---

<!--<img src="{{ site.baseurl }}/assets/profile-placeholder.gif" title="Profile Picture" class="profile">

Centrarium is a custom theme for Jekyll, made by [Ben Centra][bencentra] for his own blog. He'd be humbled if you liked it enough to use it as well! Installation and configuration instructions can be found in the [GitHub repository](https://github.com/bencentra/centrarium).

This page is a good place to write about yourself, your project, your product, or whatever it is your site is for. You can replace the image above, or you can get rid of it entirely. 

You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](http://jekyllrb.com/). And you can find the source code for Jekyll at [github.com/jekyll/jekyll](https://github.com/jekyll/jekyll)

[centrarium]: https://github.com/bencentra/centrarium
[bencentra]: http://bencentra.com
[jekyll]: https://github.com/jekyll/jekyll
-->

<div class="About">
  <div class="General-Info">
    <h1> General Info: </h1>
      <div class="Info-Elements">
      Meetings: Fridays 11:15am-12:45pm <br>
      Contact:  
        <div class="site-contact">
        <ul class="social-media-list">
          <li>
            <a href="mailto:{{ site.email }}">
              <i class="fa fa-envelope-o"></i>
              <span class="username">{{ site.email }}</span>
            </a>
          </li>

          {% for social in site.social %}
            {% if social.url != null %}
            <li>
              <a href="{{ social.url }}" title="{{ social.desc }}">
                <i class="fa fa-{{ social.icon }}"></i>
                <span class="username">{% if social.username %}{{ social.username }}{% else %}{{ social.name }}{% endif %}</span>
              </a>
            </li>
            {% endif %}
          {% endfor %}
        </ul>
        </div>
      </div>
  </div>
  
  <hr>
  
  <div class="about-section">
     <img src="{{ site.baseurl }}/assets/imgs/Bernie 1st meeting.jpg" title="first-meeting" class="image">
     <div class="content">
     <h1> About Us </h1>
     <p> What we do & why we do it. What we do & why we do it. What we do & why we do it. What we do & why we do it.</p>
     </div> 
  </div>
 
 <hr>
 
 <div class="about-section">
 <h1> Meet the Officers </h1>
 {% for officer in site.officers %}
 <div class="officer">
  <img src="{{ site.baseurl }}{{ officer.img }}" title="Profile Picture" class="profile">
  <div class="content">
      <h1 class="officer-title"> {{ officer.position }}: {{ officer.name }} </h1>
      <p>{{ officer.description }}</p>
  </div>
 </div>
 {% endfor %}
 
 </div>
  
</div>


