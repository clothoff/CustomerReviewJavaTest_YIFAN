To complete the tasks required in the CustomerReview_Exercise_Overview.txt file, I created 3 new files and modified 4 existing files. 
The details are the following:

New files:
	README.txt			(CustomerReview_Exercise folder)
	InappropriateWordException.java	(package de.hybris.platform.customerreview.impl)
	InvalidRatingException.java	(package de.hybris.platform.customerreview.impl)

Modified files(modified areas are marked with comment "============ MODIFIED BY YIFAN WU ============"):
	DefaultCustomerReviewService.java
	CustomerReviewManager.java
	GeneratedCustomerReviewManager.java
	customerreview-spring.xml


Comments:

	getNumberOfReviewsWithinRange:
		My idea right here is just to utilize the existing "getNumberOfReviews" function. 
		I change it by simply adding a "BETWEEN" condition in the Flexible Search query to return the numbers of review with ratings within the given range.

	Additional Checks before Creating Reviews:
		Since there are two different checks before creating a review, so I created two exception classes for each.
		By declaring a list of string of curse words in customerreview-spring.xml file, I inject the collection value by setter method in Spring framework. And I check if the comment contains any of these curse words.



BY YIFAN WU 2017/11/13