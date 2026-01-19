# TaskManagerWebSite
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="/static/style.css">
</head>
<body>

<h2>Your Tasks</h2>

<form method="post">
<input name="task" placeholder="New Task" required>
<button>Add Task</button>
</form>

<ul>
{% for task in tasks %}
<li>
{{ task[1] }}
<a href="/delete/{{ task[0] }}">❌</a>
</li>
{% endfor %}
</ul>

<a href="/logout">Logout</a>

</body>
</html>


<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="/static/style.css">
</head>
<body>
<h2>Login</h2>
<form method="post">
<input type="email" name="email" placeholder="Email" required>
<input type="password" name="password" placeholder="Password" required>
<button>Login</button>
<a href="/register">Register</a>
</form>
</body>
</html>


<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="/static/style.css">
</head>
<body>
<h2>Register</h2>
<form method="post">
<input name="name" placeholder="Name" required>
<input type="email" name="email" placeholder="Email" required>
<input type="password" name="password" placeholder="Password" required>
<button>Register</button>
</form>
</body>
</html>


body{
    font-family: Arial;
    background:#f2f2f2;
    text-align:center;
}
form{
    background:white;
    padding:20px;
    width:300px;
    margin:auto;
}
input,button{
    width:100%;
    padding:10px;
    margin:5px 0;
}
