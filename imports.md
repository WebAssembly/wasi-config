<h1><a id="imports"></a>World imports</h1>
<ul>
<li>Imports:
<ul>
<li>interface <a href="#wasi_config_store_0_2_0_draft"><code>wasi:config/store@0.2.0-draft</code></a></li>
</ul>
</li>
</ul>
<h2><a id="wasi_config_store_0_2_0_draft"></a>Import interface wasi:config/store@0.2.0-draft</h2>
<hr />
<h3>Types</h3>
<h4><a id="error"></a><code>variant error</code></h4>
<p>An error type that encapsulates the different errors that can occur fetching config</p>
<h5>Variant Cases</h5>
<ul>
<li>
<p><a id="error.upstream"></a><code>upstream</code>: <code>string</code></p>
<p>This indicates an error from an "upstream" config source.
As this could be almost _anything_ (such as Vault, Kubernetes ConfigMaps, KeyValue buckets, etc),
the error message is a string.
</li>
<li>
<p><a id="error.io"></a><code>io</code>: <code>string</code></p>
<p>This indicates an error from an I/O operation.
As this could be almost _anything_ (such as a file read, network connection, etc),
the error message is a string.
Depending on how this ends up being consumed,
we may consider moving this to use the `wasi:io/error` type instead.
For simplicity right now in supporting multiple implementations, it is being left as a string.
</li>
</ul>
<hr />
<h3>Functions</h3>
<h4><a id="get"></a><code>get: func</code></h4>
<p>Gets a single opaque config value set at the given key if it exists</p>
<h5>Params</h5>
<ul>
<li><a id="get.key"></a><code>key</code>: <code>string</code></li>
</ul>
<h5>Return values</h5>
<ul>
<li><a id="get.0"></a> result&lt;option&lt;<code>string</code>&gt;, <a href="#error"><a href="#error"><code>error</code></a></a>&gt;</li>
</ul>
<h4><a id="get_all"></a><code>get-all: func</code></h4>
<p>Gets a list of all set config data</p>
<h5>Return values</h5>
<ul>
<li><a id="get_all.0"></a> result&lt;list&lt;(<code>string</code>, <code>string</code>)&gt;, <a href="#error"><a href="#error"><code>error</code></a></a>&gt;</li>
</ul>
