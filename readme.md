Synopsis:

The website allows the user to search for bills passed in their area, find local Congressmen and senators, and get more information about politics and the voting process.

License:

The project has an Apache license, which means that preservation of the disclaimer and copyright notices is mandatory when reproducing or using the code. 

Code Example:

This code allows a user to enter their zip code and get their House and Senate representative based on the SunlightFoundation API.

<h1>Find your House and Senate representative</h1>
    <div class="form-group">
      <label for="usr">Enter your ZIP code:</label>
      <input type="text" class="form-control" id="usr">
    </div>
    <p id="invalid"></p>
    <button type="button" class="btn btn-default" onclick="getzip()">Submit</button>

    <p id="representative"></p>
    
    

    <script>
    function getzip () {
        var zip = document.getElementById("usr").value
        var xhr = new XMLHttpRequest();
        xhr.open("GET", "https://congress.api.sunlightfoundation.com//legislators/locate?zip=" + zip + "&apikey=6a668fb807334bbca5fee69cad4b1d96", false);
        xhr.send();
        console.log(xhr.status);
        console.log(xhr.statusText);

Motivation: 

We want to educate people about the voting process and give them unbiased resources to learn about legislature, candidates, and their representatives. We want politics to be accesible and easy to understand, so that everyone can cast an educated vote. We want to involve everyone in the workings of the government by giving them resources to contact their politicians or learn about political events in their area.


Installation:

Politicious is a website so users can openly access our site without downloading any additional apps or software. It is accessible on computer, tablet and mobile browsers.

API Reference:

For our website, we used two APIs-- Sunlight Congress and GovTrack. These databases allowed us to access information about Congress representatives and bills. The link to the Sunlight Congress API can be found here: https://sunlightlabs.github.io/congress/ and the link to the GovTrack API can be found here: https://www.govtrack.us/developers/api.

Contributors:

If you would like to contribute to our website, feel free to look through our code and contact one of the creators-- Amanda Chan, Marinn Cedillo or Anna Kondratyeva-- if you have any suggestions or additions. 