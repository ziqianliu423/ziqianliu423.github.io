<h2 id="publications" style="margin-bottom: 1.25rem;">Other Publications</h2>

<div class="publications">
  <ol class="bibliography" style="padding-left: 0; list-style: none; margin: 0;">
    {% for link in site.data.other_publications.main %}
    <li style="margin-bottom: 1.5rem;">
      <div class="pub-row row">
        <!-- 左侧：图片 / 标签栏 -->
        <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
          {% if link.image %}
            <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 120px; height: auto;">
            {% if link.conference_short %}
              <abbr class="badge" style="position: absolute; bottom: 0; right: 15px;">{{ link.conference_short }}</abbr>
            {% endif %}
          {% endif %}
        </div>
        
        <!-- 右侧：详细内容栏 -->
        <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
          <div class="title" style="font-weight: bold;">
            <a href="{{ link.pdf }}">{{ link.title }}</a>
          </div>
          <div class="author" style="margin-top: 0.25rem;">{{ link.authors }}</div>
          <div class="periodical" style="margin-top: 0.25rem;">
            <em>{{ link.conference }}</em>
          </div>
          
          <!-- 按钮与链接列表 -->
          <div class="links" style="margin-top: 0.5rem;">
            {% if link.pdf %}
              <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px; margin-right: 4px;">PDF</a>
            {% endif %}
            {% if link.code %}
              <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px; margin-right: 4px;">Code</a>
            {% endif %}
            {% if link.page %}
              <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px; margin-right: 4px;">Project Page</a>
            {% endif %}
            {% if link.bibtex %}
              <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px; margin-right: 4px;">BibTex</a>
            {% endif %}
            {% if link.notes %}
              <strong style="margin-left: 5px;"><i style="color: #e74d3c;">{{ link.notes }}</i></strong>
            {% endif %}
            {% if link.others %}
              <span style="margin-left: 5px;">{{ link.others }}</span>
            {% endif %}
          </div>
        </div>
      </div>
    </li>
    {% endfor %}
  </ol>
</div>
