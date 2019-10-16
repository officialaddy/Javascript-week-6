# Javascript-week-6
# COMP2112-Lab 6
## ES6+ features:
## 1).map function: EXPLAIN MAP FUNCTION I N YOUR WORDS HERE
# [More details about .map functions!] https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
![image of how the .map function works](LINK OF SCREENSHOT UPLOADED ON GITHUB)
 ```javascript  let tweets = [];

var btn = document.querySelector('#tweet');
btn.addEventListener('click', tweeting)

function tweeting(e) {
    e.preventDefault();

    // grab textarea element
    var textarea = document.querySelector('#exampleFormControlTextarea1');
    tweets.push({
        tweet: textarea.value
    });

    display(tweets);
}

function display(tweets) {
    const myArray = tweets.map(tweet => `


   <form>
          <div class="form-group">
       
            <hr />
            <div class="fb">

              <img id="avatar" src="https://avatars1.githubusercontent.com/u/41414116?v=4" alt="" />


              <textarea  class="form-control" id="exampleFormControlTextarea1" rows="1">${tweet.tweet}</textarea>

              <div class="imgGifPoll"></div>
            </div>
            <div class="fb">
              <section>
                <div id="inserts" class="btn-group mr-2">
                  <button type="button" class="btn btn-secondary mdi mdi-image-outline" aria-label="Insert image"></button>
                  <button type="button" class="btn btn-secondary mdi mdi-gif" aria-label="Insert gif"></button>
                  <button type="button" class="btn btn-secondary mdi mdi-poll" aria-label="Insert Poll" style=""></button>
                  <button type="button" class="btn btn-secondary mdi mdi-emoticon-happy-outline" aria-label="Insert emoji"></button>
                </div>
              </section>
             
            </div>
          </div>
        </form>`





    ).join('');
    console.log(myArray)

    const main = document.querySelector('main');
    main.innerHTML = myArray
}```
