---
title: During installation, Reflection Exception error
labels: Magento Commerce Cloud,Magento Commerce,installation,Redis,cache,Reflection,Exception,Error,how to
---

This article provides a solution for the Reflection Exception error, during installation.

<h2 id="details">Details</h2>

During the installation, a message similar to the following displays:

<pre><code class="language-php">[ERROR] exception 'ReflectionException' with message 'Class Magento\Framework\StoreManagerInterface does not exist' in /&lt;path>/lib/internal/Magento/Framework/Code/Reader/ClassReader.php</code></pre>

<h2 id="solution">Solution</h2>

Clear all directories and files under Magento's `` var `` subdirectory and install the Magento software again.

As the [Magento file system owner](https://devdocs.magento.com/guides/v2.3/install-gde/prereq/file-sys-perms-over.html) or as a user with `` root `` privileges, enter the following commands:

<pre><code class="language-bash">$ cd &lt;your Magento install directory>/var</code></pre>

<pre><code class="language-bash">$ rm -rf var/cache/* di/* generation/* page_cache/*</code></pre>

<h3 id="redis">Redis</h3>

If you use Redis and still get an error, clear the Redis cache as follows:

<pre><code class="language-bash">$ redis-cli FLUSHALL</code></pre>