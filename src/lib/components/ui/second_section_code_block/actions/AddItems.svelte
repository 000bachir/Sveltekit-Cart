<pre class="text-sm font-semibold  overflow-x-auto whitespace-pre">
    <code class="text-gray-200 leading-relaxed">
        <span class="text-green-400">addItem</span> : (<span class="text-purple-400">item</span> : <span class="text-yellow-300">Omit</span>&#60;<span class="text-blue-400">CartProduct</span> , <span class="text-green-300">'quantity'</span>&#62; , <span class="text-purple-400">quantity</span> = <span class="text-orange-400">1</span>)<span class="text-blue-400">=></span>&#123;
            <span class="text-yellow-300">cartStore</span>.<span class="text-green-400">update</span>&#40;(<span class="text-purple-400">cart</span>)<span class="text-blue-400">=></span>&#123;
                <span class="text-blue-400">const</span> <span class="text-purple-400">existingItem</span> = <span class="text-purple-400">cart</span>.<span class="text-green-400">find</span>&#40;(<span class="text-purple-400">index</span>)<span class="text-blue-400">=></span> <span class="text-purple-400">index</span>.<span class="text-green-400">id</span> === <span class="text-purple-400">item</span>.<span class="text-green-400">id</span> &#41;

                <span class="text-blue-400">if</span> &#40;<span class="text-purple-400">existingItem</span>&#41;&#123;
                    <span class="text-blue-400">return</span> <span class="text-purple-400">cart</span>.<span class="text-green-400">map</span>&#40;(<span class="text-purple-400">index</span>)<span class="text-blue-400">=></span> <span class="text-purple-400">index</span>.<span class="text-green-400">id</span> === <span class="text-purple-400">item</span>.<span class="text-green-400">id</span> ? &#123;...<span class="text-purple-400">index</span> , <span class="text-green-400">quantity</span> : <span class="text-purple-400">index</span>.<span class="text-green-400">quantity</span> + <span class="text-purple-400">quantity</span>&#125; : <span class="text-purple-400">index</span> &#41;
                &#125;<span class="text-blue-400">else</span>&#123;
                    <span class="text-blue-400">return</span> [...<span class="text-purple-400">cart</span> , &#123;...<span class="text-purple-400">item</span> , <span class="text-purple-400">quantity</span>&#125;]
                &#125;
            &#125;&#41;
        &#125;,
    </code>
</pre>