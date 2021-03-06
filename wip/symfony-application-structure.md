<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Symfony Application Structure &mdash; Loïc Faugeron &mdash; Technical Blog</title>
    <meta name="description" content="Technical articles about Symfony and TDD">
    <meta name="author" content="Loïc Faugeron">

    <meta name="viewport" content="width=device-width, initial-scale=1">

    <link rel="canonical" href="/wip/symfony-application-structure.md"/>
        <link rel="alternate" href="https://gnugat.github.io/feed/atom.xml" type="application/atom+xml" title="Loïc Faugeron"/>
    
    <link rel="stylesheet" href="https://gnugat.github.io/css/normalize.css">
    <link rel="stylesheet" href="https://gnugat.github.io/css/skeleton.css">
    <link rel="stylesheet" href="https://gnugat.github.io/css/dop-dop-dop.css">
    <link rel="stylesheet" href="https://gnugat.github.io/css/highlight_9_0_0_monokai_sublime.min.css">
</head>
<body>
    <div class="container">
        <header class="title">
            <h1>
                <a href="https://gnugat.github.io/">Loïc Faugeron</a>
                <span class="sub-title">Technical Blog</span>
            </h1>
        </header>

        <article>
            <header>
                <h2>
    Symfony Application Structure
    <span class="sub-title">24/03/2016</span>
</h2>
                            <nav>
                                                            <a class="button " href="https://gnugat.github.io/tags/symfony">symfony</a>
                    </nav>
                </header>

                <blockquote>
  <p><strong>TL;DR</strong>:</p>
  
  <ol>
  <li><code>AppBundle</code> only</li>
  <li>extract services to <code>Vendor\Project\Domain</code>, <code>Vendor\Project\Bridge</code> and <code>Vendor\Project\Bundle</code></li>
  <li>split <code>AppBundle</code> into smaller applications, in a monolithic repository</li>
  </ol>
</blockquote>

<p>There are many ways to organize <a href="http://symfony.com">Symfony</a> applications:</p>

<p>*</p>

<p>In this article we're going to see a progressive approach.</p>

<h2 id="starting-with-appbundle">Starting with AppBundle</h2>

<p>When creating an application, sticking to <code>AppBundle</code> is simple:</p>

<pre><code>.
├── app
│   └── config
│       ├── routings
│       └── services
├── bin
├── src
│   └── AppBundle
│       ├── Command
│       ├── Controller
│       ├── DependencyInjection
│       ├── EventListener
│       └── Service
├── var
│   ├── cache
│   └── logs
└── web
</code></pre>

<p>At first routings and services could be simply put in <code>app/config/services</code></p>


            <footer>
                                    <hr />
            </footer>
        </article>

        <footer>
            <nav class="row">
                <a class="button three columns" href="https://gnugat.github.io/about">About</a>
                <a class="button three columns" href="https://gnugat.github.io/">Articles</a>
                <a class="button three columns" href="https://gnugat.github.io/feed/atom.xml">RSS</a>
                <a class="button three columns" href="https://github.com/gnugat/gnugat.github.io/tree/master/_sculpin">Sources</a>
            </nav>
        </footer>
    </div>

    <script src="https://gnugat.github.io/js/highlight_9_0_0.min.js"></script>
    <script type="text/javascript">hljs.initHighlightingOnLoad();</script>
    <script type="text/javascript">
        var _gaq = _gaq || [];
        _gaq.push(['_setAccount', 'UA-47822314-1']);
        _gaq.push(['_trackPageview']);

        (function() {
            var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
            ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
        })();
    </script>
</body>
</html>
