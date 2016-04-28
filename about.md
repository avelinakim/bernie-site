---
layout: page
title: About
permalink: /about/
---

<div class="About">
  <div class="General-Info">
    <h1> General Info: </h1>
      <div class="Info-Elements">
      <b>Meetings:</b> <br> Tuesdays 11:15am-12:45pm | Room TBA <br>
                            Fridays 11:15am-12:45pm | Room SCI 157 <br><br>
      <b>Contact: </b>
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
        Please fill out this <a href="http://goo.gl/forms/BcbbLufTNb">form</a> if you're interested in becoming a member 
      </div>
  </div>
  
  <hr>
  
  <div class="about-section">
     <img src="{{ site.baseurl }}/assets/imgs/fight-for-15.jpg" title="first-meeting" class="image">
     <div class="about-content">
     <h1> About Us </h1>
     <p> Santa Monica College Students for Bernie Sanders is a diverse group of students organizing
     to drastically change the political system in America. We believe that Senator Bernie Sanders 
     is the best candidate to help bring about that change.</p>
     </div> 
  </div>
 
 <hr>
 
 <div class="about-section">
 <h1> Meet the Officers </h1>
 {% for officer in site.officers %}
 <div class="officer">
  <img src="{{ site.baseurl }}{{ officer.img }}" title="Profile Picture" class="profile">
  <div class="content">
      <h1 class="officer-title"> {{ officer.name }} </h1>
      <p class="officer-position"> {{ officer.position }} </p>
      <p>{{ officer.description }}</p>
  </div>
 </div>
 {% endfor %}
 
 </div>
  
</div>


