<script>
  let activeBlock = null;

  function showPublications(type) {
    const allItems = document.querySelectorAll('.pub-item');
    allItems.forEach(item => {
      const itemTypes = item.getAttribute('data-type').split(',');
      if (type === 'all' || itemTypes.includes(type)) {
        item.style.display = 'block';
      } else {
        item.style.display = 'none';
      }
    });
  }

  function handleMouseEnter(block) {
    if (activeBlock) {
      activeBlock.classList.remove('active');
    }
    activeBlock = block;
    activeBlock.classList.add('active');
    showPublications(block.getAttribute('data-type'));
  }

  window.onload = function () {
    showPublications('all');
  };
</script>

<style>
  .pub-type-filter {
    display: flex;
    justify-content: flex-start;
    margin-bottom: 20px;
    flex-wrap: wrap;
  }

  .pub-type {
    min-width: 70px;
    padding-left: 12px;
    padding-right: 12px;
    height: 26px;
    line-height: 24px;
    background-color: #f1f1f1;
    border-radius: 5px;
    cursor: pointer;
    text-align: center;
    font-weight: bold;
    transition: background-color 0.3s ease;
    margin-right: 10px;
    border: 2px solid transparent;
  }

  .pub-type[data-type="all"] {
    background-color: #aadaac;
  }

  .pub-type[data-type="mllm"] {
    background-color: #f4a286;
  }

  .pub-type[data-type="genai"] {
    background-color: #9abcec;
  }

  .pub-type[data-type="agent"] {
    background-color: #b39ddb;
  }

  .pub-type[data-type="video"] {
    background-color: #80cbc4;
  }

  .pub-type[data-type="science"] {
    background-color: #ffd966;
  }

  .pub-type:hover {
    opacity: 0.8;
  }

  .active {
    border-color: inherit;
  }

  .pub-type[data-type="all"]:hover,
  .active[data-type="all"] {
    background-color: #4dae50;
    color: #e0e0e0;
  }

  .pub-type[data-type="mllm"]:hover,
  .active[data-type="mllm"] {
    background-color: #e64a19;
    color: white;
  }

  .pub-type[data-type="genai"]:hover,
  .active[data-type="genai"] {
    background-color: #1e88e5;
    color: white;
  }

  .pub-type[data-type="agent"]:hover,
  .active[data-type="agent"] {
    background-color: #7e57c2;
    color: white;
  }

  .pub-type[data-type="video"]:hover,
  .active[data-type="video"] {
    background-color: #00897b;
    color: white;
  }

  .pub-type[data-type="science"]:hover,
  .active[data-type="science"] {
    background-color: #f1c232;
    color: black;
  }

  .pub-item {
    display: none;
  }

  .pub-scroll {
    max-height: 440px;
    overflow-y: auto;
    overflow-x: hidden;
    margin-top: 12px;
    padding: 4px 14px 4px 4px;
    border: 1px solid rgba(128, 128, 128, 0.25);
    border-radius: 8px;
  }

  .pub-scroll::-webkit-scrollbar {
    width: 8px;
  }

  .pub-scroll::-webkit-scrollbar-thumb {
    background: rgba(128, 128, 128, 0.5);
    border-radius: 4px;
  }

  .pub-scroll::-webkit-scrollbar-thumb:hover {
    background: rgba(128, 128, 128, 0.75);
  }

  .pub-stats {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 8px 6px;
    margin: 10px 0 16px;
  }

  .pub-stats-label {
    font-weight: 700;
    color: #2b6cb0;
    margin-right: 2px;
  }

  .pub-stat {
    display: inline-block;
    padding: 2px 12px;
    border: 2px solid #4a90e2;
    border-radius: 18px;
    color: #2b6cb0;
    font-weight: 600;
    font-size: 0.85rem;
    background: #ffffff;
  }

  .pub-sep {
    color: #b8cfe6;
    font-weight: 600;
  }

  .pub-stat-total {
    display: inline-block;
    padding: 2px 14px;
    border-radius: 18px;
    background: #f5a623;
    color: #ffffff;
    font-weight: 700;
    font-size: 0.85rem;
  }
