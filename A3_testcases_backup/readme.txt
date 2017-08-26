This folder contains the test cases for A3.

The commands and expected output are as follows:

command with -d:
	./image_retrieval -d DIR_NAME IMAGE_FILE

	./image_retrieval -d actual_same_image source_images/actual_same_image.ppm
	big_table_chopped.ppm

	./image_retrieval -d different_set_similar_images source_images/different_set_similar_images.ppm
	table_03_cropped.ppm

	./image_retrieval -d distinct_large_picture source_images/distinct_large_picture.ppm
	big_table_cropped.ppm

	./image_retrieval -d many_small_pics source_images/many_small_pics.ppm
	small_466.ppm

	./image_retrieval -d mixed_valid_invalid_image source_images/mixed_valid_invalid_image.ppm
	Basket_018.ppm 

	./image_retrieval -d no_similar_images source_images/no_similar_images.ppm
	basket_chopped.ppm

	./image_retrieval -d no_sub_folder source_images/no_sub_folder.ppm
	SHOULD NOT CRASH

	./image_retrieval -d non_ppm_image source_images/non_ppm_image.ppm
	SHOULD NOT CRASH

	./image_retrieval -d similar_images_multiple_small source_images/similar_images_multiple_small.ppm
	[small_02.ppm, small_dis13_1.ppm, small_dis13_2.ppm, small_dis13_3.ppm]

	./image_retrieval -d similar_images_unique_large source_images/similar_images_unique_large.ppm
	whale_00.ppm

	./image_retrieval -d similar_images_unique_small source_images/similar_images_unique_small.ppm
	small_05.ppm

	./image_retrieval -d similar_images_with_diff_size source_images/similar_images_with_diff_size.ppm
	SHOULD NOT CRASH

	./image_retrieval -d valid_ppm_with_non_ppm_suffix source_images/valid_ppm_with_non_ppm_suffix.ppm
	basket_01.ppm



For commands without using -d option, we can cd into each directory, then call command using 
"./image_retrieval ../source_images/IMAGE_NAME", this will have the same effect as the above commands.



To test distance output:
***
Note: the precision seems to be different since I used python3 here.
So it maybe better to define a range of accepted distance.
***

./image_retrieval -d valid_ppm_with_non_ppm_suffix source_images/valid_ppm_with_non_ppm_suffix.ppm
The most similar image is basket_01.ppm with a diatance of 2.2010769747647685


./image_retrieval -d actual_same_image source_images/actual_same_image.ppm
The most similar image is basket_01.ppm with a diatance of 0.00000


./image_retrieval -d distinct_large_picture source_images/distinct_large_picture.ppm 
The most similar image is big_table_cropped.ppm with a diatance of 122.55910789223799





