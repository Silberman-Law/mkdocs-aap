# Home

<!--
For full documentation visit [mkdocs.org](https://www.mkdocs.org).
-->

### About
This is the about section
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Users
Users are defined as people with restricted access to the application based on roles.

### Login/Logout
``` py title='login function'
public function login($arg_username, $arg_password) {
    if($arg_username == "") {
        return array('status'=>'2500', 'message'=>'Username Required', 'data'=>array()); 
    }
    if($arg_password == "") {
        return array('status'=>'2500', 'message'=>'Password Required', 'data'=>array()); 
    }
    $username = $arg_username;
    $password = $arg_password;
    return array('status'=>'200', 'message'=>'All good', 'data'=>array());
}
```

### Image
![](images/example.jpg)
