<!doctype html>
<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="chrome=1">

{% seo %}
    <link rel="stylesheet" href="{{ '/assets/css/style.css?v=' | append: site.github.build_revision | relative_url }}">
    <script src="https://code.jquery.com/jquery-3.3.0.min.js" integrity="sha256-RTQy8VOmNlT6b2PIRur37p6JEBZUE7o8wPgMvu18MC4=" crossorigin="anonymous"></script>
    <script src="{{ '/assets/js/main.js' | relative_url }}"></script>
    <!--[if lt IE 9]>
      <script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv.min.js" integrity="sha256-3Jy/GbSLrg0o9y5Z5n1uw0qxZECH7C6OQpVBgNFYa0g=" crossorigin="anonymous"></script>
    <![endif]-->
    <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">

  </head>
  <body>

      <header>
        <h1>{{ site.title | default: site.github.repository_name }}</h1>
        <p>{{ site.description | default: site.github.project_tagline }}</p>
      </header>

      <div id="banner">
        <span id="logo"></span>

        <a href="{{ site.github.repository_url }}" class="button fork"><strong>View On GitHub</strong></a>
        {% if site.show_downloads %}
          <div class="downloads">
            <span>Downloads:</span>
            <ul>
              <li><a href="{{ site.github.zip_url }}" class="button">ZIP</a></li>
              <li><a href="{{ site.github.tar_url }}" class="button">TAR</a></li>
            </ul>
          </div>
        {% endif %}
      </div><!-- end banner -->

    <div class="wrapper">
      <nav>
        <ul></ul>
      </nav>
      <section>
        {{ content }}

      </section>
      <footer>
        {% if site.github.is_project_page %}
          <p>Project maintained by <a href="{{ site.github.owner_url }}">{{ site.github.owner_name }}</a></p>
        {% endif %}
        <p><small>Hosted on GitHub Pages &mdash; Theme by <a href="https://twitter.com/michigangraham">mattgraham</a></small></p>
      </footer>
    </div>
    <!--[if !IE]><script>fixScale(document);</script><![endif]-->

    {% if site.google_analytics %}
      <script type="text/javascript">
        (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
        (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
        m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
        })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
        ga('create', '{{ site.google_analytics }}', 'auto');
        ga('send', 'pageview');
      </script>
    {% endif %}
  </body>
</html>
