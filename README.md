# cmpe255-spring19-assignment1

Dataframe containing business_id and text

business_id	              text	                                          stars	positive	negative	label
0	ikCg8xy5JIg_NGPx-MSIDA	Went in for a lunch. Steak sandwich was delici...	5.0	  0         	0	      0
1	eU_713ec6fTGNO4BegRaww	I'll be the first to admit that I was not exci...	4.0	  0	          0	      0
2	3fw2X5bZYeW9xCz_zGhOHg	Tracy dessert had a big name in Hong Kong and ...	3.0	  0         	0	      0
3	zvO-PJCpNk4fgAVUnExYAA	This place has gone down hill. Clearly they h...	1.0	  0	          0	      0
4	8mIrX_LrOnAqWsB5JrOojQ	Like walking back in time, every Saturday morn...	4.0	  0	          0	      0

After counting the number of positive and negative words in reviews and labellingfor positive(+1),negative(-1) and neutral(0):

business_id	              text	                                           stars	positive	negative	label
0	ikCg8xy5JIg_NGPx-MSIDA	Went in for a lunch. Steak sandwich was delici...	5.0	 12	          0	        1
1	eU_713ec6fTGNO4BegRaww	I'll be the first to admit that I was not exci...	4.0	 23	          6	        1
2	3fw2X5bZYeW9xCz_zGhOHg	Tracy dessert had a big name in Hong Kong and ...	3.0	 18	          3	        1
3	zvO-PJCpNk4fgAVUnExYAA	This place has gone down hill. Clearly they h...	1.0 	0	          5	       -1
4	8mIrX_LrOnAqWsB5JrOojQ	Like walking back in time, every Saturday morn...	4.0	  6	          1	        1

Results after using MultinomialNB:
               precision    recall  f1-score   support

         -1       0.43      0.04      0.07       558
          0       0.36      0.04      0.08       595
          1       0.88      0.99      0.94      8437

avg / total       0.83      0.88      0.83      9590

Cross Validation scores after using MultinomialNB= [0.87600536 0.87756926 0.87798883 0.87751453 0.87907912]

Results after using SGDClassifier:

                precision    recall  f1-score   support

         -1       0.43      0.35      0.39       558
          0       0.22      0.13      0.17       595
          1       0.92      0.96      0.94      8437

avg / total       0.85      0.87      0.86      9590

Cross Validation scores after using SGDClassifier= [0.87600536 0.87756926 0.87798883 0.87751453 0.87907912]


Instances of Positive Reviews-Business_id,Given_stars,Predicted label

Business_id            Stars  Predicted-Labels
gnKjwL_1w79qoiV3IC_xQQ 4.0    1.0
fweCYi8FmbJXHCqLnwuk8w 4.0    1.0
1RHY4K3BD22FK7Cfftn8Mg 4.0    1.0
NDuUMJfrWk52RA-H-OtrpA 3.0    1.0
BvYU3jvGd0TJ7IyZdfiN2Q 3.5    1.0


Instances of Negative Reviews-Business_id,Given-stars,Predicted label

Business_id            Stars  Predicted-Labels
emyCP3Ry2SbpNrwRAtm9PQ 2.5    -1.0
5DLxa3EQQykWFdIJ-KU5jg 2.5    -1.0
zLHOG9ty0OcXSQ6iy2BwwA 2.0    -1.0
rDTCvOrVYN9USxyB-fNHyw 2.5    -1.0
2uAicR2Gel9BMy7jyYUcjw 1.5    -1.0

Instances of Neutral Reviews-Business_id,Given-stars,Predicted label

Business_id            Stars  Predicted-Labels
-jdNqqzF1Dbve04oEd4jww 3.0    0.0
UmFty_GxdqVe35apYnmGbw 3.0    0.0
Z3UBeP5EoKIXIDmEdA3JmQ 3.0    0.0
CnWb3k8tUaxLZfDoYrpagA 3.0    0.0
QJMRAjCIuqrHGmeAZeYzOQ 3.0    0.0
VIsPmeZBMLkgbgw4UqCjUQ 3.0    0.0

Instances of Misclassified Reviews-Business_id,Given-stars,Predicted label

Business_id            Stars  Predicted-Labels
PZ-LZzSlhSe9utkQYU8pFg 4.0    0.0
NDuUMJfrWk52RA-H-OtrpA 3.0    1.0
_J_x_RaYTqAqAuCwgRhnRQ 3.0    1.0
kANF0dbeoW34s2vwh6Umfw 2.0    1.0
gyFYZV4b_9TxG1ulQNi0Ig 2.0    1.0
