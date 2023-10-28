---
layout: page
title: Rules
---
All of the APIs indexed with APIs.io are rated using Spectral rules that are designed to look for specific properties, and when found points are applied. The goal of these rules are to incentivize API producers to index their APIs, and provide as many properties as possible, helping API consumers be more successful. These are all of the rules currently being used to rate APIs, including the current points applied.

{% assign rules = site.data.rules %}
<div class="container">
    <div class="row">

        {% for rule in rules %}
        <div class="col-sm-4">
            <div class="card">
            <div class="card-body">
                <h5 class="card-title">{{ rule.description }}</h5>
                <p class="card-text">{{ rule.message }}</p>
                <p class="card-text">{{ rule.score }} points</p>
            </div>
            </div>
        </div>    
        {% endfor %}

    </div>
</div>
<br>
We are  just getting started and wil be adding new rules, refining existing rules, and adjust points based upon the desired behaviors we are looking for. APIs that have a higher score applied by the rating system will show up higher in the search index, helping the best APIs rise to the top. As more APIs are added we will keep applying what we are learning through the development of new rules.