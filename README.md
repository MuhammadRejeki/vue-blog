## Project setup

```
npm install
npm run serve
npm run build
```

## What do you get from this tutorial !

```
Learn about Composition API
There is setup() , created(), then mounted()
setup = first running before all
created = after setup
mounted = after the html load, then mounted automatically running

Template refs (import from vue)
refs can make variable with dom element dan bisa membuat reactive variable

```

## Notes

```
All variable in setup() example you define with "Let" command it will be not reactive variable (variable tetap tidak bisa diubah)

Sedangkan kalau nulis variable property di data() itu akan menjadi reactive variable

Pada dasarnya variable yang ditulis di setup() bersifat tetap, namun bisa dijadikan berubah kalau variable nya menjadi tipe refs / reactive, "Generally a lot of people using refs than reactive".


```
