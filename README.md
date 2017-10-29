# LinkedinConnectionsHack
Linkedin Connections Hack...

1. add chrome extension `cjs` (add jQuery)
2. add the following code
3. goto https://www.linkedin.com/mynetwork/ 

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

		if(users.length > 0){
      setTimeout(function() {
        location.reload();
      }, seed * (users.length + 1));    
    }

  }, 2500);
});

```

### run only few times a day, then you won't be caught by the LinkedIn bot.
