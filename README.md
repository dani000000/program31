# program31
#name: alfa quezada
#email: alfa.quezada55@myhunter.cuny.edu

import pandas as pd
import matplotlib.pyplot as plt

int1 = input("Enter the name of the input file:")
int2 = input("Enter the name of the output file:")

homeless = pd.read_csv(int1)
homeless["Fraction Children"] = homeless["Total Children in Shelter"] / homeless["Total Individuals in Shelter"]

homeless.plot(x="Date of census", y ="Fraction Children")

fig = plt.gcf()
fig.savefig(int2)
