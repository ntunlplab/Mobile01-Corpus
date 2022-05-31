# Mobile01 Corpus
Introduction
Datasets are indispensable for the study of opinion spam/spammer detection. However, to prepare such a kind of dataset is more difficult than that for the other types of spam detection tasks such as email spams and web spams due to the subtle nature of opinion spams. This website provides a dataset for a real case, Samsung probed in Taiwan over ‘fake web reviews’, reported by BBC on 16 April 2013. It can be used to study the behaviors of opinion spammers, their interactions in terms of first posts and replies, and the detection tasks.

# Data source
This dataset contains threads and posts from the Samsung board on Mobile01 during Jan, 2011 to May, 2012 and profiles of users who posted at least one post during the period. The spam dataset comes from two confidential spreadsheets that appear to be internally-kept records of the spam posts.

# Dataset content
The data instances are split into the training set and the test set mainly by their temporal orders. There are 2 detection tasks, i.e., spam detection and spammer detection, in our work. The following is a brief introduction to the files. For more details, please refer to our papers in WWW 2015 and SIGIR 2015.

(1) Spam detection for first posts
            - data/first_post/train.json: The training set file for first posts.
            - data/first_post/test.json: The test set file for first posts.
            - data/first_post/test_star.json: The test set* file for first posts.

(2) Spam detection for replies
            - data/reply/train.json: The training set file for replies.
            - data/reply/test.json: The test set file for replies.
            - data/reply/test_star.json: The test set* file for replies.

(3) Spammer detection
            - spammer/train.json: The train set file for spammers.
            - spammer/test.json: The test set file for spammers.

Beyond models:
            - data/thread_info.json: The file providing all meta data of threads.

# Data format
All files are in JSON format and each JSON file has a list of JSON objects containing a post data. The meta data of posts (i.e., first posts and replies) includes 'content', 'is_spam', 'nfloor', 'pnum', 'thid','time', 'uid' and 'uname'. The following is an example of a spam post.
```yaml
{
  'content': '現在智慧型手機市場成熟了，機海搞不好反而會收到效果
            各階層的需求市場都可以買單
            這招好像走對了
            |挖鼻孔|',
  'is_spam' : True,
  'nfloor' : 4,
  'pnum' : 1,
  'thid' : '2708016',
  'time' : '2012-04-26T17:47:00.000Z',
  'uid' : '2092614',
  'uname' : 'imCH'
}
```

The meta data of profiles includes 'is_spam', 'login_time', 'n_eff_posts', 'n_posts', 'n_replies', 'n_threads', 'p_phone_section', 'reg_time', 'score', and 'uid'. The following is an example of a non-spammer.
```yaml
{
  'is_spam' : False,
  'login_time' : '2014-04-22T00:00:00.000Z',
  'n_eff_posts' : 7,
  'n_replies' : 7,
  'n_threads' : 0,
  'p_phone_section' : 100,
  'reg_time' : '2011-04-19T00:00:00.000Z',
  'score' : 0,
  'uid' : '1955698',
}
```
The meta data of threads includes 'clicks', 'fid', 'thid', 'time', 'title' and 'tot_pages'.

Please refer to our WWW-2015 and SIGIR-2015 paper for more details.

# Dataset language and Character encoding
All text is in traditional Chinese and encoded to UTF8.

# Download
Please go to [resources page](http://nlg.csie.ntu.edu.tw/m01-corpus/) to access resources.

# How to Cite the Corpus
Please cite the following two papers when referring to the Mobile01 Corpus in academic publications and papers.

Yu-Ren Chen and Hsin-Hsi Chen (2015). “Opinion Spam Detection in Web Forum: A Real Case Study.” In Proceedings of 24th International World Wide Web Conference (WWW 2015), May 18-22, 2015, Florence, Italy. DOI: http://dx.doi.org/10.1145/2736277.2741085
Yu-Ren Chen and Hsin-Hsi Chen (2015). “Opinion Spammer Detection in Web Forum.” Proceedings of the 38th Annual ACM SIGIR Conference (SIGIR 2015), August 9-13, 2015, Santiago, Chile. DOI: http://dx.doi.org/10.1145/2766462.2767766
