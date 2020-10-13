---
title: 'Swore Declaration'
published: true
date: '09-10-2020 20:56'
taxonomy:
    category:
        - blog
    tag:
        - Java
        - Application
        - Quarkus
hide_git_sync_repo_link: false
blog_url: /blog
show_sidebar: true
show_breadcrumbs: true
show_pagination: true
hide_from_post_list: false
feed:
    limit: 10
---

It's all start with a friend that has some squashs court's and during covid-19, every people how enters to the club need to sign a swore declaration in paper with a pen.  
Whats the consequence of that, we need to take pen to sign a paper.... WHAT? The idea is to get ride off the paper and touching things!  
So we planned to have a QR code at the entrance of the club and when you enter, with your cellphone scan that and sign digitally the questions of the swore declaration.  
That a "simple" app, so I decided to develop on [Quarkus](https://quarkus.io/)!  
The base of the app requirements has:  
1.- the Entity (the courts of squash). 
2.- the User that is accessing to the club, that must register on it.  
3.- And the Swore Declaration to be signed by the User at the Entity.  
  
I have made the app on 4 days, and use _KISS_ (Keep It Simple Stupid) as a premise.  The Entities and the Users are store on a database, and the Swore Declaration is a static form that have some questions to answer. The login, no exists, is just a registration form with fields that the Swore Declaration needs like Name, surname and location.  

So thas works! testing and deploying. Greats. Everyone is happy.

===

## Going Further
How ever, I decide to go further. 
First, a login to have Users, Entities/Space and Declaration to admin them.  
A dashboard to control who person access to the club and which Declaration have been signed.   
Between times, we can check how users are related on the court.  
We could made our own Sworn Declarations.  
Manage the Entity, defining properties and Spaces. Spaces are the places/courts where people stand.  

So the application start growing with some interesting things.  
The technology using its [ElephantSQL](https://www.elephantsql.com/) to test [Postgres](https://www.postgresql.org/) over the net.  
This is a classy java web app with RESTEasy/JAX-RS protocol. I said classic because I came from JavaEE with Jboss, so that why.  

## Looking Beyond  
What could I made, make it [Reactive](https://quarkus.io/guides/getting-started-reactive). Quarkus brings reactivness in the all the aspects of the life cycle; in database, backend and front.  
Use Panache, for the repository.  
Make API first.  
A new frontend, maybe add [Svelte](https://svelte.dev/) (you are invited to colaborate) o [https://quasar.dev/](https://quasar.dev/) (how I said, 2Qute to Be Real)  
Add mail support to connect users.  
Made Test to verify the functionality of the app.  

To learn about Quarkus.io visit [https://quarkus.io/](https://quarkus.io/)!  

You could access github repository in <i class="fa fa-github fa-2x"></i>  [https://github.com/wuiler/declaracion/](https://github.com/wuiler/declaracion/)
