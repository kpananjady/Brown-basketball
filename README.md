# Brown-basketball
 
This is a project that the Brown Daily Herald's editors wanted to look into after anecdotal knowledge of the team's drop off rate. The idea was to find out whether or not the rates of retention we're seeing today are historical abberations in the team's performance. Editors also wanted to compare and contrast the men's and women's teams in this regard. It formed the basis for a quick numeracy training I did with the staff of the 129th editorial board.

On this website you can find jupyter notebooks that I used to scrape rosters from the Brown Athletics website (Brown athletes retention, Automating Selenium loop, etc). In the Final folder, you'll find nice clean data, a notebook I used to analyze the data I scraped, as well as csvs of retention/attrition rates. 
___
At the moment, the definition of attrition is simple: (number of people who left the team from one year to the next / the number of people who were not seniors on the team) * 100. You might find that this needs to be refined; see the note below.
___

My analyses notebooks have section headers to explain the code that follows, and function comments are inline. Questions that arise about my data over the course of my analysis are also inline. 

I've included some screenshots of basic viz to help with leads, etc. Links to the original Datawrapper projects are available in the text file links.rtf.

Data source: https://brownbears.com/index.aspx

Tools: Selenium, python, regex, pandas, DataWrapper. 

Codebook

Men's:

- Class Year: string, format: FR,SO,JR,SR
- Height: string, format: feet + inches
- Hometown: string, format: city, state (abbr.) / city, country  (if international)
- Name: string, format: FIRST LAST NAME
- Number: float, format: d.0
- Position: string, format: G/F/C
- School: string
- Weight: float, format: pounds
- Team: string, Men's/Women's
- Roster: string, format: 20xx-yy

Women's

- Class Year: string, format: FR,SO,JR,SR,RS (red-shirt)
- Height: string, format: feet + inches
- Hometown: string, format: city, state / city, country  (if international)
- Name: string, format: FIRST LAST NAME
- Number: float, format: d.0
- Position: string, format: GUARD,FORWARD,CENTER,GUARD/FORWARD
- School: string
- Team: string, Men's/Women's
- Roster: string, format: 20xx-yy

Here's a caveat to this analysis that you should definitely read!
Note about red-shirts: They have the potential to complicate these findings. For starters, only the women's team uses them, and it uses them only in 2009-10 data. Some people classified as red-shirts reappear with different class years in later data. The reason this is annoying is because of the way I define the population eligible to stay on for another year, i.e. anyone who is not a senior. 

In the absence of a RS designation, people could be listed with the same class year in consecutive years. If people start being listed as seniors multiple times in consecutive years, that messes with my definition of an eligible population and therefore any estimation of a retention/attrition rate that I can come up with. (I point out examples of this in the men's analysis notebook.) One of the first orders of business is going to be to understand this dataset from the people who maintain it and understand why they use RS or don't use it. Time to go bug Brown Athletics!



