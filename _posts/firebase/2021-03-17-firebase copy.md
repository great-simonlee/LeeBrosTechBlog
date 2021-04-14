---
layout: post
title: Firebase
categories: firebase lecture
author: Simon Lee
permalink: /:categories/:title
---

<strong>[Firebase Official Website][firebase]</strong>

## 12. SDK (Software Development Kit)

`yarn add react-router-dom`

<strong>[React Router Official Website][react-router]</strong>

One important thing to note is that a `<Route path>` matches the beginning of the URL, not the whole thing. So a `<Route path="/">` will always match the URL. Because of this, we typically put this `<Route>` last in our `<Switch>`. Another possible solution is to use `<Route exact path="/">` which does match the entire URL.

<br>
<br>
<br>

## 13. How to use

In the `app.js` file, React Router should be imported first as below.
{% highlight javascript%}
import { BrowserRouter, Link, Route, Switch } from 'react-router-dom';
{% endhighlight %}

In the return area, the links can be added as follows.
{% highlight javascript %}

<BrowserRouter>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/profile">Profile</Link>
  </nav>
  <Switch>
    <Route path={["/", "/home"]} exact>
      <Home />
    </Route>
    <Route path="/profile">
      <Profile />
    </Route>
  </Switch>
</BrowserRouter>
{% endhighlight %}

<br>
<br>
<br>

## 14. Anchor/Button

In the Home.jsx

{% highlight javascript %}
import React from 'react';
import { useHistory } from 'react-router';

const Home = (props) => {
const history = useHistory();
return (<>

<h1>Home</h1>
<button onClick={ () => {history.push('/profile')} }>
Go to Profile</button>

</>
)
};
{% endhighlight %}

In the Profile.jsx

{% highlight javascript %}
import React from 'react';
import { useHistory } from 'react-router';

const Profile = (props) => {
const history = useHistory();
return (<>

<h1>Profile</h1>
<button onClick={ () => {history.push('/Home')} }>
Go to Home</button>

</>
)
};
{% endhighlight %}

<br>
<br>
<br>

## 15. Offial Website

<strong>[React Router Official Website][react-router]</strong>

[firebase]: https://firebase.google.com/

<br>
<br>
<br>
