<template>
    <section class="w-full flex items-center justify-center h-full gap-4">
        <div class="w-full lg:w-2/3 flex flex-col h-full gap-4 pt-32">
            <div class="flex flex-col">
                <h1 class="text-2xl font-bold">Installing</h1>
                <span class="w-full h-1 bg-gray-400 bg-opacity-50 rounded-full mt-4 mb-4"></span>
                <span>First you need download <a href="https://nodejs.org/en/" target="_blank" class="text-blue-600 underline">node</a> and <a href="https://docs.npmjs.com/downloading-and-installing-node-js-and-npm" target="_blank" class="text-blue-600 underline">npm</a> or <a href="https://classic.yarnpkg.com/lang/en/docs/install/#windows-stable" target="_blank" class="text-blue-600 underline">yarn</a>.</span>
                <span>After downloading node, open console and type this:</span>
                <pre>
                    <code class="bg-gray-800 rounded-lg language-bash">
$ mkdir myapp

$ cd myapp
                    </code>
                </pre>
                <span>Create project:</span>
                <pre>
                    <code class="bg-gray-800 rounded-lg language-bash">
$ npm init -y

or

$ yarn init -y
                    </code>
                </pre>
                <span>Install cumpress:</span>
                <pre>
                    <code class="bg-gray-800 rounded-lg language-bash">
$ npm install cumpress
                    </code>
                </pre>
                If you want use yarn, you can type this:
                <pre>
                    <code class="bg-gray-800 rounded-lg language-bash">
$ yarn add cumpress
                    </code>
                </pre>
                And now you are ready to use cumpress! 🎉
                <pre>
                    <code class="bg-gray-800 rounded-lg" id="docs">
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
        </div>
        <script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/11.6.0/highlight.min.js"></script>
        <script>hljs.highlightAll();</script>
    </section>
</template>