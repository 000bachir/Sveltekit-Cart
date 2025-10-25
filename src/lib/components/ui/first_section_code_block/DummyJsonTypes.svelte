<pre class=" text-sm text-zinc-100">
    <code id="language-ts" class="leading-relaxed font-semibold">
        <span style="color: #569cd6">export</span> <span style="color: #569cd6">type</span> <span style="color: #4ec9b8">Product</span> = &#123;
            <span style="color: #9cdcfe">id</span>: <span style="color: #569cd6">number</span>;
            <span style="color: #9cdcfe">title</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">description</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">category</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">price</span>: <span style="color: #569cd6">number</span>;
            <span style="color: #9cdcfe">discountPercentage</span>: <span style="color: #569cd6">number</span>;
            <span style="color: #9cdcfe">rating</span>: <span style="color: #569cd6">number</span>;
            <span style="color: #9cdcfe">stock</span>: <span style="color: #569cd6">number</span>;
            <span style="color: #9cdcfe">tags</span>: <span style="color: #569cd6">string</span>[];
            <span style="color: #9cdcfe">brand</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">sku</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">weight</span>: <span style="color: #569cd6">number</span>;
            <span style="color: #9cdcfe">dimensions</span>: <span style="color: #4ec9b8">Dimensions</span>;
            <span style="color: #9cdcfe">warrantyInformation</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">shippingInformation</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">availabilityStatus</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">reviews</span>: <span style="color: #4ec9b8">Review</span>[];
            <span style="color: #9cdcfe">returnPolicy</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">minimumOrderQuantity</span>: <span style="color: #569cd6">number</span>;
            <span style="color: #9cdcfe">meta</span>: <span style="color: #4ec9b8">Meta</span>;
            <span style="color: #9cdcfe">thumbnail</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">images</span>: <span style="color: #569cd6">string</span>[];
        &#125;
            <span style="color: #569cd6">export</span> <span style="color: #569cd6">type</span> <span style="color: #4ec9b8">CartProduct</span> = &#123;
            <span style="color: #9cdcfe">id</span>: <span style="color: #569cd6">string</span>;
            <span style="color: #9cdcfe">product</span>: <span style="color: #4ec9b8">Product</span>;
            <span style="color: #9cdcfe">quantity</span>: <span style="color: #569cd6">number</span>;
        &#125;
    </code>
</pre>