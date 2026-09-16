# Raider Roster Hub

**Live:** https://rjedtech.github.io/Raider-Roster-Hub/

Roster Hub takes a Regis Jesuit class list once and makes it usable in other tools without exposing student names. Teachers can use ZipGrade without putting names into ZipGrade, and the same classes carry over to the Raider Randomizer and the Pod Generator. A class list becomes three-digit numbers, and Roster Hub gives the teacher:

- the file to import into ZipGrade (numbers only),
- printable code slips to hand out,
- a private key that turns numbers back into names,
- a score list by name, plus an optional Canvas gradebook import file.

Everything runs in the browser. There is no server and no upload.

Full guide for teachers: [ZipGrade: scan paper quizzes without student names](https://rjhs.instructure.com/courses/5414/pages/zipgrade-scan-paper-quizzes-without-student-names) (Canvas PD course).

## Class lists

Roster Hub reads class lists with the same roster reader as the [Raider Randomizer](https://rjedtech.github.io/Raider-Randomizer/) and the [Pod Generator](https://rjedtech.github.io/Raider-Pods/). It accepts:

- **MyRJ Manual Attendance Sheet - By Teacher And Section → Excel, column A.**
  - With **Section = All**, each class is listed separately and numbered 1, 2, 3 in order.
  - Each class is named by its block rotation, for example `4W-1W-3W · Theology of Encounter`, since blocks switch every six weeks.
  - IMPACT starts unticked.
  - All students are never merged into one class.
- **The Canvas People page.** Parents, teachers and designers are left out.
- **The Canvas Gradebook.** Grades and assignment names are left out.
- **The MyRJ Roster cards.** Emails, addresses and phone numbers are left out.
- **A plain list**, one name per line.

Roster Hub uses legal first names, which match Canvas and ZipGrade records.

## Sharing classes with the other tools

All three tools run on `rjedtech.github.io`, so they can read each other's saved classes. This happens only in the same browser on the same computer:

- Roster Hub offers classes saved in the Randomizer (`rs3_classes`) and the Pod Generator (`rr_pods_v3`) as one-tap buttons.
- The Randomizer and the Pod Generator show classes remembered in Roster Hub (`rj-roster-hub-v1`) in their "bring one back" rows.

## Codes

Student *s* in class *c* gets the code `c × 100 + s`, so student 7 in class 3 is `307`.

- Roster Hub numbers up to 8 classes.
- Each ZipGrade file has 40 seats, so a late addition's code already exists in ZipGrade.
- A new paste never overwrites a class that is already set up. It takes the next free class number.

## Files

`index.html`: a single file with no dependencies beyond the IBM Plex Mono web font.
