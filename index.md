---
title: MetaSLAM
subtitle: A Collective Intelligence Framework for Mapping, Localization and Exploration
layout: page
# callouts: home_callouts
# show_sidebar: true
show_sidebar: false
hide_footer: false
hero_height: is-large
hero_image: /img/web.gif
hero_link: /research/
hero_link_text: Researches

# hero_link2: /publications/
# hero_link_text2: Publications

# hero_link3: /playground/
# hero_link_text3: Playground
---

# About Us

MetaSLAM is a joint organization, targeting at cutting-edge robotics localization, mapping, exploration and decision making.
<!-- We are combined with the top-researchers abround the world, [Carnegie Mellon University](https://www.cmu.edu/),  -->

# Highlights
{% assign posts = site.posts | where:"categories","highlights" %}
<div class="columns is-multiline">
    {% for post in posts %}
    <div class="column is-4-desktop is-6-tablet">
        {% include post-card.html %}
    </div>
    {% endfor %}
</div>
