# README

Meteor 1.6.1.4 repo for reproducing issue with allocation bomb of fibers in Meteor 1.7+.

```
meteor npm install
meteor npm run start
```

Then open some browser tabs on `http://localhost:3000` and observe the server console output report the number of fibers created.

Opening 5+ tabs (and having them visible on-screen to prevent your browser from throttling JS) will cause much fewer fibers to be created than in the corresponding Meteor 1.8.0.1 version of this example ([here](https://github.com/ebbe-brandstrup/meteor-1.8-fibers-regression-reproduction)).

Used for https://github.com/meteor/meteor/issues/10359.
