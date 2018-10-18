![larathon-banner](https://user-images.githubusercontent.com/19610753/47154697-eb77ca80-d2da-11e8-9e0d-aa2539d07ca8.jpg)
## Symfony Hackathon Starter  
  
 **Live Demo**: [https://symfony-hackathon-starter.herokuapp.com/](https://symfony-hackathon-starter.herokuapp.com/)
 A boilerplate for  **Symfony**  web applications.
 
If you have attended any hackathons in the past, then you know how much time it takes to   
get a project started: decide on what to build, pick a programming language,   
pick a web framework, pick a CSS framework. A while later, you might have an   
initial project up on GitHub and only then can other team members start contributing.  
 Or how about doing something as simple as Sign in with Facebook authentication?   
 You can spend hours on it if you are not familiar with how OAuth 2.0 works.  
  
  The aim and usage of this project goes beyond hackathon purposes only, Symfony Hackathon starter will definitely save any developer hours or even days of development time and can serve as a learning guide for web developers in general.
  
Describe Symfony as a set of reusable PHP components and a web framework here. And add more details  
 
 [Symfony](https://symfony.com) is an open-source PHP framework with an elegant structure and a reputation for being a suitable framework to kick-start any project irrespective of its size. As a set of reusable components, its flexibility, architecture, and high performance make it a top choice for building a highly complex enterprise application. 
  
Symfony Hackathon Starter is a boilerplate application developed with Symfony 4 to keep you ahead in hackathons.  
  
<h4 align="center">Modern Theme</h4>  
  
![](https://user-images.githubusercontent.com/19610753/47153649-1ad90800-d2d8-11e8-9f89-3164cfe11479.png)  
  
<h4 align="center">LOGIN</h4>  
  
![](https://user-images.githubusercontent.com/19610753/47153651-1b719e80-d2d8-11e8-90b1-f45cd9e08834.png)  
  
  
  <h4 align="center">REGISTER</h4>  
  
![](https://user-images.githubusercontent.com/19610753/47153652-1c0a3500-d2d8-11e8-85ff-ece0ec18d1e6.png)


Table of Contents  
-----------------  
  
- [Features](#features)  
- [Prerequisites](#prerequisites)  
- [Getting Started](#getting-started)  
- [Obtaining API Keys](#obtaining-api-keys)  
- [Project Structure](#project-structure)  
- [List of Packages](#list-of-packages)  
- [Useful Tools and Resources](#useful-tools-and-resources)  
- [Recommended Design Resources](#recommended-design-resources)  
- [Recommended Symfony Libraries](#recommended-symfony-libraries)  
- [Pro Tips](#pro-tips)  
- [FAQ](#faq)  
- [How It Works](#how-it-works-mini-guides)  
- [Symfony Best Practises](#symfony-best-practises)
- [Deployment](#deployment)  
- [Changelog](#changelog)  
- [Contributing](#contributing)  
- [License](#license)  
  
Features  
--------  
  
- **Local Authentication** using Email and Password  
- **OAuth 1.0a Authentication** via Twitter  
- **OAuth 2.0 Authentication** via Facebook, Google, GitHub, GitLab, LinkedIn, Auth0, Instagram  
- Flash notifications  
- MVC Project Structure  
- Bootstrap 4 
- Contact Form (powered by Gmail, Mailgun)  
- **Account Management**  
 - Profile Details  
 - Change Password  
 - Forgot Password  
 - Reset Password  
 - Delete Account  
 - CSRF protection  
  
Prerequisites  
-------------  
  
- [Mysql or Postgresql](https://www.mysql.com/ or http://www.postgresql.org/)  
- [PHP 7.1.3+](http://php.net/)  
- Command Line Tools  
 - <img src="http://deluge-torrent.org/images/apple-logo.gif" height="17">&nbsp;**Mac OS X:** [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) (or **OS X 10.9+**: `xcode-select --install`)  
 - <img src="http://dc942d419843af05523b-ff74ae13537a01be6cfec5927837dcfe.r14.cf1.rackcdn.com/wp-content/uploads/windows-8-50x50.jpg" height="17">&nbsp;**Windows:** [Visual Studio](https://www.visualstudio.com/products/visual-studio-community-vs)  
 - <img src="https://lh5.googleusercontent.com/-2YS1ceHWyys/AAAAAAAAAAI/AAAAAAAAAAc/0LCb_tsTvmU/s46-c-k/photo.jpg" height="17">&nbsp;**Ubuntu** / <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Logo_Linux_Mint.png" height="17">&nbsp;**Linux Mint:** `sudo apt-get install build-essential`  
 - <img src="http://i1-news.softpedia-static.com/images/extra/LINUX/small/slw218news1.png" height="17">&nbsp;**Fedora**: `sudo dnf groupinstall "Development Tools"`  
 - <img src="https://en.opensuse.org/images/b/be/Logo-geeko_head.png" height="17">&nbsp;**OpenSUSE:** `sudo zypper install --type pattern devel_basis`  
  
**Note:** If you are new to Symfony 4, I recommend to watch  
[Learn Symfony 4](https://symfonycasts.com/tracks/symfony), the official screencast for Symfony by Ryan Weaver and the SymfonyCasts crew. Alternatively,  
here is another great tutorial for building a project time tracker app for beginners/intermediate developers - [Let’s Build a Project Time Tracker with Symfony and VueJS](https://www.cloudways.com/blog/time-tracking-system-php-symfony-vue/).  
  
Getting Started  
---------------  
  
#### Via Cloning The Repository:  
  
  The easiest way to get started is to clone the repository:
```bash  
# Get the project  
git clone https://github.com/yemiwebby/symfony-hackathon-starter.git
```
  
#### Change directory  
```bash
cd symfony-hackathon-starter  
```

### Copy .env.dist to .env  
```
cp .env.dist .env  
```

#### Configure and add database credentials (in .env file)  

Open `.env` file and locate the database URL, then add your database credentials as shown here:

```
DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name
```

-   Change db_user to **YOUR_DATABASE_USERNAME**
-   Change db_password to **YOUR_DATABASE_PASSWORD**
-   db_name to **YOUR_DATABASE_NAME**
-   The database host by default is 127.0.0.1 and with a database port of 3306. You can leave this values as it is.
 
  
#### Install Composer dependencies  
```
$ composer install
```

#### Create Database

```bash
$ php bin/console doctrine:database:create
```

#### Update Schema

```bash
 $ php bin/console doctrine:schema:update --force
```

#### Run the application with

```bash
php bin/console server:run
```

![home-hac](https://user-images.githubusercontent.com/19610753/47153650-1b719e80-d2d8-11e8-9228-c7f785050039.png)
  

This starter pack includes the following APIs. You will need to obtain appropriate credentials like Client ID, Client secret, API key, or Username & Password by going through each provider and generate new credentials.  
  
* GitHub  
* Twitter  
* Auth0  
* LinkedIn    
  
Obtaining API Keys  
------------------  
  
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/1000px-Google_2015_logo.svg.png" width="200">  

- Visit [Google Cloud Console](https://cloud.google.com/console/project)  
- Click on the **Create Project** button  
- Enter *Project Name*, then click on **Create** button  
- Then click on *APIs & auth* in the sidebar and select *API* tab  
- Click on **Google+ API** under *Social APIs*, then click **Enable API**  
- Next, under *APIs & auth* in the sidebar click on *Credentials* tab  
- Click on **Create new Client ID** button  
- Select *Web Application* and click on **Configure Consent Screen**  
- Fill out the required fields then click on **Save**  
- In the *Create Client ID* modal dialog:  
 - **Application Type**: Web Application  
 - **Authorized Javascript origins**: http://localhost:8000  
 - **Authorized redirect URI**: http://localhost:8000/secured/login_google  
- Click on **Create Client ID** button  
- Copy and paste *Client ID* and *Client secret* keys into `.env`  
  
**Note:** When you ready to deploy to production don't forget to  
add your new url to *Authorized Javascript origins* and *Authorized redirect URI*,  
e.g. `http://my-awesome-app.herokuapp.com` and  
`http://my-awesome-app.herokuapp.com/secured/login_google` respectively.  
The same goes for other providers.  
  
<hr>  

<img src="https://github.global.ssl.fastly.net/images/modules/logos_page/GitHub-Logo.png" width="200">
  
- Go to [Account Settings](https://github.com/settings/profile)  
- Select **Applications** from the sidebar  
- Then inside **Developer applications** click on **Register new application**  
- Enter *Application Name* and *Homepage URL*  
- For *Authorization Callback URL*: http://localhost:8000/secured/login_github  
- Click **Register application**  
- Now copy and paste *Client ID* and *Client Secret* keys into `.env` file  
  
<hr>  
  
<img src="https://g.twimg.com/ios_homescreen_icon.png" width="90">  

- Sign in at [https://apps.twitter.com/](https://apps.twitter.com/)  
- Click **Create a new application**  
- Enter your application name, website and description  
- For **Callback URL**: http://127.0.0.1:8000/secured/login_twitter  
- Go to **Settings** tab  
- Under *Application Type* select **Read and Write** access  
- Check the box **Allow this application to be used to Sign in with Twitter**  
- Click **Update this Twitter's applications settings**  
- Copy and paste *Consumer Key* and *Consumer Secret* keys into `.env` file  
  
<hr>  
  
<img src="http://www.danpontefract.com/wp-content/uploads/2014/02/logo-linkedin.png" width="200">
  
- Sign in at [LinkedIn Developer Network](https://developer.linkedin.com/)  
- From the account name dropdown menu select **API Keys**  
 - *It may ask you to sign in once again*  
- Click **+ Add New Application** button  
- Fill out all the *required* fields  
 - **OAuth 2.0 Redirect URLs**: http://localhost:8000/secured/login_linkedin  
 - **JavaScript API Domains**: http://localhost:3000  
- For **Default Application Permissions** make sure at least the following is checked:  
 - `r_basicprofile`  
- Finish by clicking **Add Application** button  
- Copy and paste *API Key* and *Secret Key* keys into `.env` file  
 - *API Key* is your **clientID**  
 - *Secret Key* is your **clientSecret**  
  
<hr>  
  
<img src="https://raw.github.com/mailgun/media/master/Mailgun_Primary.png" width="200">  
- Go to http://www.mailgun.com  
- Sign up and add your *Domain Name*  
- From the domain overview, copy and paste the default SMTP *Login* and *Password* into `.env` file  
  
<hr>  
 
  
Project Structure  
-----------------  
  
| Name                                     | Description                                                  |  
| ----------------------------------       | ------------------------------------------------------------ |  
| **config**/app.php                       | Configuration for service providers and facades              |  
| **config**/auth.php                      | Configuration for password resets                            |  
| **config**/broadcasting.php              | Configuration for broadcasting                               |  
| **config**/cache.php                     | Configuration for cache generation and storage               |  
| **config**/cloudder.php                  | Configuration for cloudinary                                 |  
| **config**/compile.php                   | Configuration for compilation                                |  
| **config**/database.php                  | Configuration for database drivers                           |  
| **config**/filesystems.php               | Configuration for different file systems                     |  
| **config**/github.php                    | Configuration for github API                                 |  
| **config**/mail.php                      | Configuration for mails                                      |  
| **config**/queue.php                     | Configuration for queue                                      |  
| **config**/services.php                  | Configuration for several services like mailgun etc.         |  
| **config**/session.php                   | Configuration for sessions                                   |  
| **config**/ttwitter.php                  | Twitter API config file                                      |  
| **config**/twilio.php                    | Twilio API config file                                       |  
| **config**/view.php                      | Configuration for location of views and view cache           |  
| **controllers**/AccountController.php    | Controller for Account management                            |  
| **controllers**/AviaryController.php     | Controller for Aviary API functionality                      |  
| **controllers**/ClockworkController.php  | Controller for Clockwork API functionality                   |  
| **controllers**/ContactController.php    | Controller for Contact page                                  |  
| **controllers**/Controller.php           | BaseController                                               |  
| **controllers**/GithubController.php     | Controller for Github API functionality                      |  
| **controllers**/LastFmController.php     | Controller for LastFM API functionality                      |  
| **controllers**/LobController.php        | Controller for Lob API functionality.                        |  
| **controllers**/NytController.php        | Controller for New York Times API functionality              |  
| **controllers**/OauthController.php      | Controller for Oauthentication                               |  
| **controllers**/PaypalController.php     | Controller for Paypal API functionality                      |  
| **controllers**/SteamController.php      | Controller for Stream API functionality                      |  
| **controllers**/StripeController.php     | Controller for Stripe API functionality                      |  
| **controllers**/TwilioController.php     | Controller for Twilio API functionality                      |  
| **controllers**/TwitterController.php    | Controller for Twitter API functionality                     |  
| **controllers**/WebScrapingController.php| Controller for Web Scraping.                                 |  
| **controllers**/YahooController.php      | Controller for Yahoo API functionality                       |  
| **controllers**/user.js                  | Controller for user account management.                      |  
| **models**/User.php                      | Model for User.                                             |  
| **public**/                              | Static assets (fonts, css, js, img).                         |  
| **public**/**css**/main.css              | Main stylesheet for your app.                                |  
| **resources/views/account**/             | Templates for *login, password reset, signup, profile*.      |  
| **views/api**/                           | Templates for API Examples.                                  |  
| **views/partials**/alerts.blade.php      | Error, info and success flash notifications.                 |  
| **views/partials**/navbar.blade.php      | Navbar partial template.                                     |  
| **views**/layouts**/master.blade.php     | Base template.                                               |  
| **views**/apidashboard.blade.php         | API dashboard template.                                      |  
| **views**/contact.blade.php              | Contact page template.                                       |  
| **views**/welcome.blade.php              | Home page template.                                          |  
| .travis.yml                              | [Travis CI](https://travis-ci.org/) integration.             |  
| .env.example                             | Your API keys, tokens, passwords and database URI.           |  
| composer.json                            | File for loading all php packages.                           |  
| package.json                             | File for loading all necessary node modules.                 |  
| artisan                                  | File for enabling commands to run                            |  
  
  
List of Packages  
----------------  
  
| Package                         | Description                                                           |  
| ------------------------------- | --------------------------------------------------------------------- |  
| socialite                       | Sign-in with Facebook, Twitter and Github                             |  
| socialite providers             | Sign-in with LinkedIn, Instagram                                      |  
| cloudder                        | Upload images to Cloudinary                                           |  
| laravel github                  | Github API library                                                    |  
| clockwork                       | Clockwork SMS API library.                                            |  
| goutte                          | Scrape web pages using jQuery-style syntax.                           |  
| laravel framework               | PHP web framework                                                     |  
| twitter                         | Twitter API library                                                   |  
| twilio                          | Twilio API library                                                    |  
| lob-php                         | Lob API library                                                       |  
| lastfm-api-wrapper              | Lastfm API library                                                    |  
| phpunit                         | PHP testing library                                                   |  
| guzzlehttp                      | Simplified HTTP Request library                                       |  
  
  
Useful Tools and Resources  
--------------------------  
- [Laravel Daily](http://laraveldaily.com/) - Awesome laravel tips daily  
- [Laravel News](https://laravel-news.com/) - Laravel and PHP tutorials.  
- [Goodheads](http://goodheads.io) - Laravel, PHP and JS tutorials  
- [Favicon Generator](http://realfavicongenerator.net/) - Generate favicons for PC, Android, iOS, Windows 8.  
  
Recommended Design Resources  
----------------------------  
- [Code Guide](http://codeguide.co/) - Standards for developing flexible, durable, and sustainable HTML and CSS.  
- [Bootsnipp](http://bootsnipp.com/) - Code snippets for Bootstrap.  
- [UIBox](http://www.uibox.in) - Curated HTML, CSS, JS, UI components.  
- [Bootstrap Zero](https://www.bootstrapzero.com) - Free Bootstrap templates themes.  
- [Google Bootstrap](http://todc.github.io/todc-bootstrap/) - Google-styled theme for Bootstrap.  
- [Font Awesome Icons](http://fortawesome.github.io/Font-Awesome/icons/) - It's already part of the Hackathon Starter, so use this page as a reference.  
- [Colors](http://clrs.cc) - A nicer color palette for the web.  
- [Creative Button Styles](http://tympanus.net/Development/CreativeButtons/) - awesome button styles.  
- [Creative Link Effects](http://tympanus.net/Development/CreativeLinkEffects/) - Beautiful link effects in CSS.  
- [Medium Scroll Effect](http://codepen.io/andreasstorm/pen/pyjEh) - Fade in/out header background image as you scroll.  
- [GeoPattern](https://github.com/btmills/geopattern) - SVG background pattern generator.  
- [Trianglify](https://github.com/qrohlf/trianglify) - SVG low-poly background pattern generator.  
  
  
Recommended Laravel Libraries  
-----------------------------  
  
- [laravel-medialibrary](https://github.com/spatie/laravel-medialibrary) - Associated media files with your Eloquent models easily.  
- [laravel-emoji](https://github.com/unicodeveloper/laravel-emoji) - For using emojis in your app  
- [laravel-quotes](https://github.com/unicodeveloper/laravel-quotes) - For using all sorts of quotes especially DJKHALED in your app  
  
  
FAQ  
---  
  
### Why do I get `Token Mismatch Exception` when submitting a form?  
You need to add the following hidden input element to your form. This has been  
added in the existing codebase as part of the CSRF protection.  
  
```  
{!! csrf_field() !!}  
```  
  
  
### I get a whoops error when I deploy my app, why?  
Chances are you haven't generated the app key, so run `php artisan key:generate`.  
Chances are you haven't put your credentials in your .env file.  
  
How It Works (mini guides)  
--------------------------  
  
This section is intended for giving you a detailed explanation about  
how a particular functionality works. Maybe you are just curious about  
how it works, or maybe you are lost and confused while reading the code,  
I hope it provides some guidance to you.  
  
<hr>  
  
### How do flash messages work in this project?  
Flash messages allow you to display a message at the end of the request and access  
it on next request and only next request. For instance, on a failed login attempt, you would  
display an alert with some error message, but as soon as you refresh that page or visit a different  
page and come back to the login page, that error message will be gone. It is only displayed once.  
All flash messages are available in your views via laravel sessions.  
  
<hr>  
  
### How do I create a new page?  
A more correct way to be to say "How do I create a new route". The main file `routes.php` contains all the routes.  
Each route has a callback function associated with it. Sometimes you will see 3 or more arguments  
to routes. In cases like that, the first argument is still a URL string, while middle arguments  
are what's called middleware. Think of middleware as a door. If this door prevents you from  
continuing forward, you won't get to your callback function. One such example is a route that requires authentication.  
  
```php  
Route::get('/account', 'UserController@getAccount');  
```  
  
It always goes from left to right. A user visits `/account` page. Then `auth` middleware  
checks if you are authenticated:  
  
```php  
 Route::get('/account', [ 'uses' => 'AccountController@getAccountPage', 'as'   => 'account.dashboard', 'middleware' => ['auth']]);  
```  
  
If you are authenticated, you let this visitor pass through your "door" by calling `return $next($request);` in the auth middleware and if you are authenticated, you will be redirected to *Account Management* page, otherwise you will be redirected to *Login* page.  
  
Here is a typical workflow for adding new routes to your application. Let's say we are building  
a page that lists all books from database.  
  
**Step 1.** Start by defining a route.  
  
```php  
Route::get('/books', 'BookController@getBooks');  
```  
---  
  
**Step 2.** Create a new model `Book.php` inside the *app* directory. You can simply run `php artisan make:model Book`  
  
```php  
  
namespace App;  
  
class Book  
{  
 /** * The attributes that are mass assignable. * * @var array */ protected $fillable = [ 'name', 'isbn', ];}  
  
```  
  
**Step 3.** Create a migration file like so: `php artisan make:migration create_books_table`  
  
```php  
  
use Illuminate\Database\Schema\Blueprint;  
use Illuminate\Database\Migrations\Migration;  
  
class CreateBooksTable extends Migration  
{  
 /** * Run the migrations. * * @return void */ public function up() { Schema::create('books', function (Blueprint $table) { $table->increments('id'); $table->string('name'); $table->string('isbn'); $table->timestamps(); }); }  
 /** * Reverse the migrations. * * @return void */ public function down() { Schema::drop('books'); }}  
```  
  
**Step 4.** Create a new controller file called `BookController` inside the *app/Http/Controllers* directory. You can simply run `php artisan make:controller BookController`  
  
```php  
namespace App\Http\Controllers;  
  
use Illuminate\Http\Request;  
  
use App\Book;  
use App\Http\Requests;  
use App\Http\Controllers\Controller;  
  
class BookController extends Controller  
{  
 /** * Return all books * @return mixed */ public function getBooks() { $books = Book::all();  
 return view('books')->withBooks($books); }}  
```  
  
**Step 5.** Create `books.blade.php` template.  
```php  
@extends('layouts.master')  
  
@section('content')  
 <div class="main-container"> @include('layouts.partials.alerts')  
 <div class="page-header"> <h2><i style="color: #f00" class="fa fa-book"></i>All Books</h2> </div>  
 <ul> @foreach ($books as $book) <li> {{ $book->name }} </li> @endforeach </div> </div>@stop  
```  
  
That's it!  
<hr>  
  
Symfony Cheatsheet  
-------------------  
  
* [Symfony Cheatsheet](https://www.cheatography.com/mika56/cheat-sheets/symfony/)  


Symfony Best Practises
----------------------
* [Symfony Best Practises](https://symfony.com/doc/current/best_practices/index.html)  

  
Deployment  
----------  
  
Once you are ready to deploy your app, you will need to create an account with a cloud platform to host it. These are not the only choices, but they are my top  
picks. From my experience, **Heroku** is the easiest to get started with,  deployments and custom domain support on free accounts.  
  
### 1-Step Deployment with Heroku  
  
<img src="http://blog.exadel.com/wp-content/uploads/2013/10/heroku-Logo-1.jpg" width="200">  
- Download and install [Heroku Toolbelt](https://toolbelt.heroku.com/)  
- In terminal, run `heroku login` and enter your Heroku credentials  
- From *your app* directory run `heroku create`  
- Create a Procfile in your app root. All this file needs to contain is `web: vendor/bin/heroku-php-nginx public` or `web: vendor/bin/heroku-php-apache2 public` if you prefer to use nginx.  
- Run `heroku addons:add heroku-postgresql:dev  ` to add a Postgres database to your heroku app from your terminal  
- Lastly, do `git push heroku master`.  Done!  
- Run artisan commands on heroku like so `heroku run php artisan migrate`  
  
**Note:** To install Heroku add-ons your account must be verified.  
  
---  
  
- Finally, you can now push your code to OpenShift by running `git push -f openshift master`  
 - **Note:** The first time you run this command, you have to pass `-f` (force) flag because OpenShift creates a dummy server with the welcome page when you create a new Node.js app. Passing `-f` flag will override everything with your *Hackathon Starter* project repository. **Do not** run `git pull` as it will create unnecessary merge conflicts.  
- And you are done!  
  
<img src="https://upload.wikimedia.org/wikipedia/commons/f/ff/Windows_Azure_logo.png" width="200">  
  
- Login to [Windows Azure Management Portal](https://manage.windowsazure.com/)  
- Click the **+ NEW** button on the bottom left of the portal  
- Click **COMPUTE**, then **WEB APP**, then **QUICK CREATE**  
- Enter a name for **URL** and select the datacenter **REGION** for your web site  
- Click on **CREATE WEB APP** button  
- Once the web site status changes to *Running*, click on the name of the web site to access the Dashboard  
- At the bottom right of the Quickstart page, select **Set up a deployment from source control**  
- Select **Local Git repository** from the list, and then click the arrow  
- To enable Git publishing, Azure will ask you to create a user name and password  
- Once the Git repository is ready, you will be presented with a **GIT URL**  
- Inside your *Hackathon Starter* directory, run `git remote add azure [Azure Git URL]`  
- To push your changes simply run `git push azure master`  
 - **Note:** *You will be prompted for the password you created earlier*  
- On **Deployments** tab of your Windows Azure Web App, you will see the deployment history  
  
  
**Note:** Alternative directions, including how to setup the project with a DevOps pipeline are available at [http://ibm.biz/hackstart](http://ibm.biz/hackstart).  
A longer version of these instructions with screenshots is available at [http://ibm.biz/hackstart2](http://ibm.biz/hackstart2).  
Also, be sure to check out the [Jump-start your hackathon efforts with DevOps Services and Bluemix](https://www.youtube.com/watch?v=twvyqRnutss) video.  
  
## Contributing  
  
Thank you for considering contributing to Symfony Hackathon Starter. The contribution guide can be found in the [Contribution File](CONTRIBUTING.md)  
  
## Security Vulnerabilities  
  
If you discover a security vulnerability within Laravel Hackathon Starter, please send an e-mail to Olususi Oluyemi at yemiwebby@gmail.com. All security vulnerabilities will be promptly addressed.  
  
## Credits  
* [Prosper Otemuyiwa](https://github.com/unicodeveloper/laravel-hackathon-starter) - Larathon  
* [Sahat Yalkabov](https://github.com/sahat/hackathon-starter) - Awesome  
  
## How can I thank you?  
  
Why not star the github repo? I'd love the attention! Why not share the link for this repository on Twitter or HackerNews? Spread the word!  
  
Don't forget to [follow me on twitter](https://twitter.com/yemiwebby)!  
  
Thanks!  
Olususi Oluyemi.  
  
## License  
  
The MIT License (MIT). Please see [License File](LICENSE.md) for more information.