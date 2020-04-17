# Google Scholar and Google Patents Scraper  

## Getting started  

In the working directory of your python script  
```bash
mkdir acad_patients
cd acad_patients
git init
git remote add origin 'https://www.github.com/saadejazz/acad_patents'
git pull origin master
```
Install python dependencies:  
```bash
python -m pip install requests bs4
```

## Google scholar  
**Code:**  
```python
from acad_patients.academics_and_patents import scholar

query = "black matter"
results = scholar(query)

```
**Single output:**  
```python
{
    'title': 'Primordial black holes as dark matter',
    'link': 'https://journals.aps.org/prd/abstract/10.1103/PhysRevD.94.083504',
    'publish_data': {'authors': 'B Carr, F Kühnel, M Sandstad\xa0- Physical Review D, 2016',
    'journal/conference': 'APS',
    'site': ''},
    'pdf': {'site': ' arxiv.org', 'link': 'https://arxiv.org/pdf/1607.06077'},
    'partial_summary': 'The possibility that the dark matter comprises primordial black holes (PBHs) is considered, with particular emphasis on the currently allowed mass windows at 1 0 16–1 0 17 g, 1 0 20–1 0 24 g and 1–1 0 3 M⊙. The Planck mass relics of smaller evaporating PBHs are also\xa0…',
    'citations': '551',
    'versions': '9'
}
```

## Google Patents  
**Code:**  
```python
from acad_patients.academics_and_patents import patents

query = "broom"
results = patents(query)

```
**Single output:**  
```python
{
    'title': 'Versatile construction broom holder www.google.com.pk/patents/US4882802',
    'link': 'https://www.google.com.pk/patents/US4882802?dq=broom&hl=en&sa=X&ved=0ahUKEwjF2rbMru_oAhUWxDgGHduXCqsQ6AEIJDAA',
    'cited_link': 'www.google.com.pk/patents/US4882802',
    'inventors': [{'name': 'Chester C. LeVere, Jr.',
        'google_inventor_search_link': 'https://www.google.com/search?tbm=pts&tbm=pts&q=ininventor:%22Chester+C.+LeVere,+Jr.%22'},
    {'name': 'Levere Jr Chester C',
        'google_inventor_search_link': 'https://www.google.com/search?tbm=pts&tbm=pts&q=inassignee:%22Levere+Jr+Chester+C%22'}],
    'partial_description': 'An improved broom holder to finish newly laid concrete surfaces is provided having a collar designed to accept a number of different commerically available\xa0...',
    'status': 'Grant',
    'filing_date': '15-Jun-1988',
    'issued_date': '28-Nov-1989',
    'published_date': ''
}
```