</style>

<br>
<h2 id="publications" style="margin: 2px 0px -15px;">Selected Publications <temp style="font-size:15px;">[</temp><a href="https://scholar.google.com/citations?hl=en&user=x2VGVvcAAAAJ" target="_blank" style="font-size:15px;">Google Scholar</a><temp style="font-size:15px;">]</temp></h2>

<div class="publications">
  <div class="pub-stats">
    <span class="pub-stats-label">Publication Statistics:</span>
    <span class="pub-stat">CCF A: 9</span><span class="pub-sep">|</span>
    <span class="pub-stat">CCF B: 3</span><span class="pub-sep">|</span>
    <span class="pub-stat">TMLR: 1</span><span class="pub-sep">|</span>
    <span class="pub-stat">JCR Q1: 2</span>
    <span class="pub-stat-total">✓ Total: 15</span>
  </div>
  <p style="font-size:0.82rem; color:#8a8a8a; margin:6px 0 10px;">† Equal contribution &nbsp;&nbsp; * Corresponding author</p>
  <div class="pub-type-filter">
    <div class="pub-type" data-type="all" onmouseover="handleMouseEnter(this)">All</div>
    <div class="pub-type" data-type="mllm" onmouseover="handleMouseEnter(this)">MLLM</div>
    <div class="pub-type" data-type="genai" onmouseover="handleMouseEnter(this)">Generative</div>
    <div class="pub-type" data-type="agent" onmouseover="handleMouseEnter(this)">Agentic</div>
    <div class="pub-type" data-type="video" onmouseover="handleMouseEnter(this)">Video</div>
    <div class="pub-type" data-type="science" onmouseover="handleMouseEnter(this)">AI4Science</div>
  </div>

  <div class="pub-scroll">
  <ol class="bibliography">
    {% for link in site.data.publications.main %}
  <li class="pub-item" data-type="{{ link.type }}">
      <div class="pub-row">
        <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
          {% if link.image %}
          <img src="{{ link.image }}" playsinline="" class="teaser img-fluid z-depth-1" loading="lazy">
          {% endif %}
          {% if link.video %}
          <video poster="" id="teaser" autoplay muted loop class="teaser img-fluid z-depth-1">
            <source src="{{ link.video }}" type="video/mp4">
          </video>
          {% endif %}
          {% if link.conference_short %}
          <abbr class="badge">{{ link.conference_short }}</abbr>
          {% endif %}
          {% if link.is_preprint %}
          <abbrp class="badge">Preprint</abbrp>
          {% endif %}
        </div>
        <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
          <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
          <div class="author">{{ link.authors }}</div>
          <div class="periodical"><em>{{ link.conference }}</em></div>
          <div class="links">
            {% if link.page %}
            <a href="{{ link.page }}" target="_blank" class="btn btn-sm z-depth-0" style="font-size:12px;">Project Page</a>
            {% endif %}
            {% if link.pdf %}
            <a href="{{ link.pdf }}" target="_blank" class="btn btn-sm z-depth-0" style="font-size:12px;">PDF</a>
            {% endif %}
            {% if link.code %}
            <a href="{{ link.code }}" target="_blank" class="btn btn-sm z-depth-0" style="font-size:12px;">Code</a>
            {% endif %}
            {% if link.data %}
            <a href="{{ link.data }}" target="_blank" class="btn btn-sm z-depth-0" style="font-size:12px;">Data</a>
            {% endif %}
            {% if link.bibtex %}
            <a href="{{ link.cbibtex }}" target="_blank" class="btn btn-sm z-depth-0" style="font-size:12px;">BibTex</a>
            {% endif %}
            {% if link.notes %}
            <strong> &nbsp; <i style="color:#e74d3c">{{ link.notes }}</i></strong>
            {% endif %}
            {% if link.others %}
            {{ link.others }}
            {% endif %}
          </div>
        </div>
      </div>
      <br>
  </li>
    {% endfor %}
</ol>
  </div>
  <p style="text-align:center; font-size:0.8rem; color:#8a8a8a; margin:8px 0 0;">↓ scroll to see more publications</p>
</div>
