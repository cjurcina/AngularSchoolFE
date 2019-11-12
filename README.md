README file

Assignment 3

Date Created: 2019-11-10

Author: Chris Jurcina

Pre-requisites/installing

To run the app:

-Have angular installed on your machine. Download the project folder. run 
'ng serve' in the project folder. App should run on localhost:4200.

-Bluenose link: https://web.cs.dal.ca/~jurcina/csci3172/A3/a3v/ - This doesn't 
work, I have no idea how to make it work because we were only given a few slides
on simulating Bluenose that didn't help. Something like this needs a whole 
dedicated lab to be taught, which we didn't get. Regardless, the project folder 
is located on the link provided.



This app is built using Angular for the Framework, as required by the assignment
specifications.

Gitlab link: https://git.cs.dal.ca/jurcina/csci3172-a3


Design:

For this app, because of scope and time constraints, the app is designed very 
simply. It is kind of like a very simple version of the Best Buy website, and at 
the end of the day that is sort of the point, as Best Buy's website can be at 
time way too busy.

The app just implements the required pages for the assignment: A home page, a 
products page, a register page, and a login page.

The header is placed on all pages of the website. It features the company logo 
(Best Buy) and a simple navigation bar for home, products, register, and login. 
I did not add other navigation links like services because those pages wouldn't 
be developed for this assignment, so it would be pointless clutter to have them 
there. Also for scope and time, it was easier to just have one main products 
page rather than having dropdown navigations to tons of different pages, making 
it easier for me and for the markers to navigate. The naviagtion is always 
present, so a user can get back to previous states with ease.

The homepage implements mose of my improvements from my wireframe in assignment 
one. It gets rid of a ton of the clutter and unnessecary information that the 
original page contained. Now, it has just one large image for a deal of the 
week, and then below it top products that are sold and often bought by users. 
If development of this app was to continue, a user would be able to click a top 
product and be taken to the specific product page.

One of the biggest issues with Best Buy's website, which is something I came to 
realize even more when actually working on a new design, was that many pages of
the website are way too cluttered with elements. There are a ton of 
subcategories. On For the product page specifically, on Best Buy's actual 
website, you will actually find sections on other subcategories and selections 
before you actually get to your search results, which is really confusing and 
busy for the user. partly due to scope, and partly to just be an actual 
improvement, I just made one single products page. All it does is simply display
products and only the important information about the product in a neat, 
organized way on the product page.

Login is a simple web page. It simply provides a form for users to enter their 
username and password. Best Buy's login page already wasn't bad, but it had some
unessecary information that I cut. I also didn't like how you lost access to the
navigation bar when you are in the login page.

Register is basically the same as loogin, just with more fields for the user to 
input to 'create' a profile on the website. If development was to continue on 
this app this functionality would be fully fleshed out, customizing the website 
for the specific user. Like the whole website, this page is kept very simple for
easy understanding for the user.

The footer is straightforward, all it does is simulate some of the links that 
the origiunal footer gives on Best Buy's website. These links do not actually go
anywhere, they just simulate what the footer would look like. Again, I cut a lot
of the information on the footer that I found to be overly useless to the 
usability and user experience of the website.

The webpages are designed responively with styling that allows reshaping and 
resizing of the pages within reason.



Web Crawler:

As it stands currently, my developed web crawler would not run on my website.
It would require some modification of the Web Crawler code to get it to work. 
The crawler would have to be changed so that it targets my website, and some of 
the code would need to be changed so that it grabs text, rather than links, 
because most of my website is just text that is simulating where the links would
be on the webiste if it was fully fleshed out.


References:

Angular - Routing. (n.d.). Retrieved from https://angular.io/tutorial/toh-pt5. 
Used for the routing process in the application.

Code can be found in appModule, app-routing.module, HeaderComponent.

header.component.html

        <nav class="navbar navbar-light">
            <div class="container">
                 
                <a mat-button 
                routerLink="/home"
                routerLinkActive="active">Home</a>
                      
                <a mat-button
                routerLink="/products"
                routerLinkActive="active">Products</a>
                       
                <a mat-button
                routerLink="/register"
                routerLinkActive="active">Register</a>
                       
                <a mat-button
                routerLink="/login"
                routerLinkActive="active">Log In</a>
            </div>
        </nav>

app.module.ts:

import { AppRoutingModule, routingComponents } from './app-routing.module';

app-routing.module.ts:

const routes: Routes = [
  { path: "home", component: HomeComponent},
  { path: "products", component: ProductsComponent},
  { path: "register", component: RegisterComponent},
  { path: "login", component: LoginComponent},
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})



Acknowledgements:

TA's and the slides and lessons they provide.
Instructor for lectures on the material.

Notes/Feedback:

I feel like this assignment and its scope was too ambitious and involved. The
theory material is only lightly covered in class, and you can only cover so much
in labs. Labs should have been conducted by walking us through things in real 
time. Many of the requirements or tasks we needed to do for the assignment were 
not clearly taught or shown for most of us that have next to zero experience in 
Angular development. Even though a month is given for this assignment, it's the 
size of a project for many of my classes which would require much more than one 
month of time, even with the extension we were given. even professional 
developers would need more time tro develop a fully working front end and back 
end. Not to mention that it's weighted the same as a midterm or project. If the
assignment wasn't weighted so much, I wouldn't mind so much the extra scope, 
but as it is right now its a lot of stress for something that should not be that
stressful.


