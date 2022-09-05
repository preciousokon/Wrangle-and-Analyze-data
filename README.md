# wrangle-and-analyze-data

Real-world data rarely comes clean. I used Python and its libraries, to gather data from a variety of sources and in a variety of formats, assesse its quality and tidiness, then provides it for easy Analysis. My wrangle effort is documented in a Jupyter Notebook and a separate write-up known as wrangle report.

The dataset I wrangled is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017.

I made use of Jypyter notebook, pandas and numpy libraries, I also imported requests, tweepy and json libraries into my working environment

## Dataset Used For Wrangling
I made use of Three Dataset which was later merged into a master dataset for this Wrangling procesws

* Enhanced Twitter Archive
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which was used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, tweets with ratings only have beenfiltered for (there are 2356).

* Additional Data via the Twitter API
Regarding the basic need of Twitter archives: retweet count and favorite count are two of the notable column omissions. Fortunately, this additional data can be gathered from Twitter's API. The project queries Twitter's API to gather this valuable data.

* Image Predictions File
Udacity ran every image in the WeRateDogs Twitter archive through a neural network that can classify breeds of dogs. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).

## Some Wrangling Efforts
* I first of all dropped rows that has retweets then proceeded in dropping the column of the retweet of retweeted_status_id, retweeted_status_user_id and retweeted_status_timestamp, using their tweet_ids. 

* I change the datatype in some column from interger to datetime and string

* I identified and cleaned 9 Data Quality issues and 2 data Tidiness issue

After cleaning I went on to merge the dataset into one dataset which I used for my Analysis and visualizations


