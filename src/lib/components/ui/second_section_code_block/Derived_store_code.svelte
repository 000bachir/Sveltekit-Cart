<pre class="overflow-x-auto  text-sm font-semibold  ">
    <code class="leading-relaxed text-black font-semibold ">
        <span class="font-semibold text-pink-600">export const</span> <span class="text-black ">cartTotal</span> = <span class="font-semibold text-yellow-700">derived</span>(<span class="text-black ">cartStore</span>, (<span class="text-yellow-300">$cart</span>) =&gt; &#123;
            <span class="font-semibold text-yellow-300">let</span> <span class="text-black ">ItemCount</span> = <span class="text-yellow-300">$cart</span>.<span class="font-semibold text-yellow-700">reduce</span>((<span class="text-black ">total</span>, <span class="text-black ">item</span>) =&gt; <span class="text-black ">total</span> + <span class="text-black ">item.quantity</span>, <span class="text-orange-600">0</span>);
            <span class="font-semibold text-yellow-300">let</span> <span class="text-black ">subtotal</span> = <span class="text-yellow-300">$cart</span>.<span class="font-semibold text-yellow-700">reduce</span>((<span class="text-black ">sum</span>, <span class="text-black ">item</span>) =&gt; <span class="text-black ">sum</span> + <span class="text-black ">item.product.price</span> * <span class="text-black ">item.quantity</span>, <span class="text-orange-600">0</span>);

            <span class="font-semibold text-pink-600">return</span> &#123;
                <span class="text-black ">ItemCount</span>,
                <span class="text-black ">subtotal</span>,
                <span class="text-black ">formattedSubtotal</span>: <span class="font-semibold text-pink-600">new</span> <span class="text-cyan-700">Intl.NumberFormat</span>(<span class="text-green-700">'en-US'</span>, &#123;
                    <span class="text-black ">style</span>: <span class="text-green-700">'currency'</span>,
                    <span class="text-black ">currency</span>: <span class="text-green-700">'USD'</span>
                }).<span class="font-semibold text-yellow-700">format</span>(<span class="text-black ">subtotal</span>)
            };
        });
    </code>
</pre>
