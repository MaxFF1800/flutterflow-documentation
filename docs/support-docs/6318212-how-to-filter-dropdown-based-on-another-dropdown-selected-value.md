---
title: "How to: Filter dropdown based on another dropdown selected value"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6318212-how-to-filter-dropdown-based-on-another-dropdown-selected-value"
hide_table_of_contents: true
---

What we are doing?

We want to filter a Dropdown widget value, based on another Dropdown Selected value.

In our example, we ask the user to select his vehicle make and model. and we show the user the available vehicle makes, and based on the vehicle make selected we filter the vehicle models.

so if the user selects the BMW we just show the BMW models in the next Dropdown.

Public Project

Run Mode

---

Database:

We need separate collections for each vehicle make and vehicle model.

Collection "make", With one single field "name" from type String, we want to save the name of each vehicle make there. so for each vehicle make we need to make a collection.

![](https://downloads.intercomcdn.com/i/o/532914625/e7c54a09f1010d206602e5d3/image.png?expires=1741032900&signature=32e119043aa1f819a31cbd243ad6b570c33c030e366835a4f0618d26673c0276&req=cSMlH8h6m4NaFb4f3HP0gEcveqV9T72RHiwPSsE06pGI0lXUR5RJZj9CImXU%0AkwI%3D%0A)

![](https://downloads.intercomcdn.com/i/o/532893034/8a007826c69e1c81ed54473c/image.png?expires=1741032900&signature=0b0abfccd08456af7d3585f5bd9e8378ff10ca9cf1034b10e47d3cf0839236ea&req=cSMlHsB9nYJbFb4f3HP0gEHBpADl5G%2BI%2F%2FR6Yego8UZpoxhHHFdTTqNQGTEZ%0A4sw%3D%0A)

![](https://downloads.intercomcdn.com/i/o/532893361/23a5208747bfecc8a5ccfb87/image.png?expires=1741032900&signature=661f10f11f22c6b00c43b850d33cbc762a7b2b6112ffea0feff43f3f5c288e39&req=cSMlHsB9nodeFb4f3HP0gCA7I8rtDh5b7kxSGgBgBsFJQ7fNJnIBO9u%2Frcnx%0AS28%3D%0A)

Here we have Three vehicle makes.

Collection "model", With a field "name" from type String

a field "make_name" from type String [ we need to put the same exact name of the make collections for each model ]

![](https://downloads.intercomcdn.com/i/o/532894888/2bf9a2cdc5a0baa3b47f390e/image.png?expires=1741032900&signature=825627dc24dde0506401bf2b0000731706a47296f1e0ccb8362d461205eb82fe&req=cSMlHsB6lYlXFb4f3HP0gJ%2B0wSRYIaRL%2Bta6NVxYKGqr3CD2275yYA6WxaDi%0Aeo4%3D%0A)

![](https://downloads.intercomcdn.com/i/o/532895294/3b3c6547b50a182310902bd7/image.png?expires=1741032900&signature=577221bafa25df516b1ac13fe6d631aff64c6089854728088e1dfed3207ed7bc&req=cSMlHsB7n4hbFb4f3HP0gIBVfvM2OFaYksEz5Yrc9Q29pa3CaQETSH8Ytk3k%0A3Ww%3D%0A)

As you can see for example in model collections, for each BMW model I have a make_name field that is the same as the make collections name fields.

​

Next: User Interface

On this page, we have two dropdowns and a button to just show the selected values.

Notice: You can grow this principle for as many dropdowns you need

![](https://downloads.intercomcdn.com/i/o/532900828/2d52ab040bb1b8fabee59da2/image.png?expires=1741032900&signature=a199a3f6fdfbfd6200bfe8c6231a2f2d2bf1e15a7b16846d8f998cda87edc8fb&req=cSMlH8l%2BlYNXFb4f3HP0gEnUzWmMiFfDYF5E1GwxKFgl3NGkby%2FVIwAeCs%2Bj%0Aou4%3D%0A)

 We need to query items on each dropdown.

1: Our query on the collection "make" on the first dropdown

![](https://downloads.intercomcdn.com/i/o/532902208/5f46c0dd453f6fe83d7f9057/image.png?expires=1741032900&signature=e406e01736bf3a4c22a7ba4407fa39b11d288cf56531c75af252cc226d734ed7&req=cSMlH8l8n4FXFb4f3HP0gKn8dTDEr7LuHoYBZkCtjcq0jvVeHnVvz2Fbe8Fe%0AXfA%3D%0A)

In the first dropdown, we are retrieving all make items. then we need to set the result for dropdown options.

![](https://downloads.intercomcdn.com/i/o/532903050/0510cc07c1e595669d51e8b3/image.png?expires=1741032900&signature=f2a6216a524c7d4cc51bb0166f254edff04b76fc4bd52ef6f2fc503c14fb8276&req=cSMlH8l9nYRfFb4f3HP0gEf45TJBq4BOegn%2FhdksEezRc5r4DaLPIX4sNKfY%0AEV4%3D%0A)

![](https://downloads.intercomcdn.com/i/o/532903324/5e4635f3f2633a591dd76ec5/image.png?expires=1741032900&signature=49d2ef6c90774011fb667cadaf1f2837276e4aa2cbf3f7af087457bc991c01aa&req=cSMlH8l9noNbFb4f3HP0gDYW1dGjESijXjtz4BfFwS2h4iM%2FbraxIh9jlChk%0AwXM%3D%0A)

Now we have all vehicle makes loaded into the first dropdown.

2: We want to do the same with the second dropdown, the only difference here is that we do a query on "model" collection, and we add a filter to the query, on the field name "make_name".

the field is referring to the collection make names.

![](https://downloads.intercomcdn.com/i/o/532905249/fe90db9fc82fba9e36e547fa/image.png?expires=1741032900&signature=f6a6c5ed734d09d9367dc6cb622ad83c739e377b7f7716d1ddb5950a32a16a55&req=cSMlH8l7n4VWFb4f3HP0gFysJ6UWdaWBtTvn6Vwh6C%2FqhgSQdhwXSAmoBejR%0ASwY%3D%0A)

Again after the query, we set the result to the dropdown options.

![](https://downloads.intercomcdn.com/i/o/532905696/d45fdda41007c48c76739952/image.png?expires=1741032900&signature=6b2cb885a5e5edc2687dbca4a47ebf10b64dfeff2165661719465d583cb8c5c1&req=cSMlH8l7m4hZFb4f3HP0gNgjbhXJFE87LpSZguFgZf5%2B20AtKPnjQ0rAkrfk%0AyhQ%3D%0A)

Now both dropdowns are set, and we can use the values.

This way each time the first dropdown value is changing, our second query will be executed again with the new value [ value we used in the query filter ]

You can check the public project and see this is real action.