---
layout: default
title: Projects
---

<div class="container">
    <h1>Research Projects</h1>
    <p>Our lab works on a variety of cutting-edge research projects at the intersection of neuroscience and artificial intelligence.</p>

    <h2 id="active" class="mt-lg">Active Projects</h2>
    <div class="projects-grid">
        {% if site.data.projects.active %}
            {% for project in site.data.projects.active %}
            <div class="project-card">
                {% if project.image %}
                <img src="{{ project.image }}" alt="{{ project.title }}" class="project-image">
                {% endif %}
                <div class="project-content">
                    <div class="project-title">
                        {% if project.url %}
                        <a href="{{ project.url }}">{{ project.title }}</a>
                        {% else %}
                        {{ project.title }}
                        {% endif %}
                    </div>
                    <p class="project-description">{{ project.description }}</p>
                    <p class="project-meta">
                        <strong>Team:</strong> {{ project.members | array_to_sentence_string }}
                    </p>
                    {% if project.funding %}
                    <p class="project-meta">
                        <strong>Funding:</strong> {{ project.funding }}
                    </p>
                    {% endif %}
                </div>
            </div>
            {% endfor %}
        {% endif %}
    </div>

    <h2 id="completed" class="mt-lg">Completed Projects</h2>
    <div class="projects-grid">
        {% if site.data.projects.completed %}
            {% for project in site.data.projects.completed %}
            <div class="project-card">
                {% if project.image %}
                <img src="{{ project.image }}" alt="{{ project.title }}" class="project-image">
                {% endif %}
                <div class="project-content">
                    <div class="project-title">
                        {% if project.url %}
                        <a href="{{ project.url }}">{{ project.title }}</a>
                        {% else %}
                        {{ project.title }}
                        {% endif %}
                    </div>
                    <p class="project-description">{{ project.description }}</p>
                    <p class="project-meta">
                        <strong>Team:</strong> {{ project.members | array_to_sentence_string }}
                    </p>
                    {% if project.year %}
                    <p class="project-meta">
                        <strong>Completed:</strong> {{ project.year }}
                    </p>
                    {% endif %}
                </div>
            </div>
            {% endfor %}
        {% endif %}
    </div>

    <div class="mt-lg">
        <h2>Collaborations</h2>
        <p>
            We actively collaborate with research groups worldwide. If you're interested in collaborating,
            please reach out to us at <a href="mailto:contact@neuroai.edu">contact@neuroai.edu</a>.
        </p>
    </div>
</div>
