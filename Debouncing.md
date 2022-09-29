Debouncing is a practice in software development which makes sure that certain heavy tasks - such as searcing a query, sending HTTP requests - don't get fired so often, so the [[Performance]] can be improved. 

We can use setTimeout method to delay the function that is fired too many times.

Ex:
``` JS
let filterTimeout

const doCityFilter = query => {
  clearTimeout(filterTimeout)
  if (!query) return setFilteredCities([])

  filterTimeout = setTimeout(() => {
    console.log('====>', query)
    setFilteredCities(citiesArray.filter(
      city => city.toLowerCase().includes(query.toLowerCase())
    ))
  }, 500)
}
```

❗️ Using clearTimeout method is crucial, because we need to cancel the previous setTimeout method whenever we hit a new key, so we'll end up calling the filter function for the just last key. If we don't clear the previous timeouts, we still call the filter function for each key, just delaying the calls for 500 miliseconds.

⭐️  We can also do the clearing with the cleanup function of the [[UseEffect]] hook.

https://blog.logrocket.com/how-and-when-to-debounce-or-throttle-in-react/