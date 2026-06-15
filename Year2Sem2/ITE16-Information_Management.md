$$\def\union{\cup}
\def\intersect{\cap}$$
# How to manage info & Data Privacy laws
## Info mgmt?
- Systematic process of collecting, organizing, storing & distributing data & knowledge w/in an org
- it encompasses strats, tech, & policies to ensure datacs accessible, secure, & used effectively to support decision-making & biz procs
### Why?
- to assist employees w/ org roles or fn to make quicker & better informed decisions to deliver info to right ppl at right time n place
- it should clearly define who's responsible for IM w/in orgs.

## keys to im
- leadership
- operations
- processes
- data
- tech
## Keys to IM
- **Leadership**: engaged, set the vision/strat, make key decisions
- **Operations**: ppl, proj mgmt, & comms
- **Processes**: design, doc, exec
- **Data**: collect, organize, maintain, use
- **Technology**: tech align with prior keys
## Info Lifecycle Mgmt
- A comprehensive approach to managing org's data thruout its lifespan from creation, storage, usage, archiving & eventual disposal
### ILM stages
1. **Acquisition & creation**: here data enters an org thru various channels including manual entry, digiforms, auto sensors, & extern partnerships
2. **Storage & maintenance**:  is critical for organizations to clearly define where their information will be stored, define backup schedules, maintain the information, and secure it in appropriate ways.
3. **Processing & use**:  is critical for organizations to clearly define where their information will be stored, define backup schedules, maintain the information, and secure it in appropriate ways.
4. **Disposition**: information is kept only as long as necessary and safely deleted when no longer needed.
5. **Archival**
## GDPR
- EU's data privacy law, really strict
- applies to any orgs that target EU users
## RA 10173 (Data Privacy Act of 2012)

## National Privacy Commission
The country's privacy watchdog. It's an independent body mandated to administer & implement the 2012 DPA & monitor & ensure the country's compliance w/ i12l data protection stds


## Ethical Foundation of The Data Privacy Act
- respect for individual privacy 
- transparency and fairness 
- purpose limitation and proportionality
- accountability and responsibility 
- Protecting data subject rights

# DB Fundamentals
## Database?
It's an organised collection of related data consisting of rows & columns (well, usually, see NoSQL) used to allow efficient data storage, retrieval, updating & mgmt
## DBMS
It's a software used to create & manage dbs. It acts as a bridge between users & db (like, the file).
## DBMS component
1. **Hardware**
2. **Software**
3. **Data**
4. **Procedures** (ILM included)
5. **Db access language** (e.g., SQL, CQL)
6. **User**
## File System
Stores data in separate files & relies on the OS to organise, access & manage those files

## File System vs DBMS

| Fs                                 | Dbms                                     |
| ---------------------------------- | ---------------------------------------- |
| Files                              | Stored in structured tables, inside a db |
| May dupe data                      | Minimizes dupe data                      |
| Can be inconsistent between update | Consistent most of the time              |
| Limited security                   | High security w/ user access ctrl        |
| Difficult to support multi-user    | Easy multi-user access                   |
| Has auto backup & recov            | Manual                                   |

## Relational Algebra
~~oh no~~
Theo foundation of db that helps understand how dbs process queries. 
- Used for data selection filtering & combining
- insanely useful in writing quality sql queries

| Operation  | Symbol       | E.g.,                            |
| ---------- | ------------ | -------------------------------- |
| Selection  | $\sigma$     |                                  |
| Projection | $\pi$        | SELECT Name, Course FROM STUDENT |
| Join       | $\bowtie$    |                                  |
| Union      | $\cup$       |                                  |
| Intersect  | $\intersect$ |                                  |
| Difference | $-$          |                                  |

# Database Modeling

## Chen's Notation

> [!NOTE] o o i i a i o o o i a i
> ![[ezgif-159a0c810704d6d5.gif]]
> wait no wrong Chen
> By [Zenerat](https://x.com/zenerat/status/1732598198789919038)

# Normalization (1nf, 2nf, 3nf)
## Normalization?
A technique of minimizing redundancy by org data to
## Data redundancy 
Repetition of data which takes spaces and causing issues in:
- **ins**: 
- **del**
- **upd**

# SQL
# Indexing

