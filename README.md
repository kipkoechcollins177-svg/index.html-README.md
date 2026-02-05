S C:\Users\Admin> $html = @"
>> <!DOCTYPE html>
>> <html>
>> <head>
>>     <title>Online Registration Form</title>
>>     <style>
>>         body { font-family: Arial; text-align: center; margin-top: 50px; }
>>         input { padding: 8px; margin: 5px; width: 250px; }
>>         button { padding: 10px 20px; margin-top: 10px; font-size: 16px; }
>>         #result { margin-top: 20px; color: green; font-weight: bold; }
>>     </style>
>> </head>
>> <body>
>>
>> <h1>Online Registration</h1>
>>
>> <input type='text' id='name' placeholder='Full Name'><br>
>> <input type='email' id='email' placeholder='Email'><br>
>> <input type='tel' id='phone' placeholder='Phone Number'><br>
>> <input type='password' id='password' placeholder='Password'><br>
>>
>> <button onclick='register()'>Register</button>
>>
>> <div id='result'></div>
>>
>> <script>
>> function register() {
>>     var name = document.getElementById('name').value;
>>     var email = document.getElementById('email').value;
>>     var phone = document.getElementById('phone').value;
>>     var password = document.getElementById('password').value;
>>     var result = document.getElementById('result');
>>
>>     if(name && email && phone && password){
>>         result.innerHTML = "Registration successful!<br>Name: " + name + "<br>Email: " + email;
>>     } else {
>>         result.innerHTML = "Please fill all fields!";
>>         result.style.color = 'red';
>>     }
>> }
>> </script>
>>
>> </body>
>> </html>
>> "@
PS C:\Users\Admin>
PS C:\Users\Admin> $html | Out-File "$env:USERPROFILE\Desktop\RegistrationForm.html"
PS C:\Users\Admin>
