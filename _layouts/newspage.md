---
layout: default
twitterfeed: false
---


<div class="post">

  <header class="post-header">
    <h1 class="post-title">
     {% if page.title == blank %}
     {{ page.name }}
     {% else %}
     {{ page.title }}
     {% endif %}
    </h1>
       <p class="post-description" style="border-bottom-style:dashed; border-bottom-color:lightgrey; border-bottom-width:1px;">{{ page.description }}</p>
  </header>

  <article>

    <div class="wrapper" style="diplay:inline-block;width:100%;">
        <div class="clearfix">
          {{ content }}
        </div>
        {% if page.twitterfeed %}
            <div style="float:left; width:70%;">
        {% else %} 
            <div style="float:left; width:90%;">
        {% endif %}
        {% if page.news %}
          {% include news.html %}
        {% endif %}
        </div>
        {% if page.twitterfeed %}
            <div style="float:right;width:30%;">
              {% include twitterfeed.html %}
            </div>
        {% endif %}
    </div>
    
    <div style="clear:both;"></div>
    
    {% if page.selected_papers %}
      {% include selected_papers.html %}
    {% endif %}
    
    {% if page.social %}
    <hr>
    <div class="social">
      {% include social.html %}
      <div class="contact-note">{{ site.contact_note }}</div>
    </div>
    {% endif %}
  </article>

</div>
