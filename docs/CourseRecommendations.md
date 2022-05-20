## Running For this First time  

<div class="termy">


```console
$ python3 safalta_course_recommendations_beta.py
22022-05-18 20:28:54,702 | 67 :: Starting time
2022-05-18 20:28:54,705 | 123 :: Started querying Bigquery Tables: 2022-05-18 20:28:54.705534
2022-05-18 20:32:24,107 | 127 :: Done Querying Big Query Tables
2022-05-18 20:32:35,041 | 36 :: Started preprocess data with event_type:viewed_course
2022-05-18 20:32:40,834 | 51 :: Done preprocess_data with event_type: viewed_course
2022-05-18 20:32:43,620 | 36 :: Started preprocess data with event_type:clicked_buy_now
2022-05-18 20:32:45,031 | 51 :: Done preprocess_data with event_type: clicked_buy_now
2022-05-18 20:32:45,031 | 36 :: Started preprocess data with event_type:purchase
2022-05-18 20:32:45,590 | 51 :: Done preprocess_data with event_type: purchase
2022-05-18 20:32:45,590 | 69 :: Started Merge different datasets and further preprocessing:
2022-05-18 20:33:34,275 | 102 :: Done Merge different datasets and further preprocessing:
2022-05-18 20:33:34,583 | 50 :: Started Fitting Model:
100%|█████████████████████████████████████████████████████████████████████████████████████████████| 50/50 [05:47<00:00,  6.95s/it]
2022-05-18 20:39:41,965 | 61 :: Model Trained and Saved Successfully
2022-05-18 20:39:42,480 | 37 :: Recommendations for airforce-x-group-course
2022-05-18 20:39:42,491 | 40 :: airforce-x-y-group-course
2022-05-18 20:39:42,491 | 40 :: airforce-y-group-course
2022-05-18 20:39:42,492 | 40 :: airforce-x-y-group-30-days-crash-course-2021
2022-05-18 20:39:42,492 | 40 :: ssb-nda-na-i-ii-2020
2022-05-18 20:39:42,492 | 40 :: airforce-x-group-video-course
2022-05-18 20:39:42,492 | 40 :: nda-score-booster-batch-2021
2022-05-18 20:39:42,492 | 40 :: nda-na-i-2021
2022-05-18 20:39:42,493 | 40 :: airforce-x-y-group-video-course
2022-05-18 20:39:42,493 | 40 :: nda-na-detailed-batch-2021
2022-05-18 20:39:42,493 | 41 ::

2022-05-18 20:39:42,493 | 82 :: End Time

```

Running For this  Every time  Results

```console
$ python3 src/model/safalta_course_recommendations_beta.py
2022-05-18 20:41:44,708 | 67 :: Starting time
2022-05-18 20:41:44,708 | 135 :: Started querying Bigquery Tables:
2022-05-18 20:41:44,709 | 102 :: Started querying Bigquery views_data table for only: 2022-05-17
2022-05-18 20:42:03,231 | 109 :: Previous data shape (2382304, 3)
2022-05-18 20:42:03,325 | 111 :: Yesterday data shape: (5667, 3)
2022-05-18 20:42:05,621 | 113 :: Present data shape: (2382304, 3)
2022-05-18 20:44:09,808 | 115 :: Done Querying Big Query Tables for yesterday
2022-05-18 20:44:10,057 | 102 :: Started querying Bigquery buy_now_data table for only: 2022-05-17
2022-05-18 20:44:13,576 | 109 :: Previous data shape (568731, 2)
2022-05-18 20:44:13,604 | 111 :: Yesterday data shape: (1045, 2)
2022-05-18 20:44:14,075 | 113 :: Present data shape: (568731, 2)
2022-05-18 20:44:24,623 | 115 :: Done Querying Big Query Tables for yesterday
2022-05-18 20:44:24,674 | 102 :: Started querying Bigquery purchase_data table for only: 2022-05-17
2022-05-18 20:44:26,553 | 109 :: Previous data shape (727067, 2)
2022-05-18 20:44:26,571 | 111 :: Yesterday data shape: (0, 2)
2022-05-18 20:44:26,901 | 113 :: Present data shape: (726397, 2)
2022-05-18 20:44:43,152 | 115 :: Done Querying Big Query Tables for yesterday
2022-05-18 20:44:43,188 | 139 :: Done Querying Big Query Tables
2022-05-18 20:44:55,511 | 36 :: Started preprocess data with event_type:viewed_course
2022-05-18 20:45:01,493 | 51 :: Done preprocess_data with event_type: viewed_course
2022-05-18 20:45:01,495 | 36 :: Started preprocess data with event_type:clicked_buy_now
2022-05-18 20:45:02,875 | 51 :: Done preprocess_data with event_type: clicked_buy_now
2022-05-18 20:45:02,876 | 36 :: Started preprocess data with event_type:purchase
2022-05-18 20:45:03,385 | 51 :: Done preprocess_data with event_type: purchase
2022-05-18 20:45:03,385 | 69 :: Started Merge different datasets and further preprocessing:
2022-05-18 20:45:59,453 | 102 :: Done Merge different datasets and further preprocessing:
2022-05-18 20:46:00,091 | 50 :: Started Fitting Model:
 18%|███████████▉                                                      | 9/50 [01:15<05:33,  8.14s/it]
```
</div>


