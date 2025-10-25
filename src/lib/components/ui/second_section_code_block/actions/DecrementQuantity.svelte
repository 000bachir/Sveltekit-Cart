<pre class="h-full w-full flex items-center justify-center text-sm bg-gradient-to-r from-gray-900 to-gray-800 font-semibold">
    <code class="text-gray-200 leading-relaxed">
        <span class="text-green-400">DecrementQuantity</span> : (<span class="text-purple-400">id</span> : <span class="text-blue-400">string</span>) <span class="text-blue-400">=></span> &#123;
            <span class="text-blue-400">const</span> <span class="text-purple-400">currentCart</span> = <span class="text-green-400">get</span>(<span class="text-yellow-300">cartStore</span>)
            <span class="text-blue-400">const</span> <span class="text-purple-400">item</span> = <span class="text-purple-400">currentCart</span>.<span class="text-green-400">find</span>&#40;(<span class="text-purple-400">index</span>) => <span class="text-purple-400">index</span>.<span class="text-green-400">id</span> === <span class="text-purple-400">id</span>&#41;

            <span class="text-blue-400">if</span>(<span class="text-purple-400">item</span> && <span class="text-purple-400">item</span>?.<span class="text-green-400">quantity</span> === <span class="text-orange-400">1</span> )&#123;
                <span class="text-yellow-300">CartActions</span>.<span class="text-green-400">removeItem</span>(<span class="text-purple-400">id</span>)
            &#125;<span class="text-blue-400">else</span> &#123;
                <span class="text-yellow-300">cartStore</span>.<span class="text-green-400">update</span>&#40;(<span class="text-purple-400">cart</span>) => <span class="text-purple-400">cart</span>.<span class="text-green-400">map</span>&#40;(<span class="text-purple-400">item</span>)<span class="text-blue-400">=></span> <span class="text-purple-400">item</span>.<span class="text-green-400">id</span> === <span class="text-purple-400">id</span> ? &#123;...<span class="text-purple-400">item</span> , <span class="text-green-400">quantity</span> : <span class="text-purple-400">item</span>.<span class="text-green-400">quantity</span> - <span class="text-orange-400">1</span>&#125; : <span class="text-purple-400">item</span> &#41;&#41;
            &#125;
        &#125;,
    </code>
</pre>