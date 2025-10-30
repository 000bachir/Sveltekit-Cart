                <pre class=" h-full w-full flex items-center justify-center text-sm  bg-gradient-to-r from-gray-900 to-gray-800 font-semibold overflow-x-auto">
                    <code class="text-gray-200 leading-relaxed">
                        <span class="text-blue-400">if</span> &#40; <span class="text-purple-400">browser</span>&#41; &#123;
                            <span class="text-yellow-300">cartStore</span>.<span class="text-green-400">subscribe</span>&#40;&#40;<span class="text-purple-400">cart</span>&#41; <span class="text-blue-400">=&#62;</span> &#123;
                                <span class="text-yellow-300">localStorage</span>.<span class="text-green-400">setItem</span>&#40;<span class="text-green-300">&#39;cart&#39;</span>, <span class="text-yellow-300">JSON</span>.<span class="text-green-400">stringify</span>&#40;<span class="text-purple-400">cart</span>&#41;&#41;
                            &#125;&#41;
                        &#125;
                </code></pre>

