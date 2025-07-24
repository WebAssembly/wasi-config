<h1><a id="imports"></a>World imports</h1>
<ul>
<li>Imports:
<ul>
<li>interface <a href="#wasi_config_store_0_2_0_draft"><code>wasi:config/store@0.2.0-draft</code></a></li>
</ul>
</li>
</ul>
<h2><a id="wasi_config_store_0_2_0_draft"></a>Import interface wasi:config/store@0.2.0-draft</h2>
<p>An immutable configuration store.</p>
<hr />
<h3>Functions</h3>
<h4><a id="get"></a><code>get: func</code></h4>
<p>Gets a configuration value of type <code>string</code> associated with the <code>key</code>.</p>
<p>Returns <code>none</code> if the key does not exist.</p>
<p>This always returns the same value for any given key. Configuration
data does not change over the lifetime of the component instance.</p>
<h5>Params</h5>
<ul>
<li><a id="get.key"></a><code>key</code>: <code>string</code></li>
</ul>
<h5>Return values</h5>
<ul>
<li><a id="get.0"></a> option&lt;<code>string</code>&gt;</li>
</ul>
<h4><a id="get_all"></a><code>get-all: func</code></h4>
<p>Gets a list of configuration key-value pairs of type <code>string</code>.</p>
<p>This always returns the same data. Configuration data does not change
over the lifetime of the component instance.</p>
<h5>Return values</h5>
<ul>
<li><a id="get_all.0"></a> list&lt;(<code>string</code>, <code>string</code>)&gt;</li>
</ul>