## API

```console

$curl --location --request POST 'https://ml.safalta.com/get_course_recommendation' \
--header 'client-id: 57398d264f1c1b0016ac7a05' \
--header 'property-id: 5d39af7c8ebc3e6cba54b82e' \
--header 'Content-Type: application/json' \
--data-raw '{
    "course_slug":"digital-marketing-classes"
}'



[
  {
    "course_slug": "digital-marketing-classes",
    "recommended_courses": {
      "graphic-designing-classes": 1.0,
      "graphic-designing-class": 1.0,
      "graphic-design-online-classes": 1.0,
      "digital-marketing-session": 1.0,
      "digital-marketing-class": 1.0,
      "graphic-designing-course": 1.0,
      "graphic-designing-online-course": 1.0,
      "graphic-designing-session": 1.0,
      "digital-marketing-online-course": 1.0,
      "spoken-english-classes": 1.0
    }
  }
]

```




```console

$curl --location --request POST 'https://ml.safalta.com/get_multiple_course_recommendation' \
--header 'Client-Id: 57398d264f1c1b0016ac7a05' \
--header 'Property-Id: 5d39af7c8ebc3e6cba54b82e' \
--header 'Content-Type: application/json' \
--data-raw '{
    "courses": [
        "upsssc-pet-complete-batch-2021",
        "a-complete-set-of-puzzle-seating-arrangement",
        "not-course-slug"
    ]
}'


[
  {
    "course_slug": "upsssc-pet-complete-batch-2021",
    "recommended_courses": {
      "upsssc-e-book-set-2021": 1.0,
      "upsssc-mock-test-series-2021": 1.0,
      "upjee-polytechnic": 1.0,
      "sbi-clerk-foundation-batch-2021-batch-2": 1.0,
      "upsssc-pet-online-coaching-2021": 1.0,
      "current-affairs-one-liner-7-2021-september": 1.0,
      "up-police-si-safalta-batch-2021-batch-2": 1.0,
      "monthly-current-affairs-july-2021-hindi": 1.0,
      "afcat-mock-test-series-2021": 1.0,
      "current-affairs-one-liner-19-2021-september": 1.0
    }
  },
  {
    "course_slug": "a-complete-set-of-puzzle-seating-arrangement",
    "recommended_courses": {
      "a-complete-book-of-data-interpretation-and-analysis": 1.0,
      "ibps-clerk-mock-test-series-2021": 1.0,
      "ibps-po-prelims-mains-batch-2021": 1.0,
      "combo-book": 1.0,
      "puzzle-data-interpretation-e-book-combo-pack-hindi": 1.0,
      "ibps-clerk-online-class": 1.0,
      "arithmetic-module-1": 1.0,
      "esic-udc-stenographer-mock-test-series": 1.0,
      "ibps-rrb-mock-test-series-2021": 1.0,
      "bank-special-online-classes": 1.0
    }
  },
  {
    "course_slug": "not-course-slug",
    "recommended_courses": {}
  }
]
```
