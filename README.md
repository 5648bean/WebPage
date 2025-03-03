<html>
    <head>
        <meta charset="utf-8">
    </head>
    <body>
        <header>
            <h1>安全なパスワードを提供します。</h1>
        </header>
        <p>サイバーセキュリティの観点から、パスワードは類推しにくい文字・数字・記号などの組み合わせであることが望ましいと言われています。
                また、パスワードの使い回しはリスクが高いため、サービスごとに複雑なパスワードを作る必要があるとされます。
                このサイトでは、乱数を生成する機能を使って、ボタンを押すたびに毎回異なる１０桁の文字列を自動で生成し、安全なパスワードを提供します
        <button onclick="change1();">クリック</button>
        <p id="id2">ここに表示されます</p>

        <script>
            function change1(){
                var str = '';
                var shift = '!"#$%&\'()?';
                for (var i = 0; i < 10; i++) {
                    var n = Math.floor(Math.random()*10);
                    var m = Math.floor(Math.random()*2);
                    //document.write(m);
                    if (m==1){
                        var str=str+shift[i];
                    }
                    else{
                        var str=str+n;
                    }
                }
                document.getElementById("id2").innerHTML=str;
            }
    </script>

    </body>
</html>
