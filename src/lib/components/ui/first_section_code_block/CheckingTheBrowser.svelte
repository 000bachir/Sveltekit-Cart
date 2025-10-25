<pre class="overflow-x-auto bg-gradient-to-r from-gray-50 to-blue-50 p-6 text-sm font-semibold"><code
		class="leading-relaxed text-gray-800">
<span class="font-semibold text-red-600">const</span> StoredCart = browser ? localStorage.<span
			class="font-semibold text-red-600">getItem</span
		>(<span class="text-green-700">'cart'</span>) : <span class="text-gray-500">null</span>
<br /><span class="font-semibold text-blue-600">let</span> initialCart <span class="text-blue-600"
			>: CartProduct[]</span
		> = StoredCart ? JSON.<span class="font-semibold text-red-600">parse</span>(StoredCart) : []
            </code></pre>
