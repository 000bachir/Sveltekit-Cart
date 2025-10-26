<pre class=" text-sm overflow-x-auto whitespace-pre font-semibold">
    <code class="text-gray-200 leading-relaxed">
        <span class="text-green-400">removeItem</span> : (<span class="text-purple-400">id</span> : <span class="text-blue-400">string</span>) <span class="text-blue-400">=></span> &#123;
            <span class="text-yellow-300">cartStore</span>.<span class="text-green-400">update</span>&#40;(<span class="text-purple-400">cart</span>)<span class="text-blue-400">=></span> <span class="text-purple-400">cart</span>.<span class="text-green-400">filter</span>&#40;(<span class="text-purple-400">item</span>)<span class="text-blue-400">=></span> <span class="text-purple-400">item</span>.<span class="text-green-400">id</span> !== <span class="text-purple-400">id</span>&#41;&#41;
        &#125;,
    </code>
</pre>