# LinkedinConnectionsHack
Linkedin Connections Hack...



```javascript

$(function() {
  //wait 2.5 sec so page is fully rendered
  setTimeout(function() {
    //get a random time period (1-4 sec) for this run
    var seed = parseInt(Math.random() * 3000) + 1000;
    //user loaded this run
    var users = $('.mn-pymk-list__card');

    users.each(function(index) {
      let name = $(this).find('.mn-person-info__name--card-layout').text();
      let connect = $(this).find('.button-secondary-small');
      setTimeout(function() {
      	//send invite
        connect.click();
        //send invite to who?
        console.log(name);
      }, seed * index)
    });

    setTimeout(function() {
      location.reload();
    }, seed * (users.length + 1));

  }, 2500);
});
```

### do not run this all day long, and you won't be caught by the LinkedIn bot.
