# PyDataLA2019
Code for the workshop
1. Title: Online News Popularity

2. Source Information
    -- Creators: Kelwin Fernandes (kafc ‘@’ inesctec.pt, kelwinfc ’@’ gmail.com),
                 Pedro Vinagre (pedro.vinagre.sousa ’@’ gmail.com) and
                 Pedro Sernadela
   -- Donor: Kelwin Fernandes (kafc ’@’ inesctec.pt, kelwinfc '@' gmail.com)
   -- Date: May, 2015

3. Past Usage:
    1. K. Fernandes, P. Vinagre and P. Cortez. A Proactive Intelligent Decision
       Support System for Predicting the Popularity of Online News. Proceedings
       of the 17th EPIA 2015 - Portuguese Conference on Artificial Intelligence,
       September, Coimbra, Portugal.

       -- Results: 
          -- Binary classification as popular vs unpopular using a decision
             threshold of 1400 social interactions.
          -- Experiments with different models: Random Forest (best model),
             Adaboost, SVM, KNN and Naïve Bayes.
          -- Recorded 67% of accuracy and 0.73 of AUC.
    - Predicted attribute: online news popularity (boolean)

4. Relevant Information:
   -- The articles were published by Mashable (www.mashable.com) and their
      content as the rights to reproduce it belongs to them. Hence, this
      dataset does not share the original content but some statistics
      associated with it. The original content be publicly accessed and
      retrieved using the provided urls.
   -- Acquisition date: January 8, 2015
   -- The estimated relative performance values were estimated by the authors
      using a Random Forest classifier and a rolling windows as assessment
      method.  See their article for more details on how the relative
      performance values were set.

5. Number of Instances: 39797 

6. Number of Attributes: 61 (58 predictive attributes, 2 non-predictive, 
                             1 goal field)

7. Attribute Information:
     0. url:                           URL of the article
     1. timedelta:                     Days between the article publication and
                                       the dataset acquisition
     2. n_tokens_title:                Number of words in the title
     3. n_tokens_content:              Number of words in the content
     4. n_unique_tokens:               Rate of unique words in the content
     5. n_non_stop_words:              Rate of non-stop words in the content
     6. n_non_stop_unique_tokens:      Rate of unique non-stop words in the
                                       content
     7. num_hrefs:                     Number of links
     8. num_self_hrefs:                Number of links to other articles
                                       published by Mashable
     9. num_imgs:                      Number of images
    10. num_videos:                    Number of videos
    11. average_token_length:          Average length of the words in the
                                       content
    12. num_keywords:                  Number of keywords in the metadata
    13. data_channel_is_lifestyle:     Is data channel 'Lifestyle'?
    14. data_channel_is_entertainment: Is data channel 'Entertainment'?
    15. data_channel_is_bus:           Is data channel 'Business'?
    16. data_channel_is_socmed:        Is data channel 'Social Media'?
    17. data_channel_is_tech:          Is data channel 'Tech'?
    18. data_channel_is_world:         Is data channel 'World'?
    19. kw_min_min:                    Worst keyword (min. shares)
    20. kw_max_min:                    Worst keyword (max. shares)
    21. kw_avg_min:                    Worst keyword (avg. shares)
    22. kw_min_max:                    Best keyword (min. shares)
    23. kw_max_max:                    Best keyword (max. shares)
    24. kw_avg_max:                    Best keyword (avg. shares)
    25. kw_min_avg:                    Avg. keyword (min. shares)
    26. kw_max_avg:                    Avg. keyword (max. shares)
    27. kw_avg_avg:                    Avg. keyword (avg. shares)
    28. self_reference_min_shares:     Min. shares of referenced articles in
                                       Mashable
    29. self_reference_max_shares:     Max. shares of referenced articles in
                                       Mashable
    30. self_reference_avg_sharess:    Avg. shares of referenced articles in
                                       Mashable
    31. weekday_is_monday:             Was the article published on a Monday?
    32. weekday_is_tuesday:            Was the article published on a Tuesday?
    33. weekday_is_wednesday:          Was the article published on a Wednesday?
    34. weekday_is_thursday:           Was the article published on a Thursday?
    35. weekday_is_friday:             Was the article published on a Friday?
    36. weekday_is_saturday:           Was the article published on a Saturday?
    37. weekday_is_sunday:             Was the article published on a Sunday?
    38. is_weekend:                    Was the article published on the weekend?
    39. LDA_00:                        Closeness to LDA topic 0
    40. LDA_01:                        Closeness to LDA topic 1
    41. LDA_02:                        Closeness to LDA topic 2
    42. LDA_03:                        Closeness to LDA topic 3
    43. LDA_04:                        Closeness to LDA topic 4
    44. global_subjectivity:           Text subjectivity
    45. global_sentiment_polarity:     Text sentiment polarity
    46. global_rate_positive_words:    Rate of positive words in the content
    47. global_rate_negative_words:    Rate of negative words in the content
    48. rate_positive_words:           Rate of positive words among non-neutral
                                       tokens
    49. rate_negative_words:           Rate of negative words among non-neutral
                                       tokens
    50. avg_positive_polarity:         Avg. polarity of positive words
    51. min_positive_polarity:         Min. polarity of positive words
    52. max_positive_polarity:         Max. polarity of positive words
    53. avg_negative_polarity:         Avg. polarity of negative  words
    54. min_negative_polarity:         Min. polarity of negative  words
    55. max_negative_polarity:         Max. polarity of negative  words
    56. title_subjectivity:            Title subjectivity
    57. title_sentiment_polarity:      Title polarity
    58. abs_title_subjectivity:        Absolute subjectivity level
    59. abs_title_sentiment_polarity:  Absolute polarity level
    60. shares:                        Number of shares (target)

