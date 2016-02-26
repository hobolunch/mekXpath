# SEARCHER URL:
http://knowem.com/checkusernames.php?u=******

# FRAMEWORK
# The Group of "Popular" social media sites.
.//*[@id='listPopularProfiles']

# This will capture title of each Social Media Site
.//*[@id='listPopularProfiles']/div/@id

# This is the xPath to a distinct platform within "Popular" social media sites.
.//*[@id='listPopularProfiles']/[@id='Blogger']

# TITLE
.//*[@id='Blogger']/@bt-xtitle

# AVAILABILITY
# Unavailable - this will print out all nodes that contain "Available" which they are not.
.//*[@id='listPopularProfiles']/div/span/span/text()

# Available - this will print out all nodes that contain "Available" which they are not.
.//*[@id='listPopularProfiles']/div/span/span/a/text()

# Distinct page for each Social Media site, Xpath might need a "text" field
.//*[@id='Blogger']/a/@href


# WORKER URL:
http://knowem.com/websites/******

# Social Media "Description" of Site:
.//*[@id='networkLeft']/div[2]/p/text()

# Words associated with Social Media Site:
.//*[@id='siteTags']/p/a/text()

# Scoring - First 'div' is what changes, [1] = 'Alexa', [2] = 'Google Page Rank'
# Alexa (Returns Node= 'style="width: 97.40%;"'
.//*[@id='scoresLeft']/div[1]/div[2]/div/div/@style
# Google Page Rank
.//*[@id='scoresLeft']/div[2]/div[2]/div/div/@style
