import random

list=[]
a=-1
puan=0
def i1():
	while True:
		gen=input("uzunluk :")
		uzn=input("genişlik :")
		if gen.isdigit()==uzn.isdigit()==1:
			gen=int(gen)
			uzn=int(uzn)
			if 35>gen>1 and 35>uzn>1:
				return gen,uzn
			else:
				print("35 ve 1 arasında sayı girin")
		else:
			print("sayı yazın")

def i2(list,a,gen,uzn):
	for i in range(uzn):
		list.append([])
		a=a+1
		for ii in range(gen):
			list[a].append(0)
	return list,a

def i3(list,gen,uzn):
	for i in range(10):
		rn1=random.randint(0,gen)
		rnd1=random.randint(0,uzn)
	try:
		list[rnd1][rn1]=2
	except:
		None
	return list,rn1,rnd1
	
def i4(list,gen,uzn):
	for i in range(10):
		rn2=random.randint(0,gen)
		rnd2=random.randint(0,uzn)
	try:
		list[rnd2][rn2]=1
	except:
		None
	return list ,rn2,rnd2

def i5(list,hm,gen,uzn,rn1,rnd1,rn2,rnd2):
	while True:
		hm=0
		ar=[]
		c=1
		d=1
		for i in list:
			for ii in i:
				ar=ar+[ii]
				hm=hm+1
		if 1 in ar:
			c=1
		else:
			c=0
		if 2 in ar:
			d=1
		else:
			d=0
		if d!=1:
			list,rn1,rnd1=i3(list,gen,uzn)
		if c!=1:
			list,rn2,rnd2=i4(list,gen,uzn)
		if c==1 and d==1:
			return list,rn1,rnd1,rn2,rnd2

gen,uzn=i1()
list,a=i2(list,a,gen,uzn)
list,rn1,rnd1=i3(list,gen,uzn)
list,rn2,rnd2=i4(list,gen,uzn)

while True:
	hm=0
	for i in list:
		for ii in i:
			hm=hm+1
		if hm==gen*uzn:
			hm=0
			list,rn1,rnd1,rn2,rnd2=i5(list,hm,gen,uzn,rn1,rnd1,rn2,rnd2)
	print("\n\n\n\n\n\n\n\n\n\n")
	print("\n\n\n\n\n\n\n\n\n\n")
	print("\n\n\n\n\n\n\n\n\n\n")
	print("\n\n\n\n\n\n\n\n\n\n")
	for i in list:
		print(i)
	print("puan = {} \n1-yukarı  2-aşağı \n3-sol  4-sağ \n0-çıkış".format(puan))
	ip=input(":")
	if ip=="1" and list[0][rn2]!=list[rnd2][rn2]:
		list[rnd2][rn2]=0
		rnd2=rnd2-1
		list[rnd2][rn2]=1
	elif ip=="2" and list[-1][rn2]!=list[rnd2][rn2]:
		list[rnd2][rn2]=0
		rnd2=rnd2+1
		list[rnd2][rn2]=1
	elif ip=="3" and list[rnd2][0]!=list[rnd2][rn2]:
		list[rnd2][rn2]=0
		rn2=rn2-1
		list[rnd2][rn2]=1
	elif ip=="4" and list[rnd2][-1]!=list[rnd2][rn2]:
		list[rnd2][rn2]=0
		rn2=rn2+1
		list[rnd2][rn2]=1
	elif ip=="0":
		break
	if list[rnd1][rn1]==1:
		puan=puan+1
