{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The situation is, customers are providing some personal informations while purchasing stuff on-line or in-store. For some reasons, a client wants to know the answer to some of his questions from the dataset."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "current working directory on your computer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "'C:\\\\Users\\\\Stevy\\\\Documents\\\\Course-Material\\\\Course_Material\\\\S_4_Pandas_DA'"
      ]
     },
     "execution_count": 1,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "import os\n",
    "cwd = os.getcwd()\n",
    "cwd"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [],
   "source": [
    "#importing pandas\n",
    "import pandas as pd"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "load the data in a variable \"cust\", data file name is 'Cust_Purch_FakeData.csv'."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [],
   "source": [
    "cust = pd.read_csv('Cust_Purch_FakeData.csv')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "display first 5 rows of your data-set."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>prefix</th>\n",
       "      <th>first</th>\n",
       "      <th>last</th>\n",
       "      <th>email</th>\n",
       "      <th>gender</th>\n",
       "      <th>age</th>\n",
       "      <th>company</th>\n",
       "      <th>profession</th>\n",
       "      <th>phone</th>\n",
       "      <th>postal</th>\n",
       "      <th>province</th>\n",
       "      <th>cc_no</th>\n",
       "      <th>cc_exp</th>\n",
       "      <th>cc_type</th>\n",
       "      <th>price(CAD)</th>\n",
       "      <th>fav_color</th>\n",
       "      <th>ip</th>\n",
       "      <th>weekday</th>\n",
       "      <th>ampm</th>\n",
       "      <th>date</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Dr.</td>\n",
       "      <td>Ray</td>\n",
       "      <td>Morton</td>\n",
       "      <td>sebvajom@kol.km</td>\n",
       "      <td>Male</td>\n",
       "      <td>38</td>\n",
       "      <td>Medtronic Inc.</td>\n",
       "      <td>Health Therapist</td>\n",
       "      <td>(987) 619-2695</td>\n",
       "      <td>B6V 3W3</td>\n",
       "      <td>MB</td>\n",
       "      <td>5020000000000230</td>\n",
       "      <td>05/2018</td>\n",
       "      <td>Solo</td>\n",
       "      <td>8.36</td>\n",
       "      <td>Blue</td>\n",
       "      <td>126.23.139.2</td>\n",
       "      <td>Sunday</td>\n",
       "      <td>pm</td>\n",
       "      <td>04/05/1930</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Miss</td>\n",
       "      <td>Claudia</td>\n",
       "      <td>Rodriquez</td>\n",
       "      <td>acu@jatsot.ug</td>\n",
       "      <td>Female</td>\n",
       "      <td>51</td>\n",
       "      <td>Ames Department Stores, Inc.</td>\n",
       "      <td>Health Therapist</td>\n",
       "      <td>(356) 736-7352</td>\n",
       "      <td>G7M 5F3</td>\n",
       "      <td>SK</td>\n",
       "      <td>5020000000000230</td>\n",
       "      <td>07/2028</td>\n",
       "      <td>Visa</td>\n",
       "      <td>68.31</td>\n",
       "      <td>Black</td>\n",
       "      <td>106.198.76.211</td>\n",
       "      <td>Tuesday</td>\n",
       "      <td>am</td>\n",
       "      <td>12/20/1926</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Miss</td>\n",
       "      <td>Harry</td>\n",
       "      <td>Meyer</td>\n",
       "      <td>zuz@lo.wf</td>\n",
       "      <td>Female</td>\n",
       "      <td>51</td>\n",
       "      <td>CSX Corp.</td>\n",
       "      <td>Political Scientist</td>\n",
       "      <td>(539) 246-1806</td>\n",
       "      <td>A0Z 6P9</td>\n",
       "      <td>NS</td>\n",
       "      <td>6300000000000000</td>\n",
       "      <td>02/2023</td>\n",
       "      <td>Switch</td>\n",
       "      <td>34.65</td>\n",
       "      <td>Black</td>\n",
       "      <td>186.150.187.29</td>\n",
       "      <td>Wednesday</td>\n",
       "      <td>pm</td>\n",
       "      <td>08/20/1931</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Miss</td>\n",
       "      <td>Edith</td>\n",
       "      <td>Gilbert</td>\n",
       "      <td>hansohsi@jupec.md</td>\n",
       "      <td>Female</td>\n",
       "      <td>55</td>\n",
       "      <td>Murphy Oil Corporation</td>\n",
       "      <td>Transportation Manager</td>\n",
       "      <td>(984) 962-7494</td>\n",
       "      <td>P9I 9H3</td>\n",
       "      <td>YT</td>\n",
       "      <td>3530000000000000</td>\n",
       "      <td>02/2028</td>\n",
       "      <td>Maestro</td>\n",
       "      <td>64.59</td>\n",
       "      <td>White</td>\n",
       "      <td>80.140.57.161</td>\n",
       "      <td>Saturday</td>\n",
       "      <td>am</td>\n",
       "      <td>06/18/2001</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Dr.</td>\n",
       "      <td>Lura</td>\n",
       "      <td>Murphy</td>\n",
       "      <td>webediti@je.st</td>\n",
       "      <td>Female</td>\n",
       "      <td>20</td>\n",
       "      <td>PETsMART Inc</td>\n",
       "      <td>Statistician</td>\n",
       "      <td>(902) 568-9748</td>\n",
       "      <td>S1A 6K0</td>\n",
       "      <td>ON</td>\n",
       "      <td>4030000000000000</td>\n",
       "      <td>10/2025</td>\n",
       "      <td>Diners Club International</td>\n",
       "      <td>20.83</td>\n",
       "      <td>Yellow</td>\n",
       "      <td>211.103.43.41</td>\n",
       "      <td>Friday</td>\n",
       "      <td>pm</td>\n",
       "      <td>06/14/2045</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "  prefix    first       last              email  gender  age  \\\n",
       "0    Dr.      Ray     Morton    sebvajom@kol.km    Male   38   \n",
       "1   Miss  Claudia  Rodriquez      acu@jatsot.ug  Female   51   \n",
       "2   Miss    Harry      Meyer          zuz@lo.wf  Female   51   \n",
       "3   Miss    Edith    Gilbert  hansohsi@jupec.md  Female   55   \n",
       "4    Dr.     Lura     Murphy     webediti@je.st  Female   20   \n",
       "\n",
       "                        company              profession           phone  \\\n",
       "0                Medtronic Inc.        Health Therapist  (987) 619-2695   \n",
       "1  Ames Department Stores, Inc.        Health Therapist  (356) 736-7352   \n",
       "2                     CSX Corp.     Political Scientist  (539) 246-1806   \n",
       "3        Murphy Oil Corporation  Transportation Manager  (984) 962-7494   \n",
       "4                  PETsMART Inc            Statistician  (902) 568-9748   \n",
       "\n",
       "    postal province             cc_no   cc_exp                    cc_type  \\\n",
       "0  B6V 3W3       MB  5020000000000230  05/2018                       Solo   \n",
       "1  G7M 5F3       SK  5020000000000230  07/2028                       Visa   \n",
       "2  A0Z 6P9       NS  6300000000000000  02/2023                     Switch   \n",
       "3  P9I 9H3       YT  3530000000000000  02/2028                    Maestro   \n",
       "4  S1A 6K0       ON  4030000000000000  10/2025  Diners Club International   \n",
       "\n",
       "   price(CAD) fav_color              ip    weekday ampm        date  \n",
       "0        8.36      Blue    126.23.139.2     Sunday   pm  04/05/1930  \n",
       "1       68.31     Black  106.198.76.211    Tuesday   am  12/20/1926  \n",
       "2       34.65     Black  186.150.187.29  Wednesday   pm  08/20/1931  \n",
       "3       64.59     White   80.140.57.161   Saturday   am  06/18/2001  \n",
       "4       20.83    Yellow   211.103.43.41     Friday   pm  06/14/2045  "
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust.head()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    " How many entries your data have?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "<class 'pandas.core.frame.DataFrame'>\n",
      "RangeIndex: 30000 entries, 0 to 29999\n",
      "Data columns (total 20 columns):\n",
      "prefix        30000 non-null object\n",
      "first         30000 non-null object\n",
      "last          30000 non-null object\n",
      "email         30000 non-null object\n",
      "gender        30000 non-null object\n",
      "age           30000 non-null int64\n",
      "company       30000 non-null object\n",
      "profession    30000 non-null object\n",
      "phone         30000 non-null object\n",
      "postal        30000 non-null object\n",
      "province      30000 non-null object\n",
      "cc_no         30000 non-null int64\n",
      "cc_exp        30000 non-null object\n",
      "cc_type       30000 non-null object\n",
      "price(CAD)    30000 non-null float64\n",
      "fav_color     30000 non-null object\n",
      "ip            30000 non-null object\n",
      "weekday       30000 non-null object\n",
      "ampm          30000 non-null object\n",
      "date          30000 non-null object\n",
      "dtypes: float64(1), int64(2), object(17)\n",
      "memory usage: 4.6+ MB\n"
     ]
    }
   ],
   "source": [
    "cust.info()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    " The max and min ages of your customer. Find mean of your customer."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Max. age of the customer is: 65\n",
      "Min. age of the customer is: 18\n",
      "Avg. age of the customer is: 41.550066666666666\n"
     ]
    }
   ],
   "source": [
    "print('Max. age of the customer is:', cust['age'].max())\n",
    "print('Min. age of the customer is:', cust['age'].min())\n",
    "print('Avg. age of the customer is:', cust['age'].mean())"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "the three most common customer's names"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Willie     130\n",
       "Francis    124\n",
       "Eula        86\n",
       "Name: first, dtype: int64"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust['first'].value_counts().head(n=3)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Two customers have the same phone number,find those customers."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(263) 382-8004    2\n",
       "(759) 301-6886    1\n",
       "(857) 427-6949    1\n",
       "Name: phone, dtype: int64"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust['phone'].value_counts().head(n=3)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The customer who has the same phone number"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>prefix</th>\n",
       "      <th>first</th>\n",
       "      <th>last</th>\n",
       "      <th>email</th>\n",
       "      <th>gender</th>\n",
       "      <th>age</th>\n",
       "      <th>company</th>\n",
       "      <th>profession</th>\n",
       "      <th>phone</th>\n",
       "      <th>postal</th>\n",
       "      <th>province</th>\n",
       "      <th>cc_no</th>\n",
       "      <th>cc_exp</th>\n",
       "      <th>cc_type</th>\n",
       "      <th>price(CAD)</th>\n",
       "      <th>fav_color</th>\n",
       "      <th>ip</th>\n",
       "      <th>weekday</th>\n",
       "      <th>ampm</th>\n",
       "      <th>date</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>15</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Lilly</td>\n",
       "      <td>Tyler</td>\n",
       "      <td>kofadu@itohi.tf</td>\n",
       "      <td>Female</td>\n",
       "      <td>38</td>\n",
       "      <td>CSX Corp.</td>\n",
       "      <td>Structural Engineer</td>\n",
       "      <td>(263) 382-8004</td>\n",
       "      <td>V7K 1E3</td>\n",
       "      <td>ON</td>\n",
       "      <td>30000000000000</td>\n",
       "      <td>11/2022</td>\n",
       "      <td>Diners Club Carte Blanche</td>\n",
       "      <td>9.61</td>\n",
       "      <td>Yellow</td>\n",
       "      <td>74.124.37.227</td>\n",
       "      <td>Saturday</td>\n",
       "      <td>am</td>\n",
       "      <td>03/30/1985</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>16</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Peter</td>\n",
       "      <td>Cain</td>\n",
       "      <td>megkosig@anazeor.gn</td>\n",
       "      <td>Male</td>\n",
       "      <td>27</td>\n",
       "      <td>Campbell Soup Co.</td>\n",
       "      <td>Insurance Adjuster</td>\n",
       "      <td>(263) 382-8004</td>\n",
       "      <td>E8T 2B4</td>\n",
       "      <td>YT</td>\n",
       "      <td>3530000000000000</td>\n",
       "      <td>03/2024</td>\n",
       "      <td>Solo</td>\n",
       "      <td>13.74</td>\n",
       "      <td>Black</td>\n",
       "      <td>25.207.141.135</td>\n",
       "      <td>Tuesday</td>\n",
       "      <td>am</td>\n",
       "      <td>08/05/1950</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   prefix  first   last                email  gender  age            company  \\\n",
       "15   Mrs.  Lilly  Tyler      kofadu@itohi.tf  Female   38          CSX Corp.   \n",
       "16   Mrs.  Peter   Cain  megkosig@anazeor.gn    Male   27  Campbell Soup Co.   \n",
       "\n",
       "             profession           phone   postal province             cc_no  \\\n",
       "15  Structural Engineer  (263) 382-8004  V7K 1E3       ON    30000000000000   \n",
       "16   Insurance Adjuster  (263) 382-8004  E8T 2B4       YT  3530000000000000   \n",
       "\n",
       "     cc_exp                    cc_type  price(CAD) fav_color              ip  \\\n",
       "15  11/2022  Diners Club Carte Blanche        9.61    Yellow   74.124.37.227   \n",
       "16  03/2024                       Solo       13.74     Black  25.207.141.135   \n",
       "\n",
       "     weekday ampm        date  \n",
       "15  Saturday   am  03/30/1985  \n",
       "16   Tuesday   am  08/05/1950  "
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[cust['phone'] == '(263) 382-8004']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "How many customers have profession \"Structural Engineer\"?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "87"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[cust['profession'] == 'Structural Engineer'].count()['last']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "prefix        87\n",
       "first         87\n",
       "last          87\n",
       "email         87\n",
       "gender        87\n",
       "age           87\n",
       "company       87\n",
       "profession    87\n",
       "phone         87\n",
       "postal        87\n",
       "province      87\n",
       "cc_no         87\n",
       "cc_exp        87\n",
       "cc_type       87\n",
       "price(CAD)    87\n",
       "fav_color     87\n",
       "ip            87\n",
       "weekday       87\n",
       "ampm          87\n",
       "date          87\n",
       "dtype: int64"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[cust['profession'] == 'Structural Engineer'].count()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "How many male customer are 'Structural Engineer'?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "prefix        43\n",
       "first         43\n",
       "last          43\n",
       "email         43\n",
       "gender        43\n",
       "age           43\n",
       "company       43\n",
       "profession    43\n",
       "phone         43\n",
       "postal        43\n",
       "province      43\n",
       "cc_no         43\n",
       "cc_exp        43\n",
       "cc_type       43\n",
       "price(CAD)    43\n",
       "fav_color     43\n",
       "ip            43\n",
       "weekday       43\n",
       "ampm          43\n",
       "date          43\n",
       "dtype: int64"
      ]
     },
     "execution_count": 12,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[(cust['profession'] == 'Structural Engineer')\n",
    "     & (cust['gender'] == 'Male')].count()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "the female Structural Engineer from province Alberta(AB)?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>prefix</th>\n",
       "      <th>first</th>\n",
       "      <th>last</th>\n",
       "      <th>email</th>\n",
       "      <th>gender</th>\n",
       "      <th>age</th>\n",
       "      <th>company</th>\n",
       "      <th>profession</th>\n",
       "      <th>phone</th>\n",
       "      <th>postal</th>\n",
       "      <th>province</th>\n",
       "      <th>cc_no</th>\n",
       "      <th>cc_exp</th>\n",
       "      <th>cc_type</th>\n",
       "      <th>price(CAD)</th>\n",
       "      <th>fav_color</th>\n",
       "      <th>ip</th>\n",
       "      <th>weekday</th>\n",
       "      <th>ampm</th>\n",
       "      <th>date</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>8858</th>\n",
       "      <td>Dr.</td>\n",
       "      <td>Roy</td>\n",
       "      <td>Stanley</td>\n",
       "      <td>apiunvo@ehasom.ir</td>\n",
       "      <td>Female</td>\n",
       "      <td>39</td>\n",
       "      <td>Cincinnati Financial Corp.</td>\n",
       "      <td>Structural Engineer</td>\n",
       "      <td>(876) 758-2929</td>\n",
       "      <td>N5A 6L2</td>\n",
       "      <td>AB</td>\n",
       "      <td>6300000000000000</td>\n",
       "      <td>02/2022</td>\n",
       "      <td>InstaPayment</td>\n",
       "      <td>31.86</td>\n",
       "      <td>Red</td>\n",
       "      <td>165.249.159.57</td>\n",
       "      <td>Sunday</td>\n",
       "      <td>pm</td>\n",
       "      <td>12/25/1903</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>9058</th>\n",
       "      <td>Mr.</td>\n",
       "      <td>Lora</td>\n",
       "      <td>Kennedy</td>\n",
       "      <td>dennap@rabac.se</td>\n",
       "      <td>Female</td>\n",
       "      <td>51</td>\n",
       "      <td>BJ Services Company</td>\n",
       "      <td>Structural Engineer</td>\n",
       "      <td>(305) 786-6959</td>\n",
       "      <td>N3R 4B7</td>\n",
       "      <td>AB</td>\n",
       "      <td>201000000000000</td>\n",
       "      <td>06/2019</td>\n",
       "      <td>Diners Club United States &amp; Canada</td>\n",
       "      <td>53.29</td>\n",
       "      <td>Black</td>\n",
       "      <td>42.216.243.206</td>\n",
       "      <td>Thursday</td>\n",
       "      <td>pm</td>\n",
       "      <td>06/06/2028</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>24736</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Nell</td>\n",
       "      <td>Richards</td>\n",
       "      <td>dob@me.ki</td>\n",
       "      <td>Female</td>\n",
       "      <td>18</td>\n",
       "      <td>Telephone &amp; Data Systems Inc</td>\n",
       "      <td>Structural Engineer</td>\n",
       "      <td>(262) 681-5018</td>\n",
       "      <td>N3Y 3G2</td>\n",
       "      <td>AB</td>\n",
       "      <td>347000000000000</td>\n",
       "      <td>07/2028</td>\n",
       "      <td>American Express</td>\n",
       "      <td>76.28</td>\n",
       "      <td>Blue</td>\n",
       "      <td>91.16.30.156</td>\n",
       "      <td>Wednesday</td>\n",
       "      <td>pm</td>\n",
       "      <td>07/14/1951</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>29865</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Don</td>\n",
       "      <td>McDaniel</td>\n",
       "      <td>naf@zudu.bj</td>\n",
       "      <td>Female</td>\n",
       "      <td>37</td>\n",
       "      <td>Anadarko Petroleum Corporation</td>\n",
       "      <td>Structural Engineer</td>\n",
       "      <td>(238) 789-2825</td>\n",
       "      <td>B4A 8Q9</td>\n",
       "      <td>AB</td>\n",
       "      <td>5610000000000000</td>\n",
       "      <td>12/2022</td>\n",
       "      <td>Mastercard</td>\n",
       "      <td>62.71</td>\n",
       "      <td>Blue</td>\n",
       "      <td>162.233.117.142</td>\n",
       "      <td>Sunday</td>\n",
       "      <td>pm</td>\n",
       "      <td>11/03/1989</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "      prefix first      last              email  gender  age  \\\n",
       "8858     Dr.   Roy   Stanley  apiunvo@ehasom.ir  Female   39   \n",
       "9058     Mr.  Lora   Kennedy    dennap@rabac.se  Female   51   \n",
       "24736   Mrs.  Nell  Richards          dob@me.ki  Female   18   \n",
       "29865   Mrs.   Don  McDaniel        naf@zudu.bj  Female   37   \n",
       "\n",
       "                              company           profession           phone  \\\n",
       "8858       Cincinnati Financial Corp.  Structural Engineer  (876) 758-2929   \n",
       "9058              BJ Services Company  Structural Engineer  (305) 786-6959   \n",
       "24736    Telephone & Data Systems Inc  Structural Engineer  (262) 681-5018   \n",
       "29865  Anadarko Petroleum Corporation  Structural Engineer  (238) 789-2825   \n",
       "\n",
       "        postal province             cc_no   cc_exp  \\\n",
       "8858   N5A 6L2       AB  6300000000000000  02/2022   \n",
       "9058   N3R 4B7       AB   201000000000000  06/2019   \n",
       "24736  N3Y 3G2       AB   347000000000000  07/2028   \n",
       "29865  B4A 8Q9       AB  5610000000000000  12/2022   \n",
       "\n",
       "                                  cc_type  price(CAD) fav_color  \\\n",
       "8858                         InstaPayment       31.86       Red   \n",
       "9058   Diners Club United States & Canada       53.29     Black   \n",
       "24736                    American Express       76.28      Blue   \n",
       "29865                          Mastercard       62.71      Blue   \n",
       "\n",
       "                    ip    weekday ampm        date  \n",
       "8858    165.249.159.57     Sunday   pm  12/25/1903  \n",
       "9058    42.216.243.206   Thursday   pm  06/06/2028  \n",
       "24736     91.16.30.156  Wednesday   pm  07/14/1951  \n",
       "29865  162.233.117.142     Sunday   pm  11/03/1989  "
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[(cust['profession'] == 'Structural Engineer')\n",
    "     & (cust['gender'] == 'Female')\n",
    "     & (cust['province'] == 'AB')]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The max, min and average spending"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Max. spending: 100.0\n",
      "Min. spending: 0.0\n",
      "Avg. spending: 49.990775000000184\n"
     ]
    }
   ],
   "source": [
    "print('Max. spending:', cust['price(CAD)'].max())\n",
    "print('Min. spending:', cust['price(CAD)'].min())\n",
    "print('Avg. spending:', cust['price(CAD)'].mean())"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Who did not spend anything? Company wants to send a deal to encourage the customer to buy stuff!"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>prefix</th>\n",
       "      <th>first</th>\n",
       "      <th>last</th>\n",
       "      <th>email</th>\n",
       "      <th>gender</th>\n",
       "      <th>age</th>\n",
       "      <th>company</th>\n",
       "      <th>profession</th>\n",
       "      <th>phone</th>\n",
       "      <th>postal</th>\n",
       "      <th>province</th>\n",
       "      <th>cc_no</th>\n",
       "      <th>cc_exp</th>\n",
       "      <th>cc_type</th>\n",
       "      <th>price(CAD)</th>\n",
       "      <th>fav_color</th>\n",
       "      <th>ip</th>\n",
       "      <th>weekday</th>\n",
       "      <th>ampm</th>\n",
       "      <th>date</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>5320</th>\n",
       "      <td>Dr.</td>\n",
       "      <td>Bruce</td>\n",
       "      <td>Bryan</td>\n",
       "      <td>ru@pubuspuh.cl</td>\n",
       "      <td>Male</td>\n",
       "      <td>59</td>\n",
       "      <td>Wal-Mart Stores Inc</td>\n",
       "      <td>Engineer Technician</td>\n",
       "      <td>(709) 446-8317</td>\n",
       "      <td>H6H 3Y0</td>\n",
       "      <td>NU</td>\n",
       "      <td>201000000000000</td>\n",
       "      <td>04/2024</td>\n",
       "      <td>Bankcard</td>\n",
       "      <td>0.0</td>\n",
       "      <td>White</td>\n",
       "      <td>82.70.62.64</td>\n",
       "      <td>Wednesday</td>\n",
       "      <td>am</td>\n",
       "      <td>12/11/1900</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>10597</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Flora</td>\n",
       "      <td>Clark</td>\n",
       "      <td>wad@me.com</td>\n",
       "      <td>Female</td>\n",
       "      <td>27</td>\n",
       "      <td>MetLife Inc.</td>\n",
       "      <td>Cruise Director</td>\n",
       "      <td>(775) 373-6590</td>\n",
       "      <td>B2U 8K6</td>\n",
       "      <td>NB</td>\n",
       "      <td>30100000000000</td>\n",
       "      <td>05/2020</td>\n",
       "      <td>Diners Club Carte Blanche</td>\n",
       "      <td>0.0</td>\n",
       "      <td>Red</td>\n",
       "      <td>231.156.15.63</td>\n",
       "      <td>Thursday</td>\n",
       "      <td>pm</td>\n",
       "      <td>08/22/1904</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "      prefix  first   last           email  gender  age              company  \\\n",
       "5320     Dr.  Bruce  Bryan  ru@pubuspuh.cl    Male   59  Wal-Mart Stores Inc   \n",
       "10597   Mrs.  Flora  Clark      wad@me.com  Female   27         MetLife Inc.   \n",
       "\n",
       "                profession           phone   postal province            cc_no  \\\n",
       "5320   Engineer Technician  (709) 446-8317  H6H 3Y0       NU  201000000000000   \n",
       "10597      Cruise Director  (775) 373-6590  B2U 8K6       NB   30100000000000   \n",
       "\n",
       "        cc_exp                    cc_type  price(CAD) fav_color  \\\n",
       "5320   04/2024                   Bankcard         0.0     White   \n",
       "10597  05/2020  Diners Club Carte Blanche         0.0       Red   \n",
       "\n",
       "                  ip    weekday ampm        date  \n",
       "5320     82.70.62.64  Wednesday   am  12/11/1900  \n",
       "10597  231.156.15.63   Thursday   pm  08/22/1904  "
      ]
     },
     "execution_count": 15,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    " cust[cust['price(CAD)'] == 0.0]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "As a loyalty reward, company wants to send thanks coupon to those who spent 100CAD or more, please find out the customers?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>prefix</th>\n",
       "      <th>first</th>\n",
       "      <th>last</th>\n",
       "      <th>email</th>\n",
       "      <th>gender</th>\n",
       "      <th>age</th>\n",
       "      <th>company</th>\n",
       "      <th>profession</th>\n",
       "      <th>phone</th>\n",
       "      <th>postal</th>\n",
       "      <th>province</th>\n",
       "      <th>cc_no</th>\n",
       "      <th>cc_exp</th>\n",
       "      <th>cc_type</th>\n",
       "      <th>price(CAD)</th>\n",
       "      <th>fav_color</th>\n",
       "      <th>ip</th>\n",
       "      <th>weekday</th>\n",
       "      <th>ampm</th>\n",
       "      <th>date</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>76</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Gregory</td>\n",
       "      <td>Brown</td>\n",
       "      <td>hav@jek.gs</td>\n",
       "      <td>Female</td>\n",
       "      <td>31</td>\n",
       "      <td>E*Trade Group, Inc.</td>\n",
       "      <td>Novelist</td>\n",
       "      <td>(625) 537-8923</td>\n",
       "      <td>X3S 4Q2</td>\n",
       "      <td>PE</td>\n",
       "      <td>6010000000000000</td>\n",
       "      <td>04/2018</td>\n",
       "      <td>Visa</td>\n",
       "      <td>100.0</td>\n",
       "      <td>Green</td>\n",
       "      <td>212.100.18.95</td>\n",
       "      <td>Monday</td>\n",
       "      <td>am</td>\n",
       "      <td>10/23/2063</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>21093</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Cody</td>\n",
       "      <td>Christensen</td>\n",
       "      <td>get@jovu.ag</td>\n",
       "      <td>Male</td>\n",
       "      <td>28</td>\n",
       "      <td>National City Corp.</td>\n",
       "      <td>Hospital Administrator</td>\n",
       "      <td>(261) 737-3292</td>\n",
       "      <td>X0S 1O5</td>\n",
       "      <td>PE</td>\n",
       "      <td>201000000000000</td>\n",
       "      <td>03/2024</td>\n",
       "      <td>JCB</td>\n",
       "      <td>100.0</td>\n",
       "      <td>Green</td>\n",
       "      <td>168.48.19.165</td>\n",
       "      <td>Wednesday</td>\n",
       "      <td>pm</td>\n",
       "      <td>03/28/1955</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>24385</th>\n",
       "      <td>Miss</td>\n",
       "      <td>Lizzie</td>\n",
       "      <td>Dixon</td>\n",
       "      <td>goh@tuwjaz.gd</td>\n",
       "      <td>Female</td>\n",
       "      <td>38</td>\n",
       "      <td>FleetBoston Financial Co.</td>\n",
       "      <td>Compensation Analyst</td>\n",
       "      <td>(989) 239-1752</td>\n",
       "      <td>V8X 9V6</td>\n",
       "      <td>NB</td>\n",
       "      <td>6300000000000000</td>\n",
       "      <td>07/2019</td>\n",
       "      <td>Bankcard</td>\n",
       "      <td>100.0</td>\n",
       "      <td>Blue</td>\n",
       "      <td>140.87.99.78</td>\n",
       "      <td>Saturday</td>\n",
       "      <td>pm</td>\n",
       "      <td>03/03/1983</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "      prefix    first         last          email  gender  age  \\\n",
       "76      Mrs.  Gregory        Brown     hav@jek.gs  Female   31   \n",
       "21093   Mrs.     Cody  Christensen    get@jovu.ag    Male   28   \n",
       "24385   Miss   Lizzie        Dixon  goh@tuwjaz.gd  Female   38   \n",
       "\n",
       "                         company              profession           phone  \\\n",
       "76           E*Trade Group, Inc.                Novelist  (625) 537-8923   \n",
       "21093        National City Corp.  Hospital Administrator  (261) 737-3292   \n",
       "24385  FleetBoston Financial Co.    Compensation Analyst  (989) 239-1752   \n",
       "\n",
       "        postal province             cc_no   cc_exp   cc_type  price(CAD)  \\\n",
       "76     X3S 4Q2       PE  6010000000000000  04/2018      Visa       100.0   \n",
       "21093  X0S 1O5       PE   201000000000000  03/2024       JCB       100.0   \n",
       "24385  V8X 9V6       NB  6300000000000000  07/2019  Bankcard       100.0   \n",
       "\n",
       "      fav_color             ip    weekday ampm        date  \n",
       "76        Green  212.100.18.95     Monday   am  10/23/2063  \n",
       "21093     Green  168.48.19.165  Wednesday   pm  03/28/1955  \n",
       "24385      Blue   140.87.99.78   Saturday   pm  03/03/1983  "
      ]
     },
     "execution_count": 16,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[cust['price(CAD)'] >= 100.0]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "How many emails are associated with this credit card number '5020000000000230'?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0    sebvajom@kol.km\n",
       "1      acu@jatsot.ug\n",
       "Name: email, dtype: object"
      ]
     },
     "execution_count": 17,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[cust['cc_no'] == 5020000000000230]['email']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    " We need to send new cards to the customers well before the expire, how many cards are expiring in 2019?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "2684"
      ]
     },
     "execution_count": 18,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sum(cust['cc_exp'].apply(lambda x: x[5:]) == '19')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "How many people use Visa as their Credit Card Provider?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1721"
      ]
     },
     "execution_count": 19,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sum(cust['cc_type'] == 'Visa')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The customer who spent 100 CAD using Visa?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>prefix</th>\n",
       "      <th>first</th>\n",
       "      <th>last</th>\n",
       "      <th>email</th>\n",
       "      <th>gender</th>\n",
       "      <th>age</th>\n",
       "      <th>company</th>\n",
       "      <th>profession</th>\n",
       "      <th>phone</th>\n",
       "      <th>postal</th>\n",
       "      <th>province</th>\n",
       "      <th>cc_no</th>\n",
       "      <th>cc_exp</th>\n",
       "      <th>cc_type</th>\n",
       "      <th>price(CAD)</th>\n",
       "      <th>fav_color</th>\n",
       "      <th>ip</th>\n",
       "      <th>weekday</th>\n",
       "      <th>ampm</th>\n",
       "      <th>date</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>76</th>\n",
       "      <td>Mrs.</td>\n",
       "      <td>Gregory</td>\n",
       "      <td>Brown</td>\n",
       "      <td>hav@jek.gs</td>\n",
       "      <td>Female</td>\n",
       "      <td>31</td>\n",
       "      <td>E*Trade Group, Inc.</td>\n",
       "      <td>Novelist</td>\n",
       "      <td>(625) 537-8923</td>\n",
       "      <td>X3S 4Q2</td>\n",
       "      <td>PE</td>\n",
       "      <td>6010000000000000</td>\n",
       "      <td>04/2018</td>\n",
       "      <td>Visa</td>\n",
       "      <td>100.0</td>\n",
       "      <td>Green</td>\n",
       "      <td>212.100.18.95</td>\n",
       "      <td>Monday</td>\n",
       "      <td>am</td>\n",
       "      <td>10/23/2063</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   prefix    first   last       email  gender  age              company  \\\n",
       "76   Mrs.  Gregory  Brown  hav@jek.gs  Female   31  E*Trade Group, Inc.   \n",
       "\n",
       "   profession           phone   postal province             cc_no   cc_exp  \\\n",
       "76   Novelist  (625) 537-8923  X3S 4Q2       PE  6010000000000000  04/2018   \n",
       "\n",
       "   cc_type  price(CAD) fav_color             ip weekday ampm        date  \n",
       "76    Visa       100.0     Green  212.100.18.95  Monday   am  10/23/2063  "
      ]
     },
     "execution_count": 20,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[(cust['cc_type'] == 'Visa') & (cust['price(CAD)'] == 100.00)]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    " The two most common professions."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Preschool Teacher       112\n",
       "Distribution Manager    107\n",
       "Name: profession, dtype: int64"
      ]
     },
     "execution_count": 21,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust['profession'].value_counts().head(n = 2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "the top 5 most popular email providers? (e.g. gmail.com, yahoo.com, etc...)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "gmail.com      1687\n",
       "me.com         1676\n",
       "outlook.com    1664\n",
       "live.com       1660\n",
       "hotmail.com    1659\n",
       "Name: email, dtype: int64"
      ]
     },
     "execution_count": 22,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust['email'].apply(lambda x: x.split('@')[1]).value_counts().head()\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Is there any customer who is using email with \"am.edu\"?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>prefix</th>\n",
       "      <th>first</th>\n",
       "      <th>last</th>\n",
       "      <th>email</th>\n",
       "      <th>gender</th>\n",
       "      <th>age</th>\n",
       "      <th>company</th>\n",
       "      <th>profession</th>\n",
       "      <th>phone</th>\n",
       "      <th>postal</th>\n",
       "      <th>province</th>\n",
       "      <th>cc_no</th>\n",
       "      <th>cc_exp</th>\n",
       "      <th>cc_type</th>\n",
       "      <th>price(CAD)</th>\n",
       "      <th>fav_color</th>\n",
       "      <th>ip</th>\n",
       "      <th>weekday</th>\n",
       "      <th>ampm</th>\n",
       "      <th>date</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>150</th>\n",
       "      <td>Miss</td>\n",
       "      <td>Loretta</td>\n",
       "      <td>Fletcher</td>\n",
       "      <td>barit@am.edu</td>\n",
       "      <td>Female</td>\n",
       "      <td>48</td>\n",
       "      <td>York International Corp</td>\n",
       "      <td>Rehabilitation Counselor</td>\n",
       "      <td>(323) 279-8038</td>\n",
       "      <td>E5X 8L0</td>\n",
       "      <td>QC</td>\n",
       "      <td>6330000000000000</td>\n",
       "      <td>05/2021</td>\n",
       "      <td>Diners Club United States &amp; Canada</td>\n",
       "      <td>97.26</td>\n",
       "      <td>White</td>\n",
       "      <td>147.57.240.225</td>\n",
       "      <td>Monday</td>\n",
       "      <td>am</td>\n",
       "      <td>11/07/2066</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "    prefix    first      last         email  gender  age  \\\n",
       "150   Miss  Loretta  Fletcher  barit@am.edu  Female   48   \n",
       "\n",
       "                     company                profession           phone  \\\n",
       "150  York International Corp  Rehabilitation Counselor  (323) 279-8038   \n",
       "\n",
       "      postal province             cc_no   cc_exp  \\\n",
       "150  E5X 8L0       QC  6330000000000000  05/2021   \n",
       "\n",
       "                                cc_type  price(CAD) fav_color              ip  \\\n",
       "150  Diners Club United States & Canada       97.26     White  147.57.240.225   \n",
       "\n",
       "    weekday ampm        date  \n",
       "150  Monday   am  11/07/2066  "
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust[cust['email'].apply(lambda x: x.split('@')[1]) == 'am.edu']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    " Which day of the week, the store gets more customers?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Saturday     4376\n",
       "Wednesday    4365\n",
       "Thursday     4327\n",
       "Friday       4316\n",
       "Monday       4216\n",
       "Name: weekday, dtype: int64"
      ]
     },
     "execution_count": 24,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "cust['weekday'].value_counts().head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "gist": {
   "data": {
    "description": "Pandas-Project_Customer_Purchase_Data.ipynb",
    "public": true
   },
   "id": ""
  },
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.0"
  },
  "toc": {
   "base_numbering": 1,
   "nav_menu": {},
   "number_sections": true,
   "sideBar": true,
   "skip_h1_title": false,
   "title_cell": "Table of Contents",
   "title_sidebar": "Contents",
   "toc_cell": false,
   "toc_position": {},
   "toc_section_display": true,
   "toc_window_display": false
  },
  "varInspector": {
   "cols": {
    "lenName": 16,
    "lenType": 16,
    "lenVar": 40
   },
   "kernels_config": {
    "python": {
     "delete_cmd_postfix": "",
     "delete_cmd_prefix": "del ",
     "library": "var_list.py",
     "varRefreshCmd": "print(var_dic_list())"
    },
    "r": {
     "delete_cmd_postfix": ") ",
     "delete_cmd_prefix": "rm(",
     "library": "var_list.r",
     "varRefreshCmd": "cat(var_dic_list()) "
    }
   },
   "types_to_exclude": [
    "module",
    "function",
    "builtin_function_or_method",
    "instance",
    "_Feature"
   ],
   "window_display": false
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
