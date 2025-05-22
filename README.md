### **Goal:**
- To predict song recommendations from user music preferences.
- To model arbitrary listening/streaming habits.
- To take advantage of the [wrappify](https://github.com/lukavuko/wrappify) library for seamless EDA in R markdown.

### **Current state**
- [x] Created functions using the Spotify API for rapidly extracting audio features and genre information from a user's streaming history and library. 
- [x] Extracted audio features and genre information from 2 sets of streaming and library data.
- [x] Created functions for retreiving top 100 genres and songs in user streaming data.
- [x] Visualize when users listen to music during the day and year (add week as well)
- [x] Visualize if audio features of listened music changes throughout the day or week.
- [ ] Engineer a feature for liked vs disliked songs as a predictor (ie. listening time)
- [ ] Exploring genre latent space (audio features) with which we may be able to cluster music taste sentiments (THIS IS REALLY HARD SURPRISINGLY). So far:
  - [x] Principal component analysis on audio features to assess if music clusters by sentiment (Result: no obvious clusters)
  - [x] Principal component analysis on average genre audio features to assess if genres cluster by sentiment (Result: no obvious clusters)
  - [x] Group specific genres into their greater categories to reduce the number of genre classes
  - [x] Using random forest to explore audio features as genre predictors for a dozen or so overarching genres (this worked with roughly ~86% accuracy but I'm sure we can still do better)
- [ ] Modeling streaming tendencies for audiofeatures (what time of day do they listen to what kind of music? Can certain recommendations be tailored to specific times of day?)
- [ ] Predicting genre recommendations based on recent trends in audio features.

### **Screenshots**

**Functions to fetch song metadata and determine top songs/genres by streams/listening time:**

![image](https://github.com/user-attachments/assets/52fc9f3f-f3aa-4d34-885c-e8db7f9a41ea)

![image](https://github.com/user-attachments/assets/a1f24a30-32f7-40f8-890b-eba70c7cc6d3)

**Spline models for playtime by time of year, hour of the day, day of the week**

*Note: summer months --> tree planting --> lots of music straming*
![image](https://github.com/user-attachments/assets/12bca098-15a3-4473-a501-e279e05a365a)

![image](https://github.com/user-attachments/assets/061545a4-4ac2-4191-a75e-3e492585e97d)

![image](https://github.com/user-attachments/assets/6fe4802f-6a69-411b-b4f2-3a711f9eb0bb)


Given this project is a work in progress, much of the current work was just a fun little EDA...
