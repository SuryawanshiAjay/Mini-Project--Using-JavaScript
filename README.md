<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        input,button
        {
            padding: 10px;
            height: 30px;
        }

        fieldset
        {
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <h1>local storage java-script</h1>
    <fieldset>
        <legend>insert data</legend>
        <input type="text" placeholder="enter key" id="inputkey">
        <input type="text" placeholder="enter value" id="inputvalue">
        <button type="button" id="btn">submit</button>
    </fieldset>
    <fieldset>
        <legend>local storage</legend>
        <div id="output"></div>
    </fieldset>

    <script>
        const inputkey=document.getElementById("inputkey");
        const inputvalue=document.getElementById("inputvalue");
        const btn=document.getElementById("btn");
        const output=document.getElementById("output");

        btn.onclick = function()
        {
            const key = inputkey.value;
            const value = inputvalue.value;

            if(key && value)
            {
                localStorage.setItem(key,value)
                location.reload();
                
            }
        }
            for(i=0;i<localStorage.length;i++)
                {
                    const key = localStorage.key(i);
                    const value = localStorage.getItem(key);
                    output.innerHTML+=`${key}: ${value} <br>`
                }
        
    </script>
</body>
</html>
