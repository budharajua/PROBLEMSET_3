# PROBLEMSET_3
#solutions for problem set 3

#PROBLEM 1
fhand = open("/ufrc/zoo6927/share/Class_Files/data/CO-OPS__8729108__wl.csv")
largest = None
for line in fhand:
    line = line.rstrip()
    delimiter = ","
    words = line.split(delimiter)
    #print(words[1])
    if largest is None or words[1]>largest:
        largest = words[1]
print("Highest Water Level:", largest) 

#PROBLEM 2
df=pd.read_csv("/ufrc/zoo6927/share/Class_Files/data/CO-OPS__8729108__wl.csv")
df.loc[df[' Water Level'].idxmax()]

#PROBLEM 3
df= pd.read_csv("/ufrc/zoo6927/share/Class_Files/data/CO-OPS__8729108__wl.csv")
df["Water_Level_Difference"] = df[" Water Level"] - df[" Water Level"].shift(-1)
df.loc[df["Water_Level_Difference"].idxmax()]

#PROBLEM 4
#Undergrad
