# lesson-9-files-and-exeptions
import codecs
try:
    file = codecs.open("how-to-turn-dirt-into-gold.txt", "r", "utf_8_sig")
    string = file.read()
    string = string.lower()
    listik = string.split()
    count1 = listik.count('the')
    count2 = listik.count("if")
    count3 = string.count("e")
    file.close()

except IOError:
    count1 = 0
    count2 = 0
    count3 = 0
    print("Not found!!!...")
file2 = open("statistics.txt", "w")
file2.write("Count of the: " + str(count1) + '\n')
file2.write("Count of if: " + str(count2) + '\n')
file2.write("Count of e: " + str(count3) + '\n')
file2.close()




#The output in statistics:
Count of the: 70
Count of if: 1
Count of e: 398

