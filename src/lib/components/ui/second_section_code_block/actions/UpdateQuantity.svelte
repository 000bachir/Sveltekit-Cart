<pre class="text-sm  font-semibold  whitespace-pre">
    <code class="text-gray-200 leading-relaxed">
        <span class="text-green-400">UpdateQuantity</span> : (<span class="text-purple-400">id</span> : <span class="text-blue-400">string</span> , <span class="text-purple-400">quantity</span> : <span class="text-blue-400">number</span>) <span class="text-blue-400">=></span>&#123;
            <span class="text-blue-400">if</span>(<span class="text-purple-400">quantity</span> &le;=  <span class="text-orange-400">0</span>)&#123;
                <span class="text-yellow-300">CartActions</span>.<span class="text-green-400">removeItem</span>(<span class="text-purple-400">id</span>)
                <span class="text-blue-400">return</span>
            &#125;
            <span class="text-yellow-300">cartStore</span>.<span class="text-green-400">update</span>&#40;(<span class="text-purple-400">cart</span>)<span class="text-blue-400">=></span> <span class="text-purple-400">cart</span>.<span class="text-green-400">map</span>&#40;(<span class="text-purple-400">item</span>)<span class="text-blue-400">=></span> <span class="text-purple-400">item</span>.<span class="text-green-400">id</span> === <span class="text-purple-400">id</span> ? &#123;...<span class="text-purple-400">item</span> , <span class="text-purple-400">quantity</span>&#125; : <span class="text-purple-400">item</span> &#41;&#41;
        &#125;,
    </code>
</pre>