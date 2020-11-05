# attention_matrices_opennmt_transofrmer
This code will provide additional debug function to output attention matrices from all heads in all layers.

**Be careful, this code is only for transformer translation with OpenNMT**

**You cannot use this for any other purpose (training, rnn model, and so on)**

## Original code outputs
```
                    彼          は         水泳          が         得意          で          は          な         かっ          た          。 
        he  0.1926349  0.2135644 *0.3037547  0.1662329  0.0272146  0.0256509  0.0133634  0.0147541  0.0181808  0.0119007  0.0127486 
       was  0.0003296  0.0002715  0.0078232  0.0054593  0.2146050  0.0028785  0.0006307  0.0103063  0.0127522 *0.7397975  0.0051462 
       not *0.2972103  0.1988322  0.1497583  0.0059330  0.1654069  0.0012575  0.0006963  0.0025957  0.0013412  0.1657965  0.0111720 
      good  0.0726774  0.0635210  0.0339526  0.0030502 *0.2572910  0.0081822  0.0988948  0.1765248  0.1591378  0.0552028  0.0715652 
        at  0.0029933  0.0025115  0.0109872  0.0131064  0.0026235  0.0025539  0.1246577  0.1441116 *0.3401029  0.3384554  0.0178969 
  swimming  0.0001587  0.0002043 *0.9994454  0.0001555  0.0000120  0.0000039  0.0000073  0.0000008  0.0000015  0.0000027  0.0000078 
         .  0.0002052  0.0002118  0.0001796  0.0119230  0.0093502  0.0049550  0.1294626 *0.3055270  0.2840273  0.0903514  0.1638069 
      </s>  0.0774564  0.0717031  0.0039419  0.0056847  0.0809682  0.1477892  0.0580925  0.1051003  0.0485598 *0.3345482  0.0661556 
```

## Modified code outputs
```
layer: 1 || head: 1
                    彼          は         水泳          が         得意          で          は          な         かっ          た          。 
        he  0.1317690  0.1431092 *0.6492066  0.0621998  0.0006849  0.0008576  0.0014918  0.0022297  0.0019207  0.0056224  0.0009081 
       was  0.0011874  0.0013639  0.0133887  0.0139621  0.0087429  0.0320573 *0.3478778  0.2681966  0.1891317  0.0130612  0.1110303 
       not  0.0010208  0.0009970  0.0214519  0.0192029  0.0749326  0.0314771  0.0560722  0.0436250  0.0320744 *0.6824098  0.0367364 
      good  0.0002222  0.0001636  0.0007924  0.0088532 *0.4916196  0.2402480  0.0559826  0.1036002  0.0343166  0.0145008  0.0497008 
        at  0.0576358  0.0497589  0.0043088  0.0112185 *0.3325394  0.2438139  0.1574941  0.0710646  0.0165800  0.0355184  0.0200677 
  swimming  0.0075492  0.0065343  0.0198430  0.0475265  0.0167443  0.0219905  0.1683472  0.2541997 *0.2550970  0.0312095  0.1709588 
         . *0.5177081  0.4450698  0.0088729  0.0010436  0.0191833  0.0033670  0.0011628  0.0001845  0.0003695  0.0016854  0.0013532 
      </s> *0.4841074  0.3982586  0.0734532  0.0163170  0.0003891  0.0017990  0.0095470  0.0010076  0.0022769  0.0076561  0.0051879 
layer: 1 || head: 2
                    彼          は         水泳          が         得意          で          は          な         かっ          た          。 
        he  0.0292578  0.0316353  0.0005262  0.0002370  0.0010367  0.0019914  0.0302462  0.0094020  0.0091893 *0.8819256  0.0045523 
       was  0.0353563  0.0373492  0.0041485  0.0004376  0.0011323  0.0015732  0.0262167  0.0205722  0.0455045 *0.8202386  0.0074709 
       not  0.0095911  0.0107062  0.0223548  0.1388103  0.1576510 *0.4056246  0.0903982  0.0435534  0.0369983  0.0296234  0.0546886 
      good  0.0006642  0.0008153  0.0010357  0.0070738  0.2544952 *0.7129974  0.0016512  0.0033023  0.0021015  0.0017880  0.0140755 
        at  0.0007473  0.0007896  0.0020935  0.1212146 *0.5621742  0.1673461  0.0132722  0.0657197  0.0210916  0.0014378  0.0441134 
  swimming  0.0043402  0.0044556  0.0000607  0.0029863 *0.6194050  0.2679759  0.0145156  0.0260168  0.0119995  0.0013175  0.0469268 
         .  0.1603826  0.1392348 *0.4098374  0.1753191  0.0128001  0.0191576  0.0341322  0.0069451  0.0122139  0.0022830  0.0276941 
      </s> *0.2140017  0.1782235  0.0489036  0.0328684  0.0006416  0.0368659  0.1510854  0.0508401  0.1071648  0.0293944  0.1500104 
layer: 1 || head: 3
:
:
```

## Usage

The usage is described the next 2 files.

[0_training.ipynb](https://github.com/YasumotoGenki/attention_matrices_opennmt_transofrmer/blob/main/0_training.ipynb),

[1_translation.ipynb](https://github.com/YasumotoGenki/attention_matrices_opennmt_transofrmer/blob/main/1_translation.ipynb)

## LICENSE

This code is based on [MIT LICENSE]()
