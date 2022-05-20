## Running For this First time  




## API

```console

$curl --location --request GET 'https://ml.safalta.com/get_related_entity_recommendation' \
--header 'client-id: 57398d264f1c1b0016ac7a05' \
--header 'property-id: 5d39af7c8ebc3e6cba54b82e' \
--header 'Content-Type: application/json' \
--data-raw '{
    "blog_slug": "police"
}'

[
  {
    "blog_slug": "police",
    "recommended_courses": {
      "course": [
        "up-police-si-free-class",
        "up-police-si-safalta-batch-2021",
        "haryana-police-constable-batch-2021",
        "up-constable-hindi-classes",
        "up-si-practice-batch",
        "up-police-si-safalta-batch-2021-batch-2",
        "up-police-si-safalta-batch-2021-batch-3",
        "delhi-police-constable-60-days-video-course",
        "up-si-test-series-2021-mock-test",
        "up-police-si-asi-umaang-2-0-batch",
        "up-police-online-classes",
        "up-police-si-online-coaching",
        "bihar-police-fireman-all-india-mock-test"
      ],
      "ebook": [
        "up-police-constable-free-e-book-kit",
        "up-si-ebook-kit-2021-hindi",
        "delhi-police-constable-gk-capsule"
      ],
      "mock": [
        "haryana-police-si-mock-test-series-2021"
      ],
      "practice": [
        "up-police-si-free-practice-tests"
      ],
      "video": [
        "up-si-marathon-video-course"
      ]
    }
  }
]

```
