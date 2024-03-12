## This is my Code Structure Portfolio project 🔥
Here I will show examples of everything that I know: 📢📢📢
 
   ###### First of all I give an overview list of what I will show in this project:
        ✍️ Role & Permissions Management (Gates And Policies.)
        ✍️ Repository Design Pattern.
        ✍️ ChildClass Inheritance constructor and destructor.
        ✍️ Custom Service Provider.
        ✍️ Custom Middleware.
        ✍️ Helpers
        ✍️ Mail Sending
        ✍️ Laravel Queue / CornJob / Schdule
        ✍️ Custom Command
        ✍️ Event Listeners & Model Observer         
        ✍️ Eloquent ORM ( one-to-one , one-to-many and others)
        ✍️ Seeder & Factory
        ✍️ Request & Error Handaling.
        ✍️ Cache
        ✍️ Query Optimization. 
        ✍️ Security (Breeze).
        ✍️ Multi-languages.(localization)
        ✍️ GuzzleHttp
        ✍️ Accessor-Mutators
        ✍️ Livewire
## Alright, let's get started. 🎉

🟢Example: Role & Permissions Management (Gates), Custom Middleware <br>

##### Open the file: /App/Http/Middleware/AuthGateMiddleware; (note: this is my custom middleware)

                 Gate::define($permission->slug, function(User $user) use ($permission){
                    return $user->hasPermission($permission->slug);
                });
this function where I define all gates for role permissions; 

##### Then, Open the file: /App/Http/Controller/RoleController;
      
    public function index()
    {
        Gate::authorize('role.index');
        $roles = $this->role->all();
        return view('backend.role.index', compact('roles'));
    }
in here, I verify permission by using "Gate::authorize" function;

🟢Example:  Repository Design Pattern, child-class, Inheritance, implements, constructor and destructor function.
    

🟢Example: Email Sending, Event-Listener:

