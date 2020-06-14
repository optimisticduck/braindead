import itertools

f = open("p.txt", "w+")

first_word = list(itertools.permutations('abcdefghijklmnopqrstuvwxyz', 2))

counter1 = 0
counter2 = 0

f.write("Permutations for the first word: \n")
for i in first_word:
    f.writelines("p"+"".join(i)+"\n")
    counter1+=1

second_word = list(itertools.permutations('abcdefghijklmnopqrstuvwxyz', 4))

f.write("Permutations for the second word: \n")
for i in second_word:
    f.writelines("".join(i)+"\n")
    counter2+=1

f.writelines("Total number of permutations for the first word: " + str(counter1) + "\n")
f.writelines("Total number of permutations for the second word: " + str(counter2))

f.close()
