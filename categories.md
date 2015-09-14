---
layout: default
title: Category archive
---
<div class="page-content wc-container">
  <h1>Categories</h1>  

  <nav>

       {% for category in site.categories %}

           <a href="#{{ category | first | remove:' ' }}">&lt;{{ category | first }}&gt;</a>
       {% endfor %}
  </nav>

  <p></p>


   {% for category in site.categories %}
       <div class="catbloc" id="{{ category | first | remove:' ' }}">
           <h2>{{ category | first }}</h2>

           <ul>
              {% for posts in category %}
                {% for post in posts %}
                  {% if post.url %}
                    <li>
                     <a href="{{ post.url }}">
                       <time>{{ post.date | date: "%Y-%m-%d" }}</time>
                       {{ post.title }}
                     </a>
                   </li>
                 {% endif %}
               {% endfor %}
             {% endfor %}
          </ul>
      </div>
  {% endfor %}

</div>
