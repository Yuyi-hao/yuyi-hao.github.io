---
layout: page
title: Extensions
icon: fas fa-puzzle-piece
order: 2
---

Browser extensions I've built. They're free and open source, and you can download and install them below.

{% assign extensions = site.data.projects_list | where: "category", "extensions" %}
{% for ext in extensions %}
<div class="card mb-4">
  <div class="row g-0">
    {% if ext.image and ext.image != "" %}
    <div class="col-md-5">
      <img src="{{ ext.image | relative_url }}" alt="{{ ext.name }} screenshot" class="img-fluid rounded-start h-100" style="object-fit: cover;" loading="lazy">
    </div>
    {% endif %}
    <div class="{% if ext.image and ext.image != '' %}col-md-7{% else %}col-12{% endif %}">
      <div class="card-body">
        <h3 class="card-title mt-0">{{ ext.name }}</h3>
        <p class="text-muted">{{ ext.description }}</p>
        <p class="small mb-3">
          {% if ext.browser %}<strong>Browser:</strong> {{ ext.browser }}<br>{% endif %}
          {% if ext.last_updated != "" %}<strong>Updated:</strong> {{ ext.last_updated }}<br>{% endif %}
          {% if ext.license != "" %}<strong>License:</strong> {{ ext.license }}{% endif %}
        </p>
        <a href="{{ ext.download }}" class="btn btn-primary me-2 mb-2">
          <i class="fas fa-download me-1"></i> Download (.zip)
        </a>
        <a href="{{ ext.repo }}" target="_blank" rel="noopener noreferrer" class="btn btn-outline-secondary mb-2">
          <i class="fab fa-github me-1"></i> Source
        </a>
      </div>
    </div>
  </div>
</div>
{% endfor %}

## How to install

These extensions aren't on the Chrome Web Store yet, so you install them in developer mode:

1. Download the `.zip` above and extract it.
2. Open `chrome://extensions/` (in Edge use `edge://extensions/`, in Brave `brave://extensions/`).
3. Turn on **Developer mode** (top-right toggle).
4. Click **Load unpacked** and select the extracted folder, which contains `manifest.json`.
5. The extension is now active. Pin it from the puzzle-piece menu in the toolbar if you like.

To update, download the new zip, replace the folder, and click the reload icon on the extension's card in `chrome://extensions/`.
{: .prompt-tip }
