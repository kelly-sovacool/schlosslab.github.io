---
layout: index_page
category: papers
title: Papers
---

<div class="bibliography">

<ol>
	{%	for paper_hash in site.data.papers	%}
		{%	assign pub = paper_hash[1]	%}
		<li>
			<b>{{ pub.authors }}.</b>
			{{ pub.year }}.
			{{ pub.title }}.
			{{ pub.journal }}.
			<b>{{ pub.volume }}:</b>
			{{ pub.pages }}.

			{% if pub.doi %}
			DOI: <a href="http://doi.org/{{pub.doi}}">{{pub.doi}}</a>.
			{% endif %}

			<div class="supp">
				<a href="/assets/pdf/{{paper_hash[0]}}.pdf">
					<i class="fa fa-file-pdf-o fa-lg"></i>
				</a>
				{% if pub.github	%}
					<a href="https://github.com/{{ pub.github }}">
						<i class="fa fa-github fa-lg" ></i>
					</a>
				{% endif			%}

				{% if pub.data		%}
					<a href="{{pub.data}}">
						<i class="fa fa-table fa-lg" ></i>
					</a>
				{% endif			%}
			</div>

		</li>
	{%	endfor %}
</ol>
</div>