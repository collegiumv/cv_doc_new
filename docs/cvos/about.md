# Why?

When the CVOS Project was started, one of the biggest questions that was asked was "why," and on the surface, it's a very good question.  To the casual observer everything worked, and there was nothing to be improved.  However, behind the scenes, the lounge was one good thunderstorm away from having a very broken network.

The admins strive to provide a robust, enterprise-grade network with as much up-time as can be practically achieved, but it is important to remember that admins are full-time students.  The limit of reliability is then how much time is left for the admins to work on the lounge computers after finishing homework, studying, and other school related activities.  If research is needed to complete a task, that further draws out the process.  Finally there is the constraint that every 4 years, there is a completely new group running the network, and ideally this happens without a complete refactor every time.

Sounds impossible right?  Wrong.

The previous system was good, it did almost everything that was asked of it, but had 2 key flaws:

* It featured a single point of failure (SPOF)
* No files were backed up

## A single point of failure

A single point of failure means that there is a single link which, when removed, causes the failure of the entire system.  In the case of the old lounge network, this was one of the primary Windows Servers. The server in question simultaneously managed the user accounts for all 600 lounge users, the print queues for Franklin and Koster, file storage for everyone on the network, and Windows Updates for all the lounge computers.  On top of all this, because it was a Windows server, it was very difficult to troubleshoot and diagnose when any errors came up.  While almost everything else on the network had at least one backup, this very important system became a constant cause of worry for the admins.

The single point of failure case, together with a second issue, created a perfect storm waiting to happen.  Due to the limits imposed by the Windows Server File Services service, the only efficient way to backup files is to another Windows server, which then has the same maintainability issues!

Thus after a particularly bad evening of troubleshooting some errors that had cropped up on one of the Windows servers, the admins began looking for a better way.  The solution was immediate to the admins, but there was concern whether this solution, a system written specifically to suite the needs of Collegium V students, would be accepted.  A technical round-table was scheduled to ask lounge users if this was a viable plan.  The minutes from that round-table are better lost to time, but in the end, it was decided that yes, the lounge could adapt and benefit from a more maintainable, more adaptable system.

And so the CVOS project began.  If you're interested in the steps that led to the full installations that are present in the lounge, or are interested in technical information not covered in this article, please ask an admin.

## The first great refactor

After a year of running the network on a custom Linux solution, a great deal of new information has been gathered.  For example, while Ubuntu Linux was originally thought to be an easy solution on which to base the CVOS platform, due to its "off the shelf" nature, it became more of a liability than the admins were comfortable with.  Most of these issues were related to the management of the "micro-services" that are needed to keep everything running smoothly.  These services range from minecraft authentication daemons to LDAP bridge APIs.  These services were painful enough to manage under Ubuntu's mashup of init systems, and would have required a substantial amount of refactoring to work correctly under systemd.

In parallel, the university's Computer Science department had begun substantial student involvement with Void Linux.  After evaluating the viability of using Void Linux on the CV network, the admins decided it would be an acceptable solution.  This transition was completed in the summer before the 2016-2017 academic year.


## Where did MS Office Go?

A reasonable question is "where did office go!?"  Since 1998, The University of Texas System has participated with Microsoft Corporation in a Microsoft Campus Agreement (MSCA) to provide students, faculty, and staff access to the latest release of Microsoft Office and Office for Mac productivity suites and Microsoft Windows, at no cost or at substantially reduced cost.  The terms of the MSCA stipulate who and how the software will be used in rigid, legally rigorous terminalogy.  One can think of the MSCA as a Terms of Service (ToS) agreement for who can use the software.  It is not surprising that the MSCA doesn't account for people wanting to run MS products in non-Windows or non-macOS environments.

The CVAdmins have sought twice to get approval to run the MS Office suite by sending a written request for a review of the licensing agreement to OIT.  Both times the request has been unanswered.  Until written approval is granted from an office legally able to do so, MS products cannot be installed on the CV workstations.


### So what do I write my papers in?

While MS Office is not provided, there are many solutions provided for your use.  Please consult the [Office](office.md) page to find a suite that is conducive to your working style.