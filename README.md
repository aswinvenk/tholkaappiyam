Tholkaappiyam -  A library for Python to globalize the ancient text of the oldest language in the world, Tamil"
===============================================================================================================

## A Python package to understand Tholkaappiyam in English and use it for enhancing NLP
Tholkaappiyam is the most ancient extant Tamil grammar text and the oldest extant long work of Tamil literature.
In order to make people all over the world understand Tamil, **i18n Solutions Salem**, have developed this package.

> Developed by i18nSolutions <i18nsolutions@gmail.com> 
> Backend Developer : Aswin Venkat <aswinvenk8@gmail.com>
> Data Creation : Pugazhendi Neduncheralathan, Sai Sidhartha, Chandru T, Yashika Murugesan, Abisheak Sabari, Bala Murugan, Niyazuddeen Navab, Gokula krishnan

Installation
============

How to install ?

```python
pip install tholkaappiyam
```

Pre-Requisites
==============

> 1. Pandas
> 2. JSON


Importing in python
===================

How to import ?

```python
from tholkaappiyam import thol
```

About Tholkaappiyam
===================
Tolkāppiyam or Tholkaappiyam has **3 Adhikaarams**. Each Adhikaaram has **9 Iyals** in them. Each Iyal have a specific number of songs/paadal (or Sutrās). Songs are classified into **Categories**. If we analyse the songs as categories, it is easier to understand the core meaning of the Sutrās.

History of Tholkaappiyam
========================
Tholkapiyam, some traditionally believe, was written by a single author named Tolkaappiyar, a disciple of Vedic sage Agastya mentioned in the Rigveda (1500–1200 BCE). His student Tholkaappiyar was asked to compile Tamil grammar, which is Tolkappiyam. In Tamil historical sources such as the 14th-century influential commentary on Tolkappiyam by Naccinarkkiniyar, the author is stated to be Tiranatumakkini (alternate name for Tolkappiyan), the son of a Brahmin rishi named Camatakkini. The earliest mention of Agastya-related Akattiyam legends are found in texts approximately dated to the 8th or 9th century. The dating of the Tolkappiyam is difficult, much debated, and it remains contested and uncertain. Proposals range between 5,320 BCE and the 8th century CE.


Displaying
==========

```python

# About Tholkaappiyam
>> thol.about_tholkaappiyam()

# Display Adhikaarams
>> thol.display_adhikaaram()

# Display Iyals
>> thol.display_iyal(adhikaaram_no)

# Display Tholkaappiyar
>> thol.display_tholkaapiyar()
```

JSON Data 
=========

```python

# Returns the entire JSON dataset of Tholkaappiyam to the user
>> data=thol.data_json()
```

Methods
=======

```python
# Class Adhikaaram
>> thol.Adhikaaram(adhikaaram_no)
```

- It has 2 methods:
    - display_total_no_of_songs() :
        - Prints total number of songs in the Adhikaaram
    - iyals_paadal_count_dict() :
        - Returns a dict containing iyals of the adhikaaram and the number of paadal in each iyal


```python
# Class Iyal
>> thol.Iyal(adhikaaram_no,iyal_no)
```

- It has 2 methods :
    - display_total_no_of_songs() : 
        - Prints total number of songs in the Iyal
    - iyals_paadal_count_dict() :
        - Returns a dict containing categories of the iyal and the number of paadal in each categories



```python
# Class Paadal
>> thol.Paadal(adhikaaram_no,iyal_no,paadal_no)
```

- It has 1 important method :
    - paadal_data() :
        - Returns a dict of song data


```python
Paadal_data =
{
paadal                  :   "paadal...",
paadal_meaning          :   "paadal in english",
paadal_category         :   "Paadal category (eng)",
paadal_iyal             :   "Iyal that the paadal belongs",
paadal_iyal_eng         :   "Iyal of the paadal belongs in English",
paadal_adhikaaram       :   "Adhikaaram that the paadal belongs",
paadal_adhikaaram_eng   :   "Adhikaaram that the paadal belongs in English"
}
```


```python
# Class Category
>> thol.Category(adhikaaram_no,iyal_no)
```

- It has 2 methods :
    - paadal_dict():
        - Returns a dict where,
            - Key : Name of the Category you selected
            - Value : List of the Songs in that category

    - paadal_data():
        - Returns a list of paadal data of all the songs under the given category
        - This 'list of dict' data can be further used to study the song/paadal under the given topic


Sample Code
===========

## To check the number of songs in all the iyal in an Adhikaaram (Soladhikaaram)
```python
n=tholkaappiyam.Adhikaaram(2).iyals_paadal_count_dict()
for i in n:
    print(i,'\t\t',n[i])
```
## To check the number of songs in all the categories in an Iyal (Ezhuthadhikaaram, Pirappiyal)
```python
n=tholkaappiyam.Iyal(1,3).categories_paadal_count_dict()
for i in n:
    print(i,'\t',n[i])
```


REFERENCES:
===========

1. **Tolkāppiyam in Roman transliteration and English translation** by Pandit S. Subrahmanya Sastri

P.S. Subrahmanya Sastri was the first person to translate Tolkāppiyam into English. The translation of **Ezhuthadhikaaram** and **Poruladhikaaram** were published by the Kuppuswami Sastri Research Institute, while **Soladhikaaram** was published by Annamalai University. His English translation received encomiums from linguists across the world.

2. **Tolkāpiyam in English** by Dr. V. Murugan

This translation has been done by a professor of English, Dr. V. Murugan, who made his translation following the prosodic mood of the Tamil epic.