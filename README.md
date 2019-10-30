# Brown-basketball
 
This is a project that the Brown Daily Herald's current editors wanted to look into after anecdotal knowledge of the team's drop off rate. The idea was to find out whether or not the rates of retention we're seeing today are historical abberations in the team's performance. Editors also wanted to compare and contrast the men's and women's teams in this regard.

On this website you can find jupyter notebooks that I used to scrape rosters from the Brown Athletics website (Brown athletes retention, Automating Selenium loop, etc). In the Final folder, you'll find nice clean data, a notebook I used to analyze the data I scraped, as well as csvs of retention rates (you can find the definition in the analysis notebook). I'm still working on refining that definition to account for study abroad and injury, but you can see a visualization of my findings so far here. (https://kpananjady.github.io/my-portfolio2/bball.html) 

My analyses notebooks have section headers to explain the code that follows, and function comments are inline. Questions that arise about my data over the course of my analysis are also inline. 

Data source: https://brownbears.com/index.aspx

Tools: Selenium, python, regex, pandas, DataWrapper, Flourish, d3. 

Codebook

Men's:

- Class Year: string, format: FR,SO,JR,SR
- Height: string, format: feet + inches
- Hometown: string, format: city, state / city, country  (if international)
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
- Team: string, Men's/Women's
= Roster: string, format: 20xx-yy





