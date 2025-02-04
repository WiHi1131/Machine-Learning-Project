# Data Origins
Data was gathered from the  <a href = "https://developer.riotgames.com/">Riot Games Developer API</a>. This is the place to procure the most current data on both TFT matches and players. Using code found within the Data_Gathering_API notebook in my repository, I first retrieved all summoner ID's within the Challenger tier, or highest rated players in the game at the time of data retrieval. I then used various API GET methods to first find PUUID's from the encrypted summoner ID's, then use these PUUID's to get 10 matches per PUUID (or the 10 most recent matches for each Challenger player). I made sure to remove duplicate matches from my match id's and then finally retrieved all match data using these match id's. After data retrieval was completed, I had almost 1500 matches in a large .json file (so large it cannot be uploaded to Github). I ran into various roadblocks trying to clean and process this data further. I was able to separate around 90 games from the dataset that belonged to TFT Set 4, a different patch of the game with different units and mechanics than the 'current' set, Set 13, and place these into their own separate .json files. The coding environment I was using to clean and process these datasets crashed upon attempting to clean further. I will need to resolve these processing issues as I continue with this project. For now, I do not have any cleaned or processed data or any visualizations to show. Below are some images of the content in the match data .json file, as well as the code I used to generate this file: 

<div>
  <img src = "images/code_1.png" title = "Code Used to Define API Key and retrieve Summoner ID's from Challenger Players" alt = "Summoner ID Code">
  <div>
    <p>
      <b>This code was used to define my API Key and Header information, as well as the url for the first GET Request to retrieve Summoner ID information. Note the API Key has been deleted for privacy reasons</b>
    </p>
  </div>
</div>

<div>
  <img src = "images/CAPTURE.png" title = "Code Used for Second and Third GET Requests" alt = "2nd and 3rd GET Request Code">
  <div>
    <p>
      <b>This code was used to loop through the encrypted Summoner ID list and retrieve PUUID information, firstly. PUUID information then was used to grab each Challenger Player's most recent 10 matches by IDs</b>
    </p>
  </div>
</div>

<div>
  <img src = "images/code_3.png" title = "Code used to get Match information" alt = "Match information Get Code">
  <div>
    <p>
      <b>First, match ID's were first filtered for any duplicates. Then, match ID's were used in a GET request to get all match information and store it into a JSON file. Note that using time.sleep(1) was necessary to ensure rate limits in the API were preserved - even so retrieving this massive amount of data took over 30 minutes</b>
    </p>
  </div>
</div>

<div>
  <img src = "images/code_4.png" title = "Initial Cleaning Code" alt = "Cleaning Code">
  <div>
    <p>
      <b>This code was first used to separate the TFT match information by set (4 or 13), since different sets contain different units and mechanics. After this, an attempt was made to use the bottom cell to try and separate data by game type (ranked, casual, or other types), but the coding environment crashed during runtime.</b>
    </p>
  </div>
</div>


