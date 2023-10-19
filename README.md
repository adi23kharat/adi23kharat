1 List the names Of all people living in
Ans:
' area.
select personfyl 00.pname from personfyl 00,areafy100 where
personfy100.ano=areafy100.ano and areafy100.atype='Rural':
PNAME
Vishal
Shekhar
Surai
Sarfrai
Rahul
Nilesh
2 List details of all people whose names start with the alphabet '_' & contains
maximum _alphabets in if.
select from personfy100 where pname like
MAX(PNAME)
Vyanktesh
OR
select from persfy41 where pname like'V%' group by pname
having pname=
(select max(pname) from persfy41
LENGTH(PNAME) PNAME
10
Vyankatesh
3 List the names of all people whose birthday falls in the month of
Ans:
select pname FROM personfy100 WHERE
select pname FROM personfy100 WHERE
select pname FROM personfy100 WHERE 12;
PNAME
Vishal
Shekhar
Sarfraj
4 Give the count of people who are born on
select count(pname) as Born_On_Same_Day from personfy100 WHERE
2
5 Give the count of people whose income is below
select count(pname) as Below_lncome from personfyl 00 where income<30000;
BELOW_INCOME
6- List names of all people whose income is between
and
select pname from personfy100 where income between 35000 and 55000:
PNAME
Shekhar
Sartaj
Rahul
Ajay
Dipak
7. List the names of people with average income
Ans:
select avg(distinct income).pname from personfy100 group by pname;
8. List the sum of incomes of people living in •
Ans:
select personfy100,ateafy100 where
personfyl 00.ano=areafy100.ano and
SUM(PERSONFYIOO.INCOME)
I SCCCO
9. List the names of the areas having people with maximum income (duplicate
areas must be omitted in the result)
select from personfyl 00.areafy100
where personfy100.ano•areafy100.ano group by areafy100.aname having
areafy 100. anamee' Pune';
MAX(PERSONFYIOO.INCOME) ANAME
Pune
OR
select areafy 100 an ame. personfv 1 00, pname,personfy 100.income from
personfy 1 OOrareafy100 where personfy 100.ano=oreaty 100.ano
and personfy 100.income
(select max(personfy100.income) from personfy100,areafy100 where
personfyl and areafyl );
IO. Give the count of people in each orea
select OO.aname from
personty100.areafy100 where peßonfy100.ano=areafy100.ano group by
areaty100-aname;
ANAME
3
2
Daund
Shirur
Nagar
Baramati
Pune
Indapur
Chennai
11. List the details of people Eving in '
' and having income greater than
select areatyl 00.aname.personfy100.pname,personfy 100.income.areafy 100.atype
from. personfy100.areaty100 where personty100.an0—areafy100.anO
and personfy100.income •
(select maxlpersontylCO.incomel from personfylOO.areafylOO where
personty 100. ono=areafy 100. ano
ond areafy 1m.atypelAUrban• r,
ANAME
FNAME
INCOME
ATYPE
Baramati Sutc*
125000
Rural
12. List the detois pt people, sorted by person number
select • from areafy100.persorty100 where order by
persontyl 00 .pno:
ANO ANAME
ATYPE PNO PNAME
BDATE
INCOME ANO
13. List the details of people, sorted by area, person name
Ans:
select personfyl from areafy100.personfy100 where
areafyl 00.ano•personfy100.ano order by areafy100.anamewpersonfy100.pname:
PNAME
Shekhar
Suraj
Vishal
Ajay
Nilesh
Sarfraj
Dipak
Gorakh
Vyanktesh
Rahul
ANAME
Baramati
Baramati
Baramati
Chennai
Daund
Indapur
Nagar
Pune
Pune
Shirur
14. List the minimum income of people.
Ans:
select from areafy100,personfy100 where
areafy 100.ano•personfy 100.ano :
MIN(PERSONFYIOO.INCOME)
25000
OR
select min(personfyl 00.atype from areafyl 00,persontYI 00 Where
areafy100.ano=personfyIOO.ano group by areafy100.atype having
areafyl
MIN(PERSONFYIOO.INCOME) ATYPE
Rural
OR
select min(personfyl 00. atype from areafyl 00,personfy100 where
areafy100.ano=personfy100.ano group by areafyIOO.atype having
MIN(PERSONFYIOO.INCOME) ATYPE
Urban
15. Transfer all people living in •pune• to •mumbai'.
update areafy100 set anamez'Mumbai' where aname='Pune•;
select • from areafy100 where aname='Mumbai'•.
ANO ANAME
ATYPE
3 Mumbai Urban
4
Mumbai Urban
16, Delete information of all people staying in 'urban' area
delete from areafyl 00 where atype-'Urban':
4 row(s) deleted.
select • from areafy100;
ANO ANAME
1 Baramati
2
Indapur
ATYPE
Rural
Rural
SET.c
create table efy100
(eno number(3)primary key.
ename varchar2(15).
sal number(10),
gender varchar2(6),
addr varchar2( 1 S));
insert all
into efy1CO values( 1
into efyl 00 'Nagar J
into efy 100 values13,
into efy 100 values14„ 'Komal'
into efy 100
into efy 100 values(6, Sami'
select • from dual;
select • from efylOO;
ENO ENAME
2
3
S
6
Samir
Revati
Abhiram
Komal
Anita
Samir
SAL
45000
37000
GENDER
Male
Fern Ole
Male
Female
Female
Male
ADDR
Sa tara
Nagar
Baramati
pune
Murnbai
Pune
create table prfy100
(pno key,
pname varchar2( 15),
control varchar2(1 S),
budget number( 10)):
insert all
into prfylOO values( 'Account', 120000)
into pdylOO
into prfy 100 values(3. 'Work Capital', Finance', 1200000)
info prfyl 00 values(4. 'Capital', 'Finance', 400000)
into prfylCO values(S Computed .20000000)
into prfylCO values(6.'ML'.'Computer'.10000000)
select • from dual:
PNO PNAME
2
3
4
5
6
CONTROL
ERP
Account
SAP
Account
Work Capital
Finance
Capital
ML
Finance
Computer
Computer
BUDGET
120000
220C00
1200000
400000
20000000
10000000
Department(dno.dname)
create table dptfy100
(dno
key.
dnarne varchar2(lS));
Insett an
into dptfy100 values(
into dptfYIOO values(102Finance'J
into dptfYIOO values(
into dptfYlOO
into dptfytco
select • from dual:
select • from dpffy100:
ONO DNAME
105
Inventory
Computer
workson(eno.pno.dno.hrs)
create table wonfyl 00
eno efyl delete cascade,
pno prfyl OO(pnolon delete cascade,
dno dptfy1001dno)on delete cascade,
hrs number12)
insert into wonfy100 values( 1.101 ,8):
insert into wonfy 100 values(2.2.102.8);
insert into wonfylOO values(2, I. 101.2):
insert into wonfy 100 values(3.3.103.81:
insert into wonfylOO values(44.103.8);
insert into wonfy 100 valuest4.3, 103.2);
insert into wonfyl 00 values(5.3.105.2);
insert into wonfylOO 104.8):
insert into wonfy100
insert into wonfylCO values(5.5.105.2):
insert into wonfy I OO 104. O);
insert into wonfy 100 values(6.5.105.21:
insert into wonfy 100 values(4.S.105.12);
select •from wontyl 00;/seJect •from wonfy 100 order by dno:
ENO PNO DNO
2
2
4
2
.4
101
102
103
HRS
8
2
8

3
6
6
s
6
4
3
3
4
s
103
103
105
2
8
10
12
Que. Est the narnes of depcytments that controls projects whose budget is greater
thon XLakh.
Ans: select distinct control.budget from pdyl 00 where budget>200000:
CONTROL
Ftr.,ance
Account
Finance
BUDGET
20000000
1200000
10000000
220000
400003
Que.2 list the names of projects, controlled by department No 102. whose budget is
greater than otleast one project controlled by department No 101
select prfyl 00.pname.pdy100.budgei.prfy10Ccontrol.dptfy100dno from
ety100.prfy1Ø.dptty100.wonfy100 where efyl 00.eno•wonty100.en0 and
and dptty100.dno=wonfy100.dno and dptfyl 00.dnoz102
and ptfy 100 .budget>
(seQt 100.budgetl from ety 100,pffy 100.dptfY 100 where
1 OO_eno and prfy 100.pnozwonfyI 00, pno and
dpttv and dpttylOO.dn0= 101) :
PNAME
BUDGET CONTROL ONO
SAP
Account 102
Que.3. list the details of the projects with second maximum budget
Ans:
select distinct prfYI 00.pname.prfYIOO.budget,prfyIOO.confr01.dpffyIOO.dno from
where efy100.enozwonfy100.eno and
prfy100.pnozwonfy100.pno and dptfyl 00.dnozwonfy100.dno and pdy100.budget=
(select max(prty100.budget) from efyl 00.prfy100.dptfy100.wonfy100 where
efyl 00.eno=wonfy100.eno and prfy100.pno=wonfy100.pno and
dptfyl 00.dno=wonfy100.dno and prty100.budget<
(select max(pdyl 00.budget) from prfyl 00)) :
ML
BUDGET CONTROL DNO
10000000 Computer 104
Que.4. fist the details of the projects with third maximum budget.
select distinct from
where efy100.enozwonfy 100.eno and
prfyl 00. pno=wonfy 100.pno and dptfy 100.dno•wonfy 100.dno and prfy 100.budget
(select max(prfyl 00.budget) from efyl 00. prfyl 00.dptfy100.wonfy 100 where
efy100.eno=wonfy100.eno and prfy and
dptfy100.dno=wonfy100.dno and pdy100.budget
(select max(prfy 100.budget) from prfy100 where prfylOO.budget
(select max(prfylOO.budget) from prfylOOllJ :
PNAME
Work Capital
Work Capital
BUDGET CONTROL
1200000 finance
1200000 Finance
ONO
103
105
Gue.5. list the names of employees, working on some projects that employee
number 3 is working.
select 00. ename.pdy100.pname from etyl OO.prfy100,dptfy1 oo,wonfyl 00 where
em neno-wonty100.eno and prfy100.pnozwonty100,pno and
dptfy100.dno=wontyl 00.dnv ond prfy100.pname=
(select pcty100.pname from efy100,pdy100.dpffy1 oo,wonfyl 00 where
etaneno-wonty100.eno and prfy100.pnozwonfy1 oo.pno and
dpffy and efy 100.eno=3)
ENAME
Abhiram
Komal
PNAME
Work Capital
Wctk Capital
Capital
Que.6. list the names of emooyees who do not work on any project that employee
number 3 works on
select ety100.ename.prty100.pname from efyl 00.prfy100,dpffy100.wonfy100 where
efy100.eno•w0nfy100.eno and prtyl 00.pno=wonfy100.pno and
dptfy100.dnozwonfy 100. dno and prfy100-pname'=
(select distinct prty100.pname from 100.prfy100,dptfy100.wonfy100 where
ety100.eno=wonfy100.eno and pdy100.pno•wonfy100.pno and
dptfy100. dnozwonfy 100.dno and efyl 00.enoe3)
Revati
Revati
Sam*
Anita
Anita
PNAME
ERP
SAP
ERP
Capital
Capital
ML
Al
Gue.7. list the names of employees who do not work on any project controlled
bVAccount' department
Ans:
select efyl from
efy100.prfy100.dptfy100.wonfy100 where efyl 00.eno•wonfy100.eno and
prty100.pno=wonfy100.pno and dptfyl 00.dno=wonfy100.dno and prfy100.pname/=
(select prty 100.pname from where
ety100.eno•wonty100.eno and prfyl 00.pno•wonfy100.pno and
dptty100.dno=wonfy100.dno and dptfy100.dname•'Account')
ENAME
Revati
Abhiram
Komal
Komal
Anita
Anita
Anita
PNAME
SAP
Work Capital
Capital
Work Capital
Work Capital
Capital
Al
ML
DNAME
Finance
Sales
Sales
Computer
inventory
Computer
Computer
Inventory
Computer
Que.8. list the names of ptojects along with the controlling department name. fry
those projects which has atleast I employees working on it.
select 100.pname.prfy100. control from
efy100,prfy100. dpffyl 00,wonfy100 where efy100-eno•wonfy 100.eno and
prfyl 00.pno=wonfy100.pno and dptfyl 00.dno•wonfy100.dno group by
prfy100.pname,pdy100.control having count(efyl
FNAME
COUNT(EFYIOO.ENO)
ML
SAP
CONTROL
Computer
Account
Que.9. list the names of employees who is wtyked for more than IO hrs on atteasf
one project controled by Computer' dept.
select efy10Qename.wonty100.hrs from where
efy100.eno=wonfy100.eno and prfy100.pno=wonfy100.pno and
dptfy100.dno=wonfy100.dno and dptfy100.dname—'Computer' and wonfy100.hrs> 10:
ENAME
HRS
12
Que. IO. list the names of employees . who are males . and earning the maximum
salary in their department.
select distinct efy100.ename,dptfy100.dname.efy100.sal from
etYIOO.prfy100.dpffy100.wonfY100 where efyl oo.eno=wonfyl 00. eno and
prfy100.pno•wonty100.pno and dptfy100.dnozwonfy100.dno and
ety100.gender•'Male' order by ety100.ename:
ENAME DNAME SAL
Abhirarn Sales
Account 35000
Computer 35000
Inventory 3SCOO
Que.n. list the names Of employees Who in the same department as •Finance
select distinct efy100.ename.dptfy100.dnarne from
efy100.PdY100,dpffYIOO.wonfY100 where etYIOO.eno=wonfYIOO.eno and
prfy100.pno=wontY1 oo.pno and dptfyl OCdno-wonfy100.dno and
ENAME
DNAME
Revati
Finance
Que. 12. rtst the names of employees Who do not Eve in
or
ety100.0ddrnot
ENAME
Revati
Abhiram
ADDR
Satora
Nagar
Baramati
SET. D
create table movfy100(mno number(31 key,mname varchar2(
number(
insert all
into movtY100 ,
into movtylOO votues12'DDLG'.1986. I OOCOOCOO)
into movmoo votues13,'K3G'.201
into movfylOO
into movfy 100
into movfy 100
select • from
select • from movtyl 00;
MNO MNAME
2
3
4
5
6
Dil
DOLG
K3G
K2H2
Devdas
Krish
RYR
1 986
2011
2010
2009
2005
BUDGET
200C0003
1 cocooooo
3cocoooo
350000C00
410000COO
52cocooco
create table acffy100(ano numbert3)primary key.aname varchar211 Slerole
varchar2( 15J.chorge number( varcnar2( S) l;
insert all
into octyl 00 volves(l
into octfy100
into actfy 100 volves(3, 'Hri'ik
into actfy 100
3000COO,Mumb0i'J
into octfyl 00 values(SKajol'.'ACfess
30003T.'Mumban
nto acttylOO valuest6.'Arnrish puri.Vi110in.
into
into
select • from dual:
select • trom octyl 00,
ANO ANAME
2
3
4
S
6
7
9
Shahrukh
Amir Khan
Hritik Roshan
Preeti Inta
Kaid
Amrish Puri
Anupæ-n Khet
Ajay Devgan
Lead
Lead
Actress
Actress
Vibain
Father
Sidekick
CHARGE
35000000
400000C0
20000000
30C0000
30C0000
3000000
20COOOO
soocoo
ADDR
Mumbai
Mumbai
Mumbai
Mumbai
Mumbai
Mumbai
Mumbai
Mumbai
create table prody100(pid rumber13)prirnary key.pname vorchar2( 1 5) .padc±
varchar2( I
hserf au
into gyodfy ICO valuesli .Tn&a Kumar'.uumbai)
into 00 valuesf2.•Yash Chopra'.•Mumbai')
into prodty 100 values(3.'Yash Johor' , •Mumbai')
into prodfylOO voboest4,'Bhatat
into prodty 100 Roshan','Mumbai•)
into prodfy ICO values16.•Ash0k
select• from dud:
selecf• from prodfyl 00:
PID
2
PNAME
Indra Kumcr
Yash Chopra
PADDR
Mumbai
3
S
6
Yash Johar
Bharat Shaha
Rakesh Roshan
Ashok Thakeria
Rohit Shetty
Mumbai
Mumbai
Murnboi
Mumbai
Mumbai
create table mapfyl 00
mno number131references movfy OOIrnno)ON DELETE CASCADE.
ano octfylOOlon010N DELETE CASCADE.
pid number (31 references ptodty I DELETE CASCADE
insert o"
into mopfy ICO valLjeS( .2. I )
into mapfy 100 valuesl 1.7.6)
into mapfylOO vooes(2.1.21
into mapfy 100 values(2S2)
into mopfy 100 values12.6.2)
into mapfYIOO veuest3. I .31
into mapfy ICO values(3.3.3)
into mapfy 100 values13.5.3J
into mapfy 100 values141.31
Tito mapfyl 00
into moptylCO 1
into mopfy100
into mopfylCO values16,4.5)
into mcpfylOO
select • from dual:
select • from mapty100:
MNO ANO PID
2
Que.l. List the names of actors who have acted in at least one movie. in
which •shoh,rukh' has acted.
select actfyl 00.aname.movfy100.mname from movfy100.actfy100 .prodfyl 00.
mapfy100 where movty100.mno=mapty100.mno and actfy100.anozmapfy100.anO
and prodyl 00. pid•mapty100.pid and movty100.mname
order by movtyl 00.mnome:
ANAME
Arnrish Puri
Sham.Jkh
Shanrukh
Kajol
Shahrukh
MNAME
DOLG
DDLG
DOLG
Devdas
K2H2
K2H2
K3G
Hritik Roshan K3G
Que.2. List the names of movies with the highest budget.
select mname.budget from movfy100 where budget:
(select max(budget) from movfyl 00
MNAME
Krish
Highest
520ccccco
Que.3. List the names of movies with the second highest budget
select mname,budget from rnovfyl 00 where budgeta
(select max(budget) from movtyl 00 where budget<
(select max(budget) from movfy100) );
MNAME
SECOND_HIGHEST
Devdas
410000000
Que.4- List the names of actors who have acted the maximum number of
movies.
Ans:
select actfy100.aname.countC) as from
movfyl 00.actfy 100,prodfy 100.mapfy 100 where movfyl 00.mno=mapfy100.mno and
actfy100.ano•mapfy100.ano and prodfy100.pid=mapfy100.pld group by
actfy100,aname having
(select
(select count(movfy100, mno)as c from
where movfylOO.mnozmapfy100,mno and actfy100.ano•mapfy100.ano and
group by actfy100.aname));
ANAME
Shahrukh
4
ed by more than one producer.
Ques. List names of movies. produc
from
moot n acttytoo.prodtytoo.mapty100 where movfyl OO.mno=mapfy100.mno and
and prod-y' oo.pid-mapfy100.pid and movfy100.mno-
(select count(movty100.mno) from movfy100 where mno=2):
MNAME
MNO PNAUE
Dil
Kuma
Ashok Thakeria Di
Gue.6. List the names of actors who ate given with the maximum Charges
fcy the'
select Charge from
movfy100.octty1Øgodfy100.mapty100 where movfy100.mno=mapfy100.mno and
octylWano=rnapty100.ano and actfy100.chargez
(seet from octfyl 00);
ANAHE CHARGE
Khan acomcoo
Que.7. List tt•e names of producers who produce the same movie as
select movtyl 00.mname.prodfy100. pname from
where movfy100.mno•mapty100.mnO and
and ptodfy100.pid•mapfy100.pid and
MNAME PNAME
Dd ln&a Kuma
Oil Ashok Thake"a
Que.8. List the names of actors who do not live in
or _
select aname .addr from acffy100 where and
ANAME
preeti Zinta
Anupam Kher
ADDR
Punjab
Himachal
