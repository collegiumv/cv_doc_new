# Why?
When the CVOS Project was started, one of the biggest questions that was asked was "why" and on the surface its a very good question.  To the casual observer
everything worked and there was nothing to be improved.  Behind the scenes, the lounge was one good thunderstorm away from having a very broken network.

The admins strive to provide a robust, enterprise grade network with as much up-time as can be practically done, but it is important to remember that admins are full
time students.  The limit of reliability is then how much time is left for the admins to work on the lounge computers after finishing homework, studying, and other
school related activities.  If research is needed to complete a   task, that further draws out the process.  Finally there is the constraint that         every 4 years, there is
a completely new group running the network, and ideally this happens without things completely changing      every 4 years.

Sounds impossible right?  Wrong.

The previous system was good, it did almost everything that was asked of it but had 2 key flaws:

  * It featured a single point of failure (SPOF)
  * No files were backed up

## A single point of failure
A single point of failure means that there is a single link which, when removed, causes the failure of the entire system.  In the case of the old lounge network, this
was one of the primary Windows Servers.     The server in question simultaneously managed the user accounts for all 600 lounge users, the print queues for Franklin and
Beryllium, file storage        for everyone on  the network, and Windows Updates for all the lounge computers.  On top of all this, because it was a Windows server, it was
very difficult to troubleshoot and diagnose when any errors came up.  Almost everything  else on the network had at least one backup making this a very important system
that the admins always worried about.

The single point of failure case came together with the second issue to create a perfect storm waiting to happen.  Due to the limits imposed by the Windows Server File
Services service, the only efficient way to backup files is to another Windows server which then has the same maintainability issues!

Thus after a particularly bad evening of troubleshooting some errors that had cropped up on one of the Windows servers, the admins began looking for a better way.  The
solution was immediate to the admins, but there was concern if the solution of a system written specifically to suite the needs of Collegium V students would be
accepted.  A technical round-table was scheduled to ask     lounge users if this was a viable plan.  The minutes from that round-table are better lost to time, but the end
result was that yes, the lounge could adapt and benefit     from a more maintainable, more adaptable system.

And so the CVOS project began.  If you're interested in the steps that led to the full installations that are present in the lounge, or are interested in technical
information beyond the scope of this article, please ask an admin.

## The first great refactor
After a year of running the network on a custom Linux solution a great deal of new information has been gathered.  For example, while Ubuntu Linux was originally thought to be an easy solution to base the CVOS platform on due to its "off the shelf" nature, it became more of a liability than the admins are comfortable with.  Most of these issues were related to the management of the "micro-services" that are needed to keep everything running smoothly.  These services range from minecraft authentication daemons to LDAP bridge APIs.  These services were painful enough to manage under Ubuntu's mashup of init systems and would have required a substantial amount of refactoring to work correctly under systemd.

In parallel the university's computers science department has begun substantial student involvement with Void Linux.  The admins evaluated the viability of using Void Linux on the CV network and decided it would be an acceptable solution.  This transition was completed in the summer before the 2016-2017 academic year.
