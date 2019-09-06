What I Learned - Android
---

<p>As we move on developing software, we learn new skills and customize our IDE we love (or forced to work with sometimes) upon our needs to facilitate the daily development life.<br>
This repo will focus on Android development gathering my knowledge and the new stuff I learn to be a reference to me and open-sourced for anyone to help also.</p>
<h2 id="android-studio">Android Studio</h2>
<p>What if you have to move to a new machine or want to backup your settings/setup of AS that you have been installing for a quite time?<br>
There are many ways to do so:</p>
<ul>
<li><strong>Automatic:</strong> Using JB plugin <a href="https://plugins.jetbrains.com/plugin/7566-settings-repository">Settings Repository</a>, but unfortunately, it is not stable and has a lot of bad reviews and low rating.</li>
<li><strong>Semi-Manual:</strong> Export/Import them from the AS menu: <em>File</em> &gt; <em>Export Settings…</em>, then move the exported jar file to your new machine, then <em>File</em> &gt; <em>Import Settings…</em></li>
<li><strong>Manual:</strong> You can reference to this <a href="https://practical-start.blogspot.com/2016/12/changing-android-studio-settings.html">article</a> to do it totally manual.</li>
</ul>
<p><strong>AS From scratch:</strong><br>
Below is my list of plugin and tweaks to the AS to help me develop faster and more consistently:</p>
<ul>
<li></li>
</ul>
<h1 id="res">Res</h1>
<blockquote>
<p>Enable the use of support library for vector drawables</p>
</blockquote>
<p>Using vector drawables instead of PNGs in you app results in smaller apk file. But vector drawables was introduced in API 21, so to support it backward to API 7, enable support library for vector drawables to make use of them in your app as follows:</p>
<ol>
<li>In build.gradle (app level), add:</li>
</ol>
<pre><code>vectorDrawables.useSupportLibrary = true
</code></pre>
<ol start="2">
<li>Use app:srcCompat in the image tag in all your layout files:</li>
</ol>
<pre><code>app:srcCompat="@drawable/YOUR_RESOURCE_NAME"
</code></pre>
<ol start="3">
<li>You’ll also need to add the namespace to the root of the layout (like android and tools namespaces):</li>
</ol>
<pre><code>xmlns:app="http://schemas.android.com/apk/res-auto"
</code></pre>
<hr>

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTYyNTEwMDY1MV19
-->