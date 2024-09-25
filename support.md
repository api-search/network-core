---
layout: page
title: Support
---

# Support
APIs.io is an open source API search engine maintained by a handful of individuals, and we are relying on just a handful of social and community ways to support the project--use one of the following channels to learn more about what is happening and get your questions answered. 

{% assign supports = site.data.support %}
<div class="container">
    <div class="row">

        {% for support in supports %}
        <div class="col-sm-4">
            <div class="card">
            <div class="card-body">
                <h5 class="card-title">{{ support.name }}</h5>
                <p class="card-text">{{ support.description }}</p>
                <a href="{{ support.url }}" class="btn btn-primary">Go</a>
            </div>
            </div>
        </div>    
        {% endfor %}

    </div>
</div>


Thank you for getting involved and helping out where you can, making it a community effort to get this search engine stood up, indexing, and making the world of APIs more discoverable in a way that benefits everyone.
<div class="container text-center" style="width: 75%;margin-top:50px;">
    {% include partner.html %} 
</div>