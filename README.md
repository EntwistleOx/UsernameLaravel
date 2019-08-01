# Campo Username en Laravel

Al crear el auth scattfolding basico de laravel, por defecto crea el modelo users con campos email y password, en caso de querer cambiar email a username se hace lo siguiente:

En el archivo 'rutaproyecto\app\Http\Controllers\Auth\LoginController.php' agregar:
```
public function username()
{
  return 'username'; //or return the field which you want to use.
}
```
Modificamos el archivo de migracion 'rutaproyecto\database\migrations\0000_00_00_000000_create_users_table.php':
```
$table->string('username')->unique();
```
Editamos y cambiamos campo email por username en el template 'rutaproyecto\resources\views\auth\login.blade.php'.