8. Missing Attribute Values: None

9. Class Distribution: the class value (shares) is continuously valued. We
                       transformed the task into a binary task using a decision
                       threshold of 1400.

   Shares Value Range:   Number of Instances in Range:
   <  1400            18490
   >= 1400            21154


Summary Statistics:
                       Feature       Min          Max         Mean           SD
                     timedelta    8.0000     731.0000     354.5305     214.1611
                n_tokens_title    2.0000      23.0000      10.3987       2.1140
              n_tokens_content    0.0000    8474.0000     546.5147     471.1016
               n_unique_tokens    0.0000     701.0000       0.5482       3.5207
              n_non_stop_words    0.0000    1042.0000       0.9965       5.2312
      n_non_stop_unique_tokens    0.0000     650.0000       0.6892       3.2648
                     num_hrefs    0.0000     304.0000      10.8837      11.3319
                num_self_hrefs    0.0000     116.0000       3.2936       3.8551
                      num_imgs    0.0000     128.0000       4.5441       8.3093
                    num_videos    0.0000      91.0000       1.2499       4.1078
          average_token_length    0.0000       8.0415       4.5482       0.8444
                  num_keywords    1.0000      10.0000       7.2238       1.9091
     data_channel_is_lifestyle    0.0000       1.0000       0.0529       0.2239
 data_channel_is_entertainment    0.0000       1.0000       0.1780       0.3825
           data_channel_is_bus    0.0000       1.0000       0.1579       0.3646
        data_channel_is_socmed    0.0000       1.0000       0.0586       0.2349
          data_channel_is_tech    0.0000       1.0000       0.1853       0.3885
         data_channel_is_world    0.0000       1.0000       0.2126       0.4091
                    kw_min_min   -1.0000     377.0000      26.1068      69.6323
                    kw_max_min    0.0000  298400.0000    1153.9517    3857.9422
                    kw_avg_min   -1.0000   42827.8571     312.3670     620.7761
                    kw_min_max    0.0000  843300.0000   13612.3541   57985.2980
                    kw_max_max    0.0000  843300.0000  752324.0667  214499.4242
                    kw_avg_max    0.0000  843300.0000  259281.9381  135100.5433
                    kw_min_avg   -1.0000    3613.0398    1117.1466    1137.4426
                    kw_max_avg    0.0000  298400.0000    5657.2112    6098.7950
                    kw_avg_avg    0.0000   43567.6599    3135.8586    1318.1338
     self_reference_min_shares    0.0000  843300.0000    3998.7554   19738.4216
     self_reference_max_shares    0.0000  843300.0000   10329.2127   41027.0592
    self_reference_avg_sharess    0.0000  843300.0000    6401.6976   24211.0269
             weekday_is_monday    0.0000       1.0000       0.1680       0.3739
            weekday_is_tuesday    0.0000       1.0000       0.1864       0.3894
          weekday_is_wednesday    0.0000       1.0000       0.1875       0.3903
           weekday_is_thursday    0.0000       1.0000       0.1833       0.3869
             weekday_is_friday    0.0000       1.0000       0.1438       0.3509
           weekday_is_saturday    0.0000       1.0000       0.0619       0.2409
             weekday_is_sunday    0.0000       1.0000       0.0690       0.2535
                    is_weekend    0.0000       1.0000       0.1309       0.3373
                        LDA_00    0.0000       0.9270       0.1846       0.2630
                        LDA_01    0.0000       0.9259       0.1413       0.2197
                        LDA_02    0.0000       0.9200       0.2163       0.2821
                        LDA_03    0.0000       0.9265       0.2238       0.2952
                        LDA_04    0.0000       0.9272       0.2340       0.2892
           global_subjectivity    0.0000       1.0000       0.4434       0.1167
     global_sentiment_polarity   -0.3937       0.7278       0.1193       0.0969
    global_rate_positive_words    0.0000       0.1555       0.0396       0.0174
    global_rate_negative_words    0.0000       0.1849       0.0166       0.0108
           rate_positive_words    0.0000       1.0000       0.6822       0.1902
           rate_negative_words    0.0000       1.0000       0.2879       0.1562
         avg_positive_polarity    0.0000       1.0000       0.3538       0.1045
         min_positive_polarity    0.0000       1.0000       0.0954       0.0713
         max_positive_polarity    0.0000       1.0000       0.7567       0.2478
         avg_negative_polarity   -1.0000       0.0000      -0.2595       0.1277
         min_negative_polarity   -1.0000       0.0000      -0.5219       0.2903
         max_negative_polarity   -1.0000       0.0000      -0.1075       0.0954
            title_subjectivity    0.0000       1.0000       0.2824       0.3242
      title_sentiment_polarity   -1.0000       1.0000       0.0714       0.2654
        abs_title_subjectivity    0.0000       0.5000       0.3418       0.1888
  abs_title_sentiment_polarity    0.0000       1.0000       0.1561       0.2263

   
 Citation Request:
 
 Please include this citation if you plan to use this database: 
 
    K. Fernandes, P. Vinagre and P. Cortez. A Proactive Intelligent Decision
    Support System for Predicting the Popularity of Online News. Proceedings
    of the 17th EPIA 2015 - Portuguese Conference on Artificial Intelligence,
    September, Coimbra, Portugal.

