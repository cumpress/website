<template>
  <div class="w-full h-full">
    <section class="w-full flex items-center justify-center h-full gap-4">
        <div class="w-full lg:w-2/3 flex flex-col items-center justify-center h-full gap-4">
            <h1 class="text-4xl font-bold">Cumpress</h1>
            <span>Minimalist backend framework.</span>
            <div>
                <a class="trans-btn" href="#docs">Quick start.</a>
                <nuxt-link class="trans-btn" to="/docs">Docs.</nuxt-link>
            </div>
            <a href="#docs" class="arrow"></a>
        </div>
    </section>
    <section class="w-full flex items-center justify-center h-full">
        <div class="w-full lg:w-2/3 flex flex-col items-center justify-center h-full">
            <h1>Quick start.</h1>
            <pre id="docs" class="rounded-lg w-full">
                <code class="rounded-lg bg-gray-800 w-full">
const cumpress = require('cumpress');

//add routers
require('./routes/IndexRouter');

//set and get settings.
//Cumpress uses morgan.
cumpress.set("logger",true);
//Serve files.
cumpress.set("static_dir","public");

//Router example.
cumpress.use('/','GET',async(req,res) => {
    //Cumpress use emejs template engine.
    res.status(200).render('views/index.eme',[{name:'title',value:'Cumpress.'}]);
});

cumpress.use('/','POST',(req,res) => {
    //req.body = post data
    res.status(200).json(req.body);
});

//Listen app.
cumpress.listen(3000);
                </code>
            </pre>
        </div>
    </section>
    <script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/11.6.0/highlight.min.js"></script>
    <script>hljs.highlightAll();</script>
  </div>
</template>

<script>
export default {
  name: 'index'
}
</script>
