---
title: "Error: Failed to create server directory. Please contact support@flutterflow.io"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8098182-error-failed-to-create-server-directory-please-contact-support-flutterflow-io"
hide_table_of_contents: true
---

Background

---

When trying to deploy Firebase storage rules, you might encounter Error: Failed to create server directory. Please contact support@flutterflow.io. This error can occur even after you have enabled Firebase storage in your Firebase Project linked to your FlutterFlow Project. This is likely because you have not set up Cloud Firestore correctly in your Firebase Project.

![](https://downloads.intercomcdn.com/i/o/778603925/5421a47cc7d0c7c7f950ffb6/image.png?expires=1741032900&signature=3fd925587347e236601e46470acfd55b7121f6204b8c89cdd389306dcf73c0ce&req=cycvEMl9lINaFb4f3HP0gGlymc%2BDMAq%2BDydGbf8ljOELonvksFIaTx0SGXdt%0A9FY%3D%0A)---

# How to resolve this issue?

## Step 1: Set Default GCP Resource Location. 

Open your Firebase project and navigate to project settings, then set Default CGP resource location to the region that you prefer.

![](https://downloads.intercomcdn.com/i/o/778606023/d5d089fe181bca150aefc423/image.png?expires=1741032900&signature=48bfa38210088b6bf1f718141f74397f09fbcc7666ee4ee7048678e0cb7efe1f&req=cycvEMl4nYNcFb4f3HP0gPOFzAb0ckYhfVJRlO49h2Qdt3Z5MBlCoveIz6Vv%0ACLg%3D%0A)

## Step 2: Enable Firebase Storage 

In your Firebase project, navigate to the Build section and select Storage. Click get started and then set the rules to testing. In the location segment, set the same location as the one in the project settings. 

![](https://downloads.intercomcdn.com/i/o/778609348/089be7f97cd3bc78c471cd0b/image.png?expires=1741032900&signature=9ded2d21febf11d5e2f65984f037316b9d0962a6de7fc5c654e7b0809d51652e&req=cycvEMl3noVXFb4f3HP0gJWbxgN9IZTL1OSeRiOnXol%2BWl%2BmYs2iPXW4tcXF%0ArIA%3D%0A)![](https://downloads.intercomcdn.com/i/o/778609870/2f50f8967440864cba06e6d7/image.png?expires=1741032900&signature=956fd3d4c6dce2976c64f5dcec08b2e1d4242d83762c08ab6bee012a56157e6f&req=cycvEMl3lYZfFb4f3HP0gNhjm5RdfQFPA9xB5TuGofSRKc4Ui8uf3Dh8uQCw%0Ajz4%3D%0A)

## Step 3: Enable Cloud Firestore

In your Firebase project, navigate to the Build section and select Firestore Database. In some cases, cloud firebase is set to Data Store Mode, which is not recommended when working with FlutterFlow, so you will need to change Cloud Firestore from Data Store Mode to Native Mode.

![](https://downloads.intercomcdn.com/i/o/778614219/57a96120433fb707f34580a7/image.png?expires=1741032900&signature=4f15c1bde52420b0564465e097eea3582cf7c16a05940de92670a9f7fa7ffede&req=cycvEMh6n4BWFb4f3HP0gF8PbQMwI%2FTMwU%2BqY4x3EsPhHEPBom8g%2FYxB4xMT%0A2FU%3D%0A)

### Change to Cloud Firestore to Native Mode

Click on Go to Google Cloud Console

Click Switch To Native Mode

![](https://downloads.intercomcdn.com/i/o/778616395/e6c3460e4b65ba7a4911cd33/image.png?expires=1741032900&signature=e0f210da9425fba3d8f41905f6d6c540225c63f51108890a6bd4f9cc9ca8feb1&req=cycvEMh4nohaFb4f3HP0gI5%2FHJ7XpO2574wfTZBcVw9xQZu9IzQo%2FSC4Cgb3%0Aq%2FU%3D%0A)

After switching the mode, navigate back to Firebase and reload Cloud Firestore.

![](https://downloads.intercomcdn.com/i/o/778617100/782a7aa679962827ee9c2cf1/image.png?expires=1741032900&signature=5a977a24d1355717c4501034100d2d5ad0dc31380d990978c5f84fd011f3b6e5&req=cycvEMh5nIFfFb4f3HP0gLfU6zm2PomSheYWY3WUAVj2nGboAdA4ztK2Ychn%0AS54%3D%0A)

## Step 4: Deploy Firebase Storage Rules in FlutterFlow 

Open your FlutterFlow Project and re-deploy Firebase Storage Rules.

![](https://downloads.intercomcdn.com/i/o/778617912/422549df74ab1d6495c17e5b/image.png?expires=1741032900&signature=f3a9e8bdf5b87f8543d95f967ccbb2948938ea050f34e35f4c56f98753fdf91e&req=cycvEMh5lIBdFb4f3HP0gC9nq9TC3VMsyxvKVW%2F0%2BKOfnaMZegh76gcRbI3%2F%0A%2Ffs%3D%0A)![](https://downloads.intercomcdn.com/i/o/778618456/3eb0bcabe0a27cbde317d2ff/image.png?expires=1741032900&signature=77462fe23a16d4c1ba3577055eb9af9bd55df1a6447cfdd3ef847a243cdeb63f&req=cycvEMh2mYRZFb4f3HP0gNvIRgRiF%2FnCafCNN6TFzS7RioaBECzZHgCo176q%0AwWA%3D%0A)

The issue was not resolved.

---

If the error still persists after following the outlined steps, please contact support via Chat or Email at support@flutterflow.io.