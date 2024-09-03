<!-- [Jargon Chaff File][0] -->

# Jargon Chaff File

--------------------------------

This is the chaff file. It contains all the entries which have been
added to the Jargon File at some point and later rejected for various reasons
(usually because they're mainstream English or straight techspeak). They are
kept up-to date with the current master format conventions.

### Drafted but never added

**[ALGOL][1]**

**[archiver][2]**

**[balanced][3]**

**[bit mask][4]**

**[bit vector][5]**

**[escape][6]**

**[giant blue lobster][7]**

**[GUI][8]**

**[IPL][9]**

**[kernel][10]**

**[native mode][11]**

**[pass-by-name][12]**

**[pass-by-reference][13]**

**[pass-by-value][14]**

**[race condition][15]**

**[RISC][16]**

**[RMS][17]**

**[signal][18]**

**[spoofing][19]**

**[stub][20]**

**[Symbolics][21]**

**[seer][22]**

**[whitespace][23]**

**[write behind][24]**

**[write through][25]**

****

****ALGOL**: n.**
> 
> \[ALGOrithmic Language\] The common ancestor of C and the Pascal
> family (including Ada and the various versions of Modula). One of the
> great pioneering efforts in language design; indeed, it has been said that
> Algol was a great improvement over most of its successors.

****

****archiver**: n.**
> 
> /ar'kie-vr/ A utility that
> can pack and unpack file sets and/or entire directory hierarchies to and
> from an \`archive' format including the file data and information such as
> its creation date and size. There are many of these, used both for backups
> but in preparing software distributions for cross-network transport.
> UNIX's tar(1) and cpio(1), Windows's ARC.EXE, and zoo(1) for both UNIX and
> Windows handle archive formats often used not only on these systems but in
> many other environments which must communicate with them regularly.

****

****balanced**: /bal'@nst/, adj.**
> 
> Said of a system in which investment in major resources (memory,
> disk and CPU cycles) have been matched to the job load in such a way that
> programs are not typically all waiting on the same resource. See
> _bottleneck_, _hot spot_.

****

****bit mask**: n.**
> 
> A string of bits in _core_ that is interpreted
> by hardware or software as enable/disable _flag_s for
> some related set of options or operations. May be used either of hardware
> flags wired into a computer system's control logic or of software flags
> controlling some part of a program's execution. Connotes a relatively small
> set of bits (a byte or word) as opposed to a _bit
> vector_ which may be of any length. See also _bit
> bashing_.

****

****bit vector**: n.**
> 
> See _bit mask_.

****

****escape**: n.**
> 
> 1\. The ASCII character ESC, hex 1b, octal 033, usually labelled ESC
> or (rarely) ALTMODE on terminal keyboards. Some operating systems
> (including older UNIXes) use this character to indicate that output is to
> be suspended. 

> 2\. A special character that may cause the following character to
> have other than its usual meaning, esp. used under UNIX for the backslash
> character \`\\'. Such a character, used to prevent the special meaning of a
> wildcard or other special character, is said to \`escape' the character from
> its special meaning. Use of this sort of literalizing to quote quote
> characters or other special syntax is often called
> _escapement_; the use of \`\\' is often specifically
> _slashification_.

****

****giant blue lobster**: n.**
> 
> The default absurd mythological animal. This originated among
> aficionados of Live Action Role Playing, a hobby largely inhabited by
> hackers. A 1987 LARP game called \`Starlight Rendezvous' featured several
> characters who were, in game, giant blue lobsters (complete with giant
> lobster armor artfully sculpted out of blue foam rubber). These
> \`Klik-kliks' were obstreperous beings whose idea of diplomacy was to sidle
> up to other players, insult them, and declaim "We have giant blue
> pincer claws and we're not afraid to use them" in gruff voices
> resembling Richard Nixon's. Eventually one was tossed in a jacuzzi by a
> crowd chanting "Drawn butter! Drawn butter!". The lobsters
> became a running joke in later LARPs, and have since often been invoked in
> conversation by hackers who were not present for the original game and,
> indeed, have only a vague idea about where the image derives from.

****

****GUI**: /goo'ee/, n.**
> 
> \[acronym for "graphical user interface"\] A combination
> of a particular window system (such as X, NeWS or PM) and an
> interface-design policy for applications. In 1990, prominant GUIs battling
> it out for mind-share include AT&T/Sun's Open Windows, OSF's Motif,
> HP's New Wave and Microsoft's Presentation Manager interface. See
> _FUD Wars_.

****

****IPL**: /ie-pee-el/, v.,n.**
> 
> \[acronym for Initial Program Load\] Synonym for
> _boot_. Usage: now rare, reported at IBM and
> Motorola. Formerly more common at IBM shops.

****

****kernel**: /ker'nl/**
> 
> \[from UNIX, now also used elsewhere\] The resident portion of the
> operating system; that which handles I/O dispatch, runs and schedules
> processes, and provides other system services to applications through TRAPs
> or system calls. Distinguished from application libraries (on the one hand)
> and the system _shell_ or command interpreter on the
> other.

****

****native mode**: /nay'tiv mohd/, n.**
> 
> On hardware or software supporting several functional modes, some
> designed to emulate the behavior of other similar products, \`native mode'
> is the one (usually default) command set or feature set that is
> _not_ an emulation. Example: many smart CRTs support
> ANSI or vt100 emulations in addition to the default native mode defined by
> the manufacturer.

****

****pass-by-name**: /pas-bie-naym'/, n.**
> 
> See _thunk_. Abandoned as a technique by HLL
> language designers many years ago except in explicit
> _macro_ processing; it's too expensive and makes side
> effects too hard to track. Can be inexactly simulated in C or LISP by using
> the macro facility. See also _pass-by-reference_,
> _pass-by-value_.

****

****pass-by-reference**: /pas-bie-re'fr@ns/, n.**
> 
> A mode of argument-passing supported by Pascal \`var' arguments and
> in some other languages which requires the caller to give the name of a
> variable as the actual and binds the formal to the
> _address_ (in effect) of the variable. Variables passed
> to a function by reference can be modified in place by the function. This
> can be simulated in C using the address (&) operator in the function
> invocation and the pointer-dereference (\*) operator within the body of the
> function. See _pass-by-name_,
> _pass-by-value_.

****

****pass-by-value**: /pas-bie-val'yoo/, n.**
> 
> The simplest and most \`natural' form of argument passing (and the
> default in all modern HLLs); the value of the actual argument expression is
> computed once at function-call time and the corresponding formal is bound
> to it for the scope of the function. See
> _pass-by-name_,
> _pass-by-reference_.

****

****race condition**: n.**
> 
> A class of bug in multi-tasking, multi-threaded or event-driven
> systems arising from situations in which code will fail if one task gets to
> a particular execution point before another has had time to prepare for
> that event. In UNIX, often used to refer to various kinds of
> _lossage_ due to V7 and USG UNIX's non-self-resetting
> signal(2) facilities; if two signals hit a process in rapid succession, the
> second may arrive before the signal handler can reset itself, resulting in
> process death and potentially infinite
> _screwage_.

****

****RISC**: /risk/**
> 
> \[Reduced Instruction Set Computer\] An architectural approach to
> processor pioneered at Berkeley in the early 1980s which emphasizes simple
> fixed-length instructions implemented in random logic or PLAs, as opposed
> to the older style that came to be called CISC \[Complex Instruction Set
> Computer\] architectures typified by the _VAX_ in which
> elaborate microcode is used to implement bushels of addressing modes and
> special-case instructions of wildly varying length. RISC processors also
> generally feature a large file of _orthogonal_
> registers and register windowing to reduce HLL function-call overhead. The
> theory behind all this was to optimize to the code-generating style of HLL
> compilers rather than human programmers, trading away instruction-set
> complexity to eliminate decode overhead and improve performance. It worked;
> see _killer micro_.

****

****RMS**: //**
> 
> Nom de guerre of Richard M. Stallman, archetypal AI hacker famous in
> particular for 1) inventing EMACS, 2) his belief that making money from
> software is evil, and 3) the consequent creation of the Free Software
> Foundation. See _copyleft_,
> _demigod_, _EMACS_,
> _GNU_, _Symbolics_.

****

****signal**: /sig'nl/, n.**
> 
> \[from UNIX\] A software interrupt, especially one which dispatches to
> a handler written in an application (as opposed to merely triggering a
> system-level event).

****

****spoofing**: n.**
> 
> In the subjargon of computer security specialists, an attack which
> relies on the inability of users or computer programs to verify the
> identity or location of a communication partner. A
> _mockingbird_ spoofs the computer's login sequence to
> fool a user; some cracking software repeatedly spoofs human login actions
> to fool the computer. 

****

****stub**: /stuhb/, n.**
> 
> A dummy routine which either performs no action or simply announces
> its presence, inserted at the bottom of a call hierarchy to verify that the
> control flow at all levels above it is functioning as intended.

****

****Symbolics**: /sim-bo'liks/, n.**
> 
> \[aka \`Slymebolics' /sliem-bah'liks/\] A manufacturer of Lisp
> Machines that evolved out of the MIT lisp machines. Once thought by some
> to be evil incarnate because they were making money from software. (See
> _RMS_) They lost this status when they proved that
> they weren't interested in making money from software. See
> _seer_.

****

****seer**: v.**
> 
> To take a marginally successful but poorly managed company and drive
> it completely into the ground. The word comes from Brian Seer, a man who
> was brought in from the outside to manage Symbolics. His tenure there led
> to the following joke:
> 
> > Q: What do Brian Seer and Richard Stallman have in common?
> > 
> > A: Neither of them believes in making money from software.
> 
> \[Editorial disclaimer: RMS protest that this joke misrepresents his
> position\] See also _GNU_.

****

****whitespace**: /hwiet'spays/, n.**
> 
> \[esp. in C/UNIX shops\]

> 1\. Any sequence of the characters space, newline, tab,
> carriage-return and (sometimes) vertical tab. 

> 2\. Parts of a code layout style where the code is not, whether
> inserted because of parsing requirements or for human readability.
> "Remember, C hackers -- whitespace is your friend!"

****

****write behind**: /riet be-hiend'/, v.**
> 
> To buffer data for writing to a device at a convenient time in the
> future, without holding up the computation of the process doing the
> writing. Oppose _write through_.

****

****write through**: /riet throo/, v.**
> 
> To write data from a process to disk, with no buffering, each time
> and every time the process does an I/O request. Oppose _write
> behind_. Safer, but slower.

### Deleted before 2.1.1 or earlier

**[spazz][26]**

**[waterbottle soccer][27]**

**[sixty-nine][28]**

**[PTY][29]**

**[moon][30]**

**[line feed][31]**

****

****spazz**: v.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted: mainstream

> 1\. To behave spastically or erratically; more often, to commit a
> single gross error. "Boy, is he spazzing!"

> 2\. n. One who spazzes. "Boy, what a spazz!"

> 3\. n. The result of spazzing. "Boy, what a
> spazz!"

****

****waterbottle soccer**: n.**Revision 1.2.0??? 

Added

Revision 1.5.0??? 

Deleted

> A deadly sport practiced mainly by Sussman's graduate students. It,
> along with chair bowling, is the most evident manifestation of the "locker
> room atmosphere" said to reign in that sphere. (Sussman doesn't approve.)
> 
> \[As of 11/82, it's reported that the sport has given way to a new
> game called "disc-boot", and Sussman even participates
> occasionally.\]

****

****sixty-nine**: adj.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

> Large quantity. Usage: Exclusive to MIT-AI. "Go away, I have 69
> things to do to DDT before worrying about fixing the bug in the phase of
> the moon output routine..."
> 
> \[Note: Actually, any number less than 100 but large enough to have no
> obvious magic properties will be recognized as a "large number". There is
> no denying that "69" is the local favorite. I don't know whether its
> origins are related to the obscene interpretation, but I do know that 69
> decimal = 105 octal, and 69 hexadecimal = 105 decimal, which is a nice
> property. - GLS\] 

****

****PTY**: n., /pi'tee/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

> Pseudo TTY, a simulated TTY used to run a job under the supervision
> of another job. PTYJOB /pi'tee/ n. The job being run on the PTY. Also a common
> general-purpose program for creating and using PTYs. This is DEC and SAIL
> terminology; the MIT equivalent is STY.

****

****moon**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

> 1\. A celestial object whose phase is very important to hackers. See
> _phase of the moon_.

> 2\. Dave Moon (MOON@MC).

****

****line feed**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

> \[standard ASCII terminology\]

> 1\. v. To feed the paper through
> a terminal by one line (in order to print on the next line).

> 2\. n. The
> "character" that causes the terminal to perform this
> action.

### Deleted before 2.1.5

**[Cambridge notation][32]**

**[gateway][33]**

**[Kleene star][34]**

**[snog][35]**

****

****Cambridge notation**: n., /kaym'brij no-ta'shn/, /kaym'brij po'lish/**Revision 2.1.1??? 

Added

Revision 2.1.5??? 

Deleted: techspeak

> \[LISP\] The now-standard way of writing LISP expressions as nested
> lists, with parens and spaces; as opposed to the earlier and technically
> purer practice of writing full S-expressions with cons dots. Supposedly
> invented as a KLUGE because a full parser for S-expressions would have been
> harder to write.

****

****gateway**: /gayt'way/, n.**Revision 2.1.1??? 

Added

Revision 2.1.5??? 

Deleted: techspeak

> 1\. A computer or item of special-purpose hardware that links two or
> more normally incompatible data networks and does protocol translation
> between them. 

> 2\. On compatible or common-carrier networks, a piece of software
> that translates between normally incompatible data formats and addressing
> conventions.

****

****Kleene star**: n., /kleen star/**Revision 2.1.1??? 

Added

Revision 2.1.5??? 

Deleted: techspeak

> See _regular expression_s.

****

****snog**: v.**Revision 2.1.1??? 

Added

Revision 2.1.5??? 

Deleted: insufficient live use among
non-SF-fans.

> \[from old-time science-fiction fandom\] Equivalent to mainstream "make
> out" describing sexual activity, especially exploratory. Most often
> encountered as participle snogging. "Oh, they're off snogging
> somewhere."

### Deleted before 2.2.1

**[assembler][36]**

**[binary][37]**

**[pointer arithmetic][38]**

**[religious war][39]**

****

****assembler****Revision 2.1.1??? 

Added

Revision 2.2.1??? 

Deleted: techspeak

> 1\. A program translator that allows human beings to generate machine
> code using mnemonics and symbolic names for memory locations rather than
> raw binary; distinguished from an _HLL_ by the fact
> that a single assembler step generally maps to a single machine instruction
> (see also _languages of choice_).

> 2\. A _nanobot_ which is a physical
> _replicator_ (This is the \`official' term, coined by
> Eric Drexler; see _nanotechnology_).

****

****binary**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.2.1??? 

Deleted: techspeak

> The object code for a program.

****

****pointer arithmetic**: n.**Revision 2.1.1??? 

Added

Revision 2.2.1??? 

Deleted: techspeak

> \[C programmers\] The use of increment and decrement operations on
> address pointers to traverse arrays or structure fields. See also
> _bump_.

****

****religious war**: n., /ree-lij'@s wor/**Revision 2.1.1??? 

Added

Revision 2.2.1??? 

Deleted: subsumed by 'holy wars'

> \[from Usenet, but may predate it\] _flame war_s
> over _religious issues_. 

### Deleted before 2.2.1

**[cell-repair machines][40]**

****

****cell-repair machines**: n.**Revision 2.1.1??? 

Added

Revision 2.2.1??? 

Deleted: insufficient relevance

> An often-discussed probable consequence of
> _nanotechnology_; _nanobots_
> specifically programmed to repair tissue at the cellular level. Possible
> uses include reversing freezing damage from _cryonics_
> procedures and correction of mutagen-damaged DNA (including eradication of
> retroviruses and oncogenes).

### Deleted before 2.3.1

**[big BLT, the][41]**

**[BIN][42]**

**[cryonics][43]**

**[diablo][44]**

**[DMP][45]**

**[dragon][46]**

**[fuzz][47]**

**[JRN, JRL][48]**

**[IMPCOM][49]**

**[JSYS][50]**

**[output spy][51]**

**[phantom][52]**

**[REL][53]**

**[SAV][54]**

**[SHR][55]**

**[STY][56]**

**[UUO][57]**

**[XGP][58]**

**[yoyo][59]**

****

****big BLT, the**: n., /big belt, th@/**Revision 1.1.0??? 

Added: originally as part of 'PPN'.

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: the PDP-10 is long dead

> \[obs.\] Shuffling operation on the PDP-10 under some operating systems
> that consumes a significant amount of computer time. See
> _BLT_ in the main listing.

****

****BIN**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: ITS is long dead

> \[short for BINARY; used as a second file name on ITS\]

> 1\. n. Binary. 

> 2\. BIN FILE: A file containing
> the BIN for a program. Usage: used at MIT, which runs on ITS. The
> equivalent term at Stanford is DMP (pronounced "dump") FILE. Other names
> used include SAV ("save") FILE (DEC and Tenex), SHR ("share") and LOW FILES
> (DEC), and EXE ("ex'ee") FILE (DEC and Twenex). Also in this category are
> the input files to the various flavors of linking loaders (LOADER, LINK-10,
> STINK), called REL FILES.

****

****cryonics**: n.**Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: insufficient relevance

> The practice of freezing oneself in hopes of being revived in the
> future by _cell-repair machines_. A possible route to
> technological immortality already taken by 1990 by more than a handful of
> persons with terminal illnesses.

****

****diablo**: /dee-ah'blow/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: The Diablo is long dead.

> 1\. \[from the Diablo printer\] n.
> Any letter- quality printing device. n.

> 2\. v. To produce letter-quality
> output from such a device. See _lase_.

****

****DMP**: /dump/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: OS long dead.

> See _BIN_.

****

****dragon**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: ITS is long dead.

> \[ITS; UNIX calls this a _daemon_ or
> _demon_\] A program similar to a
> _daemon_, except that it doesn't sit around waiting
> for something to happen, but is instead used by the system to perform
> various useful tasks that just have to be done periodically. A typical
> example would be an accounting program that accumulates statistics, keeps
> track of who is logged in, and so on. Another example: most timesharing
> systems have several terminals, and at any given time some are in use and
> some are sitting idle; the idle ones usually sit there with some idiotic
> message on their screens, such as "Logged off.", from the last
> time someone used it. The ITS timesharing system at MIT puts these idle
> terminals to good use by displaying useful information on them, such as who
> is using the computer, where they are, what they're doing, what their
> telephone numbers are, and so on, along with other information such as
> pretty pictures (the picture collection included a unicorn, Snoopy, and the
> U.S.S. Enterprise from Star Trek). All this information was displayed on
> idle terminals by the \`name dragon', so called because it originally
> printed just the names of the users. (That it now shows all kinds of
> things, including useless though pretty pictures, is an example of
> _creeping featurism_.) The name dragon is a program
> started up by the system, and it runs about every five minutes and updates
> the information on all idle terminals.

****

****fuzz**: n.**Revision 2.1.1??? 

Added

Revision 2.6.3??? 

Deleted: techspeak

> In floating-point arithmetic, the maximum difference allowed between
> two quantities for them to compare equal. Has to be set properly relative
> to the FPU's precision limits. See _fudge factor_.
> This term is particularly common among APL hackers.

****

****JRN, JRL**: n., /jay ahr en/, /jay ahr el/**Revision 1.5.0??? 

Added: originally as part of the 'PPN'

Revision 2.2.1??? 

Added

Revision 2.3.1??? 

Deleted: TOPS-10 is long dead

> The names JRN and JRL were sometimes used as example names when
> discussing PPNs (q.v.); they were understood to be programmer names for
> (fictitious) programmers named "J. Random Nerd" and
> "J. Random Loser" (see _J. Random_). For
> example, one might say "To log in, type log one comma jay are
> en" (that is, "\[log1,JRN\]"), and the listener will
> understand that he should use his own computer id in place of
> "\[JRN\]".

****

****IMPCOM**: /imp'kom/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: totally oboslete

> See _TELNET_. This term is now nearly
> obsolete.

****

****JSYS**: /jay'sis/, /jay'sigh/, v.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: The PDP-10 is long dead.

> \[Jump to SYStem\] See _UUO_.

****

****output spy**: n.**Revision 2.2.1??? 

Added

Revision 2.3.1??? 

Deleted: ITS is gone

> On the ITS system there was a program that allowed you to see what
> is being printed on someone else's terminal. It works by
> "spying" on the other guy's output, by examining the insides
> of the monitor system. It could do this because the MIT system purposely
> had very little in the way of "protection" that prevents one
> user from interfering with another. Fair is fair, however. There was
> another program that would automatically notify you if anyone starts to spy
> on your output. It worked in exactly the same way, by looking at the
> insides of the operating system to see if anyone else was looking at the
> insides that have to do with your output. This "counterspy"
> program was called JEDGAR (pronounced as two syllables: /jed'gr/), in honor of the former head of
> the FBI. By the way, the output spy program is called OS. Throughout the
> rest of computer science, and also at IBM, OS means "operating
> system", but among old-time ITS hackers it almost always meant
> "output spy".

****

****phantom**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: SAIL is ancient history.

> \[Stanford\] The SAIL equivalent of a _dragon_
> Typical phantoms included the accounting program, the news-wire monitor,
> and the LPT and XGP spoolers. UNIX and most other environments call this
> sort of program a background _demon_ or
> _daemon_.

****

****REL**: /rel/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted

> See _BIN: TOPS-10 is long dead._ in the main
> listing. Short for \`relocatable', used on the old TOPS-10 OS.

****

****SAV**: /sayv/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: TOPS-10 is long dead.

> See _BIN_.

****

****SHR**: /sheir/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: TOPS-10 is long dead.

> See _BIN_.

****

****STY**: /stie/, _not_, /ess tee wie/, n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: TOPS-10 is long dead.

> \[ITS\] A pseudo-teletype, which is a two-way pipeline with a job on
> one end and a fake keyboard-tty on the other. Also, a standard program
> which provides a pipeline from its controlling tty to a pseudo-teletype
> (and thence to another tty, thereby providing a "sub-tty").
> This is MIT terminology; the SAIL, DEC and UNIX equivalent is PTY (see main
> text).

****

****UUO**: /yoo-yoo-oh/, n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: TOPS-10 is long dead.

> \[short for "Un-Used Operation"\] A PDP-10 system monitor
> call. The term "Un-Used Operation" comes from the fact that,
> on PDP-10 systems, monitor calls are implemented as invalid or illegal
> machine instructions, which cause traps to the monitor (see
> _trap_). The SAIL manual describing the available
> UUOs has a cover picture showing an unidentified underwater object. See
> _YOYO_. \[Note: _DEC_
> salescritters since decided that "Un-Used Operation" sounds
> bad, so UUO now stands for "Unimplemented User Operation".\]
> Tenex and Twenex systems use the JSYS machine instruction (q.v.), which is
> halfway between a legal machine instruction and a UUO, since KA-10 Tenices
> implement it as a hardware instruction which can be used as an ordinary
> subroutine call (sort of a "pure JSR").

****

****XGP**: /eks-jee-pee/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: This hardware is ancient
history.

> 1\. n. Xerox Graphics
> Printer.

> 2\. v. To print something on the
> XGP. "You shouldn't XGP such a large file."

****

****yoyo**: /yoh'yoh/, n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted: TOPS-10 is long dead.

> _DEC_ service engineers' slang for
> _UUO_. Usage: rare at Stanford and MIT, has been
> found at random DEC installations.

### Deleted before 2.5.1

**[follow-on][60]**

**[go away][61]**

**[How hard would it be][62]**

**[IRP][63]**

**[layer][64]**

**[leading-edge][65]**

**[organic debugging][66]**

**[price/performance][67]**

**[utility][68]**

**[wait state][69]**

****

****follow-on**: n.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: not really hacker-speak.

> A new release or version of a product, sufficiently different to
> merit a new designation but including all the bugs and problems of the
> previous product architecture (this is the usual result of being
> "compatible" with previous releases).

****

****go away**: v.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: mainstream.

> To vanish inexplicably. Normally used in a kind of prayer or litany:
> "With a bit of luck, that problem will go away when we install
> Release XXX".

****

****How hard would it be**: adv.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: mainsream.

> A plaintive litany used when venturing suggestions for changes.
> Immediately precedes some preposterously difficult proposal which to the
> requestor (and any other reasonable person) seems simple. From experienced
> users, a wry acknowledgement that the proposition may well be costly, but
> is nevertheless desirable. "How hard would it be to remove the
> length restriction on userids?" See also
> _WIBNI_.

****

****IRP**: v., /erp/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted

Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: MIDAS is long dead.

> \[from the MIDAS pseudo-op which generates a block of code repeatedly,
> substituting in various places the car and/or cdr of the list(s) supplied
> at the IRP\] To perform a series of tasks repeatedly with a minor
> substitution each time through. "I guess I'll IRP over these
> homework papers so I can give them some random grade for this
> semester."

****

****layer**: n.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: techspeak.

> A collection of hardware or software that can be considered to form
> a layer within the structure of an operating system or architecture.
> Conceptually, layers are smoothly overlaid on each other with a clean
> interface between each, as in an onion. Upon detailed inspection, however,
> it will be often be seen that the tough-skinned and prickly globe artichoke
> is often a more accurate model.

****

****leading-edge**: adj.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: not enough hacker relevance.

> 1\. At the forefront of innovation and technology.

> 2\. Used in _marketroid_-speak to describe
> technology that is four years out of date and is therefore mature enough to
> be used in a commercial product.

****

****organic debugging**: n.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: lame.

> \[IBM\] A parody of some fashionable techniques for improving the
> quality of software. Reportedly, the output from a compilation or assembly
> of the suspect program is placed on the floor, with a large flat dish on
> top of it, and an indoor plant in a pot is placed in the centre of the
> dish. The dish is then filled with water. The principle is that any bugs
> in the program will be attracted towards the house plant and drown as they
> try to cross the intervening water. From statistical evidence this seems
> about as effective a technique as many others currently in use.

****

****price/performance**: n.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: insufficient hacker relevance.

> An undefined measure of value-for-money. As in "The XYZ offers
> improved price/performance". See _benchmark_,
> _machoflops_.

****

****utility**: n.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: techspeak/.

> A program that provides a general service that may have a variety of
> uses. For example, sorting and printing programs are often called
> utilities. The name implies a lack of novelty, and describes a
> \`bread-and-butter' program.

****

****wait state**: n.**Revision 2.4.3??? 

Added

Revision 2.5.1??? 

Deleted: techspeak.

> 1\. A period during which a processor is idle, for example, waiting
> for input, output, or memory activity to complete.

> 2\. Also used of humans waiting on some event to act.

### Deleted before 2.6.1

**[belly up][70]**

**[black box][71]**

**[bottleneck][72]**

**[close][73]**

**[hot key][74]**

**[link][75]**

**[listing][76]**

**[mixed case][77]**

**[mount][78]**

**[null device][79]**

**[panic][80]**

**[port][81]**

**[retrofit][82]**

**[sadistics][83]**

**[script][84]**

**[SUPDUP][85]**

****

****belly up**: adj.**Revision 2.4.3??? 

Added

Revision 2.6.1??? 

Deleted: mainstream.

> \[think of a dead fish\] Down, and it stinks. Used of hardware which
> suddenly stops working, especially when the _stoppage_
> is ideally timed to disrupt a development schedule. Esp. found in the
> phrase \`to go belly up' or \`gone belly up'. See also _casters-up
> mode_. _down_.

****

****black box**: n.**Revision 2.4.1??? 

Added

Revision 2.6.1??? 

Deleted: mainsteam.

> Something which is sealed off (opaque) so the inner workings aren't
> visible, typically said of very complex algorithms. "That image
> restoration technique is a black box." The application to
> _hardware_ is general technical English, of
> course.

****

****bottleneck**: adj.**Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Renamed: 'bottlenecked' -\> 'bottleneck' (deduced from
diffs)

Revision 2.6.1??? 

Deleted: techspeak.

> A slow code section, algorithm, or hardware subsystem through which
> computation must pass (see also _hot spot_); anything
> with lower _bandwidth_ than is available for the rest
> of the computation. A system is said to be
> _bottlenecked_ when performance is usually limited by
> contention for one particular resource (such as disk, memory, or processor
> _clocks_); the opposite condition is called
> _balanced_, which is more jargon in the strict sense
> and may be found in technical dictionaries.
> 
> The connection between the central processor and memory is often
> called the _von Neumann bottleneck_. This term was
> coined by John Backus in his 1978 Turing Award lecture; it is now standard
> in the computer science literature but is also the canonical example of a
> bottleneck to hackers.

****

****close**: /klohz/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> \[from the verb \`to close', thus the /z/ sound\] 

> 1\. n. Abbreviation for \`close
> (or right) parenthesis', used when necessary to eliminate oral ambiguity.
> See _open_.

> 2\. adj. Of a delimiting
> character, used at the right-hand end of a grouping. Used in such terms as
> _close parenthesis_, _close
> bracket_, etc. 

> 3\. vt. To release a file or communication channel after
> access.

****

****hot key****Revision 2.4.3??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> 1\. n. A keystroke (or
> combination of keystrokes) that switches environments; esp. used if it
> flips between different modes or screens of a full-screen interface.
> Perhaps so called because they are always active or \`hot'; possibly related
> to _hot buttons_ in
> _marketroid_-speak. 

> 2\. v. To switch
> environments.

****

****link**: n.**Revision 2.4.3??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> A network connection between two machines. Usage: "Is that
> link down again?"

****

****listing**: n.**Revision 2.5.1??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> A physical paper printout (as opposed to on-screen display) of
> program source, or of the results (interspersed with error and status
> messages) of a compilation or assembly run. What one grovels over when
> performing a _desk check_. Both the term \`listing'
> and the thing it describes are now much less common than formerly, as
> modern time-sharing operating systems and powerful interactive editors have
> made it advantageous for hackers to do effectively all of their work
> on-line.

****

****mixed case**: adj.**Revision 2.4.3??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> Of source code, commentary, system messages, etc., not in all upper
> case or all lower case, and therefore easy to read and understand. Used
> esp. in opposition to older designs that are case-insensitive and use an
> all-caps character set.

****

****mount**: vt.**Revision 2.1.1??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> 1\. To attach a removable physical storage volume to a machine. In
> elder days and on mainframes this verb was used almost exclusively of
> tapes; nowadays it is more likely to refer to a disk or disk pack. 

> 2\. By extension, to attach any removable device such as a sensor,
> robot arm, or _meatware_ subsystem (see
> _scratch monkey_). 

> 3\. \[UNIX\] To make a _logical_ volume of some
> sort available for use. The volume in question may or may not be removable
> and may be just one partition of a physical device.

****

****null device**: n.**Revision 2.2.1??? 

Added

Revision 2.9.6??? 

Deleted: techspeak.

> \[techspeak\] A _logical_ input/output device
> connected to the _bit bucket_; when you write to it
> nothing happens, when you read from it you see an end-of-file condition.
> Useful for discarding unwanted output or using interactive programs in a
> _batch_ mode. See
> _/dev/null_. 

****

****panic**: vi.**Revision 2.1.1??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> \[UNIX\] An action taken by a process or the entire operating system
> when an unrecoverable error is discovered. The action usually consists of:
> (1) displaying localized information on the controlling terminal, (2)
> saving, or preparing for saving, a memory image of the process or operating
> system, and (3) terminating the process or rebooting the system.

****

****port****Revision 2.5.1??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> 1\. v.,n. Describes the act of
> moving, translating, reconfiguring, and adapting software from one machine
> architecture and/or operating system (the _source
> environment_) to run on a different one (the _target
> environment_). Until recently and except among a relatively
> small group of modern operating systems this process has ranged from
> extremely painful up to flat-out impossible. The ubiquity of the C
> language and the spread of the UNIX operating system have, fortunately,
> done much to change this.

> 2\. \[from mainstream \`port' for a door or gate\] n. Anything one might plug a peripheral or
> communications line into; as in a \`serial port' or \`parallel port'.

****

****retrofit**: v.**Revision 2.5.1??? 

Added

Revision 2.6.1??? 

Deleted: general to engineers.

> To graft some pieces from newer technology onto a piece of software
> or hardware representing an older one. This often results in a crocky,
> inelegant compromise between new and old. The term implies use of the
> older stuff in ways the designers didn't anticipate. Some of the bizarre
> things done during the 1970s to old-style batch operating systems like
> _GECOS_ and IBM's OS/360 in order to make them crudely
> interactive stand out as examples. More recently, personal computer
> hackers have frequently been known to graft new floppy and hard-disk
> devices onto obsolete hardware in order to preserve software written for a
> particular processor, screen and keyboard combination.

****

****sadistics**: /s@-dis'tiks/, n.**Revision 2.1.1??? 

Added

Revision 2.6.1??? 

Deleted: no evidence of live usage.

> University slang for statistics and probability theory, often used
> by hackers.

****

****script**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Deleted

Revision 2.4.3??? 

Added

Revision 2.6.1??? 

Deleted: techspeak.

> 1\. A program written in _shell_; a
> _batch file_ (see _batch_). A
> set of instructions which can be fed to a machine as though the user had
> typed them. 

> 2\. A transcript of some interaction with a machine.

****

****SUPDUP**: v.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.6.1??? 

Deleted: SUPDUP is long dead.

> To communicate with another ARPAnet host using the SUPDUP program,
> which is a SUPer-DUPer TELNET talking a special display protocol used
> mostly in talking to ITS sites. Sometimes abbreviated to SD.

### Deleted before 2.7.1

**[grungy][86]**

**[wow][87]**

**[asymptotic][88]**

**[bat file][89]**

**[sluggy][90]**

**[spin-lock][91]**

****

****grungy**: /gruhn'jee/, adj.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.7.1??? 

Deleted: mainstream.

> Incredibly dirty, greasy, or grubby. Anything which has been washed
> within the last year is not really grungy. Also used metaphorically; hence
> some programs (especially crocks) can be described as grungy.
> 
> The earliest print use anybody has reported to us of \`grungy' is from
> the National Lampoon parody _Bored Of the Rings_,
> dating from the late 1960s. It has been suggested that this term
> originated with Vietnam vets. It has recently (as of 1991) also become
> common in mainstream English.

****

****wow**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.7.1??? 

Deleted: merged into 'ASCII'.

> See _excl_.

****

****asymptotic**: adj.**Revision 2.2.1??? 

Added

Revision 2.7.1??? 

Deleted: general to all mathematically-literate
people.

> Infinitely close to. This is used in a generalization of its
> mathematical meaning to allege that something is _within epsilon
> of_ some standard, reference, or goal (see
> _epsilon_).

****

****bat file**: n.**Revision 2.6.1??? 

Added

Revision 2.7.1??? 

Deleted: techspeak.

> \[MS-DOS/Windows\] Abbreviation for _batch file_,
> the MSDOS equivalent of the UNIX shell script, derived from the .BAT
> extension required for the command interpreter to find the batch file and
> execute it.

****

****sluggy**: /sluhg'ee/, adj.**Revision 2.1.1??? 

Added

Revision 2.7.1??? 

Deleted: No evidence of live use.

> Hackish variant of \`sluggish'. Used only of people, esp. someone
> just waking up after a long _gronk out_.

****

****spin-lock**: n.**Revision 2.2.1??? 

Added

Revision 2.8.1??? 

Deleted: techspeak.

> \[Cambridge\] A _busy-wait_. Preferred in
> Britain.

### Deleted before 2.8.1

**[swapped][92]**

**[what][93]**

**[humongous][94]**

****

****swapped**: adj.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Renamed: 'swapped' -\> 'swap'Renamed: 2 infix -\> 2 (infix)
(deduced from diffs)

Revision 2.1.1??? 

Renamed: 'swap' -\> 'swapped' (deduced from
diffs)

Revision 2.6.1??? 

Added

Revision 2.8.1??? 

Deleted: subsumed by 'page in'.

> From the older (per-task) method of using secondary storage devices
> to implement support for multitasking. Something which is
> _swapped in_ is available for immediate use in main
> memory, and otherwise is _swapped out_. Often used
> metaphorically to refer to people's memories ("I read the Scheme
> Report every few months to keep the information swapped in.") or to
> their own availability ("I'll swap you in as soon as I finish looking
> at this other problem."). Compare _page in_,
> _page out_.

****

****what**: n.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.8.1??? 

Deleted: merged into 'ASCII'.

> The question mark character ("?"). See QUES. Usage: rare, used
> particularly in conjunction with _wow_.

****

****humongous**: adj., /hyoo-mohng'gus/, alt. /hyoo-muhng'gus/**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 2.4.1??? 

Renamed: 'humongous' -\> 'humungous' (deduced from
diffs)

Revision 2.8.1??? 

Deleted: has become mainstream slang since
1983\.

> See _hungus_.

### Deleted before 2.9.\[123456\]

**[blazer][95]**

**[breakage][96]**

**[FAtt][97]**

**[firmware][98]**

**[FReq][99]**

**[ONE BELL SYSTEM (IT WORKS)][100]**

**[pipeline][101]**

****

****blazer**: n.**Revision 2.1.1??? 

Added

Revision 2.9.6??? 

Deleted: The Trailblazer is long dead.

> (alt.: 'blazer) Nickname for
> any of the Telebit Trailblazers, a line of expensive but extremely reliable
> and effective high-speed modems, popular at UNIX sites that pass large
> volumes of _email_ and _USENET_
> news. 

****

****breakage****Revision 2.1.1??? 

Added

Revision 2.9.6??? 

Deleted: No evidence of live usage among
hackers.

> 1\. Brokenness and the consequent mess. 

> 2\. \[IBM\] n. The extra people that must be added to an organization
> because its master plan has changed; used esp.: of software and hardware
> development teams. 

****

****FAtt**: n.**Revision 2.6.1??? 

Added

Revision 2.9.6??? 

Deleted

> \[FidoNet\] Abbreviation for _File
> Attach_. 

****

****firmware**: n.**
> 
> Software installed into a computer-based piece of equipment on ROM.
> So-called because it's harder to change than software but easier than
> hardware.

****

****FReq**: n.**Revision 2.4.1??? 

Added

Revision 2.9.6??? 

Deleted: FidoNet is no longer
interesting.

> \[FidoNet\] Abbreviation for _File
> Request_. 

****

****ONE BELL SYSTEM (IT WORKS)****Revision 2.1.1??? 

Added

Revision 2.3.1??? 

Renamed: 'ONE BELL SYSTEM' -\> 'ONE BELL SYSTEM' (IT WORKS)
(deduced from diffs)

Revision 2.9.6??? 

Deleted: Not funny enough.

> This was the output from the old UNIX V6 \`1' command. The \`1'
> command then did a random number roll that gave it a one-in-ten chance of
> recursively executing itself. 

****

****pipeline**: n.**Revision 2.1.1??? 

Added

Revision 2.9.6??? 

Deleted: techspeak.

> \[UNIX: orig. by Doug McIlroy; now also used under MS-DOS and
> elsewhere\] A chain of _filter_ programs connected
> \`head-to-tail' so that the output of one becomes the input of the next.
> Under UNIX, user utilities can often be implemented or at least prototyped
> by a suitable collection of pipelines and temp-file grinding encapsulated
> in a shell script (this is called _plumbing_); this is
> much less effort than writing C every time, and the capability is
> considered one of UNIX's major winning features. 

### Deleted before 2.9.12

### Note

Most of these were removed due to my decision to drop IRC/MUD
slang of at best marginal interest to hackers and low giggle
or information value.

**[salsman][102]**

**[archive][103]**

**[arc wars][104]**

**[berserking][105]**

**[i14y][106]**

**[i18n][107]**

**[lame][108]**

**[BartleMUD][109]**

**[posing][110]**

**[tinycrud][111]**

**[K-line][112]**

**[Q-line][113]**

**[reset][114]**

**[subshell][115]**

**[brand brand brand][116]**

**[fuggly][117]**

**[hack-and-slay][118]**

**[arc][119]**

**[card][120]**

**[silicon foundry][121]**

**[essentials][122]**

**[fab][123]**

****

****salsman**: /salz'm@n/, v.**Revision 2.9.6??? 

Added

Revision 2.9.12??? 

Deleted: at salsman's request)

> To flood a mailing list or newsgroup with huge amounts of useless,
> trivial or redundant information. From the name of a hacker who has
> frequently done this on some widely distributed mailing lists.

****

****archive**: n.**Revision 2.8.1??? 

Added

Revision 2.9.12??? 

Deleted: techspeak.

> 1\. A collection of several files bundled into one file by a program
> such as
> ar(1),
> tar(1),
> cpio(1),
> or _arc_ for shipment or archiving (sense 2). See
> also _tar and feather_. 

> 2\. A collection of files or archives (sense 1) made available from
> an archive site via
> _FTP_ or an email server.

****

****arc wars**: n.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: old flamewar, no longer
interesting.

> \[primarily MSDOS\] _holy wars_ over which
> archiving program one should use. The first arc war was sparked when
> System Enhancement Associates (SEA) sued PKWare for copyright and trademark
> infringement on its ARC program. PKWare's PKARC outperformed ARC on both
> compression and speed while largely retaining compatibility (it introduced
> a new compression type that could be disabled for backward-compatibility).
> PKWare settled out of court to avoid enormous legal costs (both SEA and
> PKWare are small companies); as part of the settlement, the name of PKARC
> was changed to PKPAK. The public backlash against SEA for bringing suit
> helped to hasten the demise of ARC as a standard when PKWare and others
> introduced new, incompatible archivers with better compression
> algorithms. 

****

****berserking**: vi.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: MUD-specific

> A _MUD_ term meaning to gain points
> _only_ by killing other players and mobiles (non-player
> characters). Hence, a Berserker-Wizard is a player character that has
> achieved enough points to become a wizard, but only by killing other
> characters. Berserking is sometimes frowned upon because of its inherently
> antisocial nature, but some MUDs have a berserker mode in which a player becomes
> _permanently_ berserk, can never flee from a fight,
> cannot use magic, gets no score for treasure, but does get double kill
> points. "Berserker wizards can seriously damage your elf!"
> 

****

****i14y**: n.**Revision 2.4.3??? 

Added

Revision 2.9.12??? 

Deleted: techspeak.

> Abbrev. for 'interoperability', with the
> '14' replacing fourteen letters. Used in the
> _X_ (windows) community. Refers to portability and
> compatibility of data formats (even binary ones) between different programs
> or implementations of the same program on different machines. 

****

****i18n**: //, n.**Revision 2.4.3??? 

Added

Revision 2.9.12??? 

Deleted: techspeak.

> Abbrev. for \`internationali{z,s}ation', with the 18 replacing 18
> letters. Used in the _X_ (windows) community. 

****

****lame**: adj.**Revision 2.9.12??? 

Deleted: mainstream.

> Weak; losing; not up to the job. Hackish use resembles the
> mainstream idiom in phrases like "a lame excuse" but has
> special connotations. Some hacker subcultures use it for people or designs
> that display intelligence but never follow through on their promise. Thus,
> a lame design might have clever ideas in it, but fail due to laziness or
> poor debugging on the part of the implementer. A lame person (or lamer) may be bright and interesting, but
> unable to accomplish much due to chronic flakiness. Marked compounds like
> 'non-lame' and 'lameitude' flourish.

****

****BartleMUD**: /bar'tl-muhd/, n.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: subsumed by 'MUD'.

> Any of the MUDs derived from the original MUD game by Richard Bartle
> and Roy Trubshaw (see _MUD_). BartleMUDs are noted
> for their (usually slightly offbeat) humor, dry but friendly syntax, and
> lack of adjectives in object descriptions, so a player is likely to come
> across \`brand172', for instance (see _brand brand
> brand_). Bartle has taken a bad rap in some MUDding circles for
> supposedly originating this term, but (like the story that MUD is a
> trademark) this appears to be a myth; he uses \`MUD1'.

****

****posing**: n.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: MUD-specific, not general to
hackers.

> On a _MUD_, the use of : or
> an equivalent command to announce to other players that one is taking a
> certain physical action that has no effect on the game (it may, however,
> serve as a social signal or propaganda device that induces other people to
> take game actions). For example, if one's character name is Firechild, one
> might type ': looks delighted at the idea and begins hacking on the
> nearest terminal' to broadcast a message that says "Firechild
> looks delighted at the idea and begins hacking on the nearest
> terminal". See _RL_.

****

****tinycrud**: /ti:'nee-kruhd/, n.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: MUD-specific, not general to
hackers.

> 1\. A pejorative used by habitues of older game-oriented
> _MUD_ versions for TinyMUDs and other user-extensible
> _MUD_ variants; esp.: common among users of the rather
> violent and competitive AberMUD and MIST systems. These people justify the
> slur on the basis of how (allegedly) inconsistent and lacking in genuine
> atmosphere the scenarios generated in user extensible MUDs can be. Other
> common knocks on them are that they feature little overall plot, bad game
> topology, little competitive interaction, etc. --- not to mention the
> alleged horrors of the TinyMUD code itself. This dispute is one of the MUD
> world's hardiest perennial _holy wars_. 

> 2\. TinyMud-oriented chat on the USENET group rec.games.mud and elsewhere, especially
> _newbie_ questions and flamage.

****

****K-line**: v.**Revision 2.9.10??? 

Added

Revision 2.9.12??? 

Deleted: IRC-specific, not general to
hackers.

> \[IRC\] To ban a particular person from an _IRC_
> server, usually for grossly bad _netiquette_. Comes
> from the \`K' code used to accomplish this in IRC's configuration
> file.

****

****Q-line**: v.**Revision 2.9.10??? 

Added

Revision 2.9.12??? 

Deleted: IRC-specific, not general to
hackers.

> To ban a particular _IRC_ server from
> connecting to one's own; does to it what _K-line_ does
> to an individual. Since this is applied transitively, it has the effect of
> partitioning the IRC network, which is generally a _Bad
> Thing_.

****

****reset**: v.**Revision 2.9.6??? 

Added

Revision 2.9.12??? 

Deleted: MUD-specific, not general to
hackers.

> \[the MUD community\] In AberMUD, to bring all dead mobiles to life
> and move items back to their initial starting places. New players who can't
> find anything shout "Reset! Reset!" quite a bit. Higher-level
> players shout back "No way!" since they know where points are
> to be found. Used in _RL_, it means to put things
> back to the way they were when you found them.

****

****subshell**: /suhb'shel/**Revision 2.1.1??? 

Added

Revision 2.9.12??? 

Deleted: techspeak.

> \[UNIX, MS-DOS\] An OS command interpreter (see
> _shell_) spawned from within a program, such that exit
> from the command interpreter returns one to the parent program in a state
> that allows it to continue execution. Compare _shell
> out_; oppose _chain_. 

****

****brand brand brand**: n.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: MUD-specific, not general to
hackers.

> Humorous catch-phrase from _BartleMUD_s, in
> which players were described carrying a list of objects, the most common of
> which would usually be a brand. Often used as a joke in _talk
> mode_ as in "Fred the wizard is here, carrying brand ruby
> brand brand brand kettle broadsword flamethrower". A brand is a
> torch, of course; one burns up a lot of those exploring dungeons. Prob.:
> influenced by the famous Monty Python _Spam_
> skit.

****

****fuggly**: /fuhg'lee/, adj.**Revision 2.1.1??? 

Added

Revision 2.9.12??? 

Deleted: mainstream

> Emphatic form of _funky_; funky + ugly).
> Unusually for hacker jargon, this may actually derive from black
> street-jive. To say it properly, the first syllable should be growled
> rather than spoken. Usage: humorous. "Man, the
> _ASCII_-to- _EBCDIC_ code in that
> printer driver is _fuggly_." See also
> _wonky_. 

****

****hack-and-slay**: v.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: MUD-specific, not general to
hackers.

> (also hack-and-slash) 

> 1\. To play a _MUD_ or go mudding, especially
> with the intention of _berserking_ for pleasure.
> 

> 2\. To undertake an all-night programming/hacking session,
> interspersed with stints of mudding as a change of pace. This term arose
> on the British academic network amongst students who worked nights and
> logged onto Essex University's MUDs during public-access hours (2 @sc{A.M.}
> to 7 @sc{A.M.}). Usually more mudding than work was done in these
> sessions. 

****

****arc**: vt.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: obsolete, not flavorful.

> \[primarily MSDOS\] To create a compressed archive from a group of
> files using SEA ARC, PKWare PKARC, or a compatible program. Rapidly
> becoming obsolete as the ARC compression method is falling into disuse,
> having been replaced by newer compression techniques. See _tar
> and feather_, _zip_. 

****

****card**: n.**Revision 2.4.3??? 

Added

Revision 2.9.12??? 

Deleted: techspeak.

> 1\. An electronic printed-circuit board (see also _tall
> card_, _short card_. 

> 2\. obs. Syn. _punched card_. 

****

****silicon foundry**: n.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: techspeak.

> A company that _fab_s chips to the designs of
> others. As of the late 1980s, the combination of silicon foundries and
> good computer-aided design software made it much easier for
> hardware-designing startup companies to come into being. The downside of
> using a silicon foundry is that the distance from the actual
> chip-fabrication processes reduces designers' control of detail. This is
> somewhat analogous to the use of _HLL_s versus coding
> in assembler.

****

****essentials**: n.**Revision 2.1.1??? 

Added

Revision 2.9.12??? 

Deleted: gets dated too often.

> Things necessary to maintain a productive and secure hacking
> environment. "A jug of wine, a loaf of bread, a 300MHz Pentium box
> with 64 meg of core and a 2-gigabyte disk running Linux with source and X
> windows and Emacs and SLIP via a 56K modem to a friendly Internet site, and
> thou." 

****

****fab**: /fab/, v.**Revision 2.4.1??? 

Added

Revision 2.9.12??? 

Deleted: techspeak.

> \[from 'fabricate'\] 

> 1\. To produce actual silicon from a chip design. To a hacker,
> fab is practically never short for
> 'fabulous'. 

> 2\. fab line: the production
> system (lithography, diffusion, etching, etc.:) for chips at a chip
> manufacturer. Different fab lines
> are run with different process parameters, die sizes, or technologies, or
> simply to provide more manufacturing volume. 

### Deleted before 3.0.0

**[unroll][124]**

****

****unroll**: v.**Revision 2.9.10??? 

Added

Revision 3.0.0??? 

Deleted: techspeak.

> To repeat the body of a loop several times in succession. This
> optimization technique reduces the number of times the loop-termination
> test has to be executed. But it only works if the number of iterations
> desired is a multiple of the number of repetitions of the body. Something
> has to be done to take care of any leftover iterations --- such as
> _Duff's device_. 

### Deleted before 3.2.0

**[toto][125]**

**[unleaded][126]**

**[spoo][127]**

**[spooge][128]**

****

****toto**: /toh-toh'/, n.**Revision 2.6.1??? 

Added

Revision 3.1.1??? 

Deleted: info merged into \`metasyntactic
variable'

Revision 3.2.0??? 

Deleted: subsumed into 'metasyntactic variiable'

> Reportedy the default scratch file name among French-speaking
> programmers --- in other words, a francophone _foo_.
> It is reported that the phonetic mutations "titi",
> "tata", and "tutu" canonically follow toto, analogously to
> _bar_, _baz_ and
> _quux_ in English. 

****

****unleaded**: adj.**Revision 2.9.10??? 

Added

Revision 3.2.0??? 

Deleted: mainstream.

> Said of decaffeinated coffee, Diet Coke, and other imitation
> _programming fluid_s. "Do you want regular or
> unleaded?" Appears to be widespread among programmers associated
> with the oil industry in Texas (and probably elsewhere). Usage: silly, and
> probably unintelligible to the next generation of hackers. 

****

****spoo**: n.**Revision 2.9.12??? 

Added

Revision 3.2.0??? 

Deleted: mainstream.

> Variant of _spooge_, sense 1\.

****

****spooge**: /spooj/**Revision 2.1.1??? 

Added

Revision 3.2.0??? 

Deleted: mainstream, in the sense of trash or
ejaculate.

> 1\. n. Inexplicable or arcane
> code, or random and probably incorrect output from a computer
> program.

> 2\. vi. To generate spooge (sense 1).

### Deleted before 3.3.2

**[mango][129]**

**[doco][130]**

**[devo][131]**

**[sendmail][132]**

****

****mango**: /mang'go/, n.**Revision 2.1.1??? 

Added

Revision 3.3.2??? 

Deleted: no evidence of live use.

> \[orig. in-house jargon at Symbolics\] A manager. Compare
> _mangler_. See also _devo_ and
> _doco_. 

****

****doco**: /do'koh/, n.**Revision 2.1.1??? 

Added

Revision 3.3.2??? 

Deleted: no evidence of live use.

> \[orig. in-house jargon at Symbolics\] A documentation writer. See
> also _devo_ and _mango_. 

****

****devo**: /dee'voh/, n.**Revision 2.1.1??? 

Added

Revision 3.3.2??? 

Deleted: no evidence of live use.

> \[orig. in-house jargon at Symbolics\] A person in a development
> group. See also _doco_ and
> _mango_. 

****

****sendmail**: n.**Revision 3.2.0??? 

Added

Revision 3.3.2??? 

Deleted: techspeak.

> The standard Unix mail agent; written by Eric Allman. It is very
> flexible, but has very _hairy_ configuration syntax
> and has had numerous security bugs, because it's a large, monolithic
> program which needs assume with root privileges part of the time. See also
> _bug-of-the-month club_ and _Great
> Worm_. 

### Deleted before 4.1.1

**[DEChead][133]**

**[double DECkers][134]**

**[Open DeathTrap][135]**

**[microtape][136]**

**[pig, run like a][137]**

**[altmode][138]**

**[AOS][139]**

**[chine nual][140]**

**[blow away][141]**

**[cruncha cruncha cruncha][142]**

**[CTY][143]**

**[JRST][144]**

**[news][145]**

**[fepped out][146]**

**[JFCL][147]**

**[PIP][148]**

**[NOMEX underwear][149]**

**[Pink-Shirt Book][150]**

****

****DEChead**: /dek'hed/, n.**Revision 2.6.1??? 

Added

Revision 4.1.0??? 

Deleted: obs. now that DEC is gone

> A _DEC_ _field servoid_.
> Not flattering. 

> \[from 'deadhead'\] A Grateful Dead fan working at DEC.
> 

****

****double DECkers**: n.**Revision 2.4.3??? 

Added

Revision 4.1.0??? 

Deleted: obs. now that DEC is gone

> Used to describe married couples in which both partners work for
> Digital Equipment Corporation. 

****

****Open DeathTrap**: n.**Revision 2.9.10??? 

Added

Revision 4.1.0??? 

Deleted: It turns out that Open DeathTrap referred to the
_project_ not the product. Makes it less
interesting.

> Abusive hackerism for the Santa Cruz Operation's \`Open DeskTop'
> product, a Motif-based graphical interface over their Unix. The funniest
> part is that this was coined by SCO's own developers.... Compare
> _AIDX_, _Macintrash_
> _Nominal Semidestructor_,
> _ScumOS_, _sun-stools_,
> _HP-SUX_.

****

****microtape**: /mi:'kroh-tayp/, n.**Revision 1.1.0??? 

Added

Revision 4.1.0??? 

Deleted: technology obsolete and no
flavor.

> Occasionally used to mean a DECtape, as opposed to a
> _macrotape_. A DECtape is a small reel, about 4
> inches in diameter, of magnetic tape about an inch wide. Unlike those for
> today's _macrotape_s, microtape drivers allowed random
> access to the data, and therefore could be used to support file systems and
> even for swapping (this was generally done purely for _hack
> value_, as they were far too slow for practical use). In their
> heyday they were used in pretty much the same ways one would now use a
> floppy disk: as a small, portable way to save and transport files and
> programs. Apparently the term microtape was actually the official term used
> within DEC for these tapes until someone coined the word
> 'DECtape', which, of course, sounded sexier to the
> _marketroid_s; another version of the story holds that
> someone discovered a conflict with another company's
> 'microtape' trademark. 

****

****pig, run like a**: v.**Revision 2.1.1??? 

Added

Revision 4.1.0??? 

Deleted: Both mainstream and incorrect; pigs actually run
rather fast

> To run very slowly on given hardware, said of software. Distinct
> from _hog_. 

****

****altmode**: n.,obs.**Revision 2.9.10??? 

Added

Revision 4.1.1??? 

Deleted: ITS/PDP-10 reference; no longer
live

> Syn. _alt_ sense 3\. Old
> _DEC_ terminology, now historical only.

****

****AOS****Revision 1.1.0??? 

Added

Revision 4.1.1??? 

Deleted: PDP-10 mnemonic; no longer live

> 1\. /aws/ (East Coast),
> /ay'os/ (West Coast) vt. obs. To increase the amount of
> something. "AOS the campfire." \[based on a PDP-10 increment
> instruction\] Usage: considered silly, and now obsolete. Now largely
> supplanted by _bump_. See _SOS_.
> 

> 2\. n. A
> _Multics_-derived OS supported at one time by Data
> General. This was pronounced /A-O-S/ or /A-os/. A spoof of the standard AOS system
> administrator's manual (_How to Load and Generate your AOS
> System_) was created, issued a part number, and circulated as
> photocopy folklore; it was called _How to Goad and Levitate your
> CHAOS System_. 

> 3\. n. Algebraic Operating
> System, in reference to those calculators which use infix instead of
> postfix (reverse Polish) notation. 

> 4\. A _BSD_-like operating system for the IBM
> RT.

> Historical note: AOS in sense 1 was the name of a
> _PDP-10_ instruction that took any memory location in
> the computer and added 1 to it; AOS meant \`Add One and do not Skip'. Why,
> you may ask, does the \`S' stand for \`do not Skip' rather than for \`Skip'?
> Ah, here was a beloved piece of PDP-10 folklore. There were eight such
> instructions: AOSE added 1 and then skipped the next instruction if the
> result was Equal to zero; AOSG added 1 and then skipped if the result was
> Greater than 0; AOSN added 1 and then skipped if the result was Not 0; AOSA
> added 1 and then skipped Always; and so on. Just plain AOS didn't say when
> to skip, so it never skipped.
> 
> For similar reasons, AOJ meant \`Add One and do not Jump'. Even more
> bizarre, SKIP meant \`do not SKIP'! If you wanted to skip the next
> instruction, you had to say \`SKIPA'. Likewise, JUMP meant \`do not JUMP';
> the unconditional form was JUMPA. However, hackers never did this. By
> some quirk of the 10's design, the _JRST_ (Jump and
> ReSTore flag with no flag specified) was actually faster and so was
> invariably used. Such were the perverse mysteries of assembler
> programming. 

****

****chine nual**: /sheen'yu-@l/, n. obs.**Revision 1.2.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.2.1??? 

Added

Revision 2.3.1??? 

Deleted

Revision 2.8.1??? 

Added

Revision 4.1.1??? 

Deleted: been dead since the early 1980s

> \[MIT\] The LISP Machine Manual, so called because the title was
> wrapped around the cover so only those letters showed on the front.

****

****blow away**: vt.**Revision 4.1.1??? 

Deleted: mainstream

> To remove (files and directories) from permanent storage, usually by
> accident. "He reformatted the wrong partition and blew away last
> night's netnews". Oppose _nuke_.

****

****cruncha cruncha cruncha**: /kruhn'ch@ kruhn'ch@ kruhn'ch@/, interj.**Revision 2.1.1??? 

Added

Revision 4.1.1??? 

Deleted: DejaNews suggests it's dead

> An encouragement sometimes muttered to a machine bogged down in a
> serious _grovel_. Also describes a notional sound
> made by groveling hardware. See _wugga wugga_,
> _grind_ (sense 3). 

****

****CTY**: /sit'ee/, /C-T-Y/, n.**Revision 1.1.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.2.1??? 

Added

Revision 4.1.1??? 

Deleted: the OSs that used this are 15 years
dead

> \[MIT\] The terminal physically associated with a computer's system
> _console_. The term is a contraction of \`Console
> _tty_', that is, \`Console TeleTYpe'. This
> _ITS_- and _TOPS-10_-associated
> term has become less common, as most Unix hackers simply refer to the CTY
> as 'the console'. 

****

****JRST**: /jerst/, v.**Revision 1.1.0??? 

Added

Revision 2.3.1??? 

Deleted

Revision 2.8.1??? 

Added

Revision 4.1.1??? 

Deleted: PDP-10 mnemonic; no longer live

> \[based on the PDP-10 jump instruction\] To suddenly change subjects,
> with no intention of returning to the previous topic.. Usage: rather rare,
> and considered silly. "Jack be nimble, Jack be quick; Jack jrst over
> the candle stick." This is even sillier. Why JRST and not JUMP?
> The PDP-10 JUMP instruction means "do not jump", as explained
> in the definition of AOS. The JUMPA instruction ("JUMP
> Always") does jump, but it isn't quite as fast as the JRST
> instruction (Jump and ReSTore flags). The instruction was used so
> frequently that the speed matters, so all PDP-10 hackers automatically used
> the faster though more obscure JRST instruction.

****

****news**: n.**Revision 2.9.6??? 

Added

Revision 4.1.1??? 

Deleted: see netnews.

> See _netnews_.

****

****fepped out**: /fept owt/, adj.**Revision 2.6.1??? 

Added

Revision 4.1.1??? 

Deleted: nobody's seen one since LISP
machines

> The Symbolics 3600 LISP Machine has a Front-End Processor called a
> \`FEP' (compare sense 2 of _box_). When the main
> processor gets _wedged_, the FEP takes control of the
> keyboard and screen. Such a machine is said to have fepped out or dropped into the fep.

****

****JFCL**: /jif'kl/, /jaf'kl/, /j@-fi'kl/**Revision 1.1.0??? 

Added

Revision 4.1.1??? 

Deleted: PDP-10 mnemonic; no longer live

> (alt. jfcl) To cancel or
> annul something. "Why don't you jfcl that out?" The fastest
> do-nothing instruction on older models of the PDP-10 happened to be JFCL,
> which stands for "Jump if Flag set and then CLear the flag";
> this does something useful, but is a very fast no-operation if no flag is
> specified. Geoff Goodfellow, one of the Steele-1983 co-authors, had JFCL
> on the license plate of his BMW for years. Usage: rare except among
> old-time PDP-10 hackers.

****

****PIP**: /pip/**Revision 2.2.1??? 

Added

Revision 4.1.1??? 

Deleted: PDP-10 reference; no longer
live

> \[Peripheral Interchange Program\] To copy; from the program PIP on
> CP/M, RSX-11, RSTS/E, TOPS-10, and OS/8 (derived from a utility on the
> PDP-6) that was used for file copying (and in OS/8 and RT-11 for just about
> every other file operation you might want to do). It is said that when the
> program was originated, during the development of the PDP-6 in 1963, it was
> called ATLATL (\`Anything, Lord, to Anything, Lord'; this played on the
> Nahuatl word _atlatl_ for a spear-thrower,
> with connotations of utility and primitivity that were no doubt quite
> intentional). See also _BLT_,
> _dd_, _cat_. 

****

****NOMEX underwear**: /noh'meks uhn'-der-weir/, n.**Revision 2.4.3??? 

Added

Revision 4.1.1??? 

Deleted: DejaNews suggests it was never
live

> \[Usenet\] Syn. _asbestos longjohns_, used
> mostly in auto-related mailing lists and newsgroups. NOMEX underwear is an
> actual product available on the racing equipment market, used as a fire
> resistance measure and required in some racing series. 

****

****Pink-Shirt Book****Revision 2.1.5??? 

Added

Revision 4.1.1??? 

Deleted: as dead as MS-DOS.

> _The Peter Norton Programmer's Guide to the IBM
> PC_. The original cover featured a picture of Peter Norton with
> a silly smirk on his face, wearing a pink shirt. Perhaps in recognition of
> this usage, the current edition has a different picture of Norton wearing a
> pink shirt. See also _book titles_. 

### Deleted before 4.1.2

**[@Begin][151]**

**[\\begin][152]**

**[][153]**

**[JR\[LN\]][154]**

****

****@Begin**: //**Revision 1.2.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 4.1.2??? 

Deleted: long since replaced by newer styles of
pseudo-tags.

> See _\\begin_.

****

****\\begin**: //**Revision 2.3.1??? 

Added

Revision 4.1.2??? 

Deleted: folded into front matter

> \[from the LaTeX command\] With \\end, used humorously in writing to
> indicate a context or to remark on the surrounded text. For
> example:
> 
>   
> \\begin{flame}  
> Predicate logic is the only good programming  
> language.  Anyone who would use anything else  
> is an idiot.  Also, all computers should be  
> tredecimal instead of binary.  
> \\end{flame}  
> 
> The Scribe users at CMU and elsewhere used to use @Begin/@End in an
> identical way (LaTeX was built to resemble Scribe). On Usenet, this
> construct would more frequently be rendered as **** and ** OFF\>**, or **\#ifdef FLAME** and
> **\#endif FLAME**. Recently the pseudo-HTML
> form ** ... ** has
> become popular. 

****

******: n.**Revision 3.0.0??? 

Added

Revision 3.2.0??? 

Added

Revision 4.1.2??? 

Deleted: DejaNews suggests it's dead

> \[Usenet: alt.folklore.urban and elsewhere\] Commonly
> used as a placeholder for omitted text in a followup message (not copying
> the whole parent message is considered good form). Refers, of course, to
> the celebrated mutilation of John Bobbitt. 

****

****JR\[LN\]**: /J-R-L/, /J-R-N/, n.**Revision 1.5.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.3.1??? 

Added

Revision 4.1.2??? 

Deleted: PDP-10 reference; no longer
live

> The names JRL and JRN were sometimes used as example names when
> discussing a kind of user ID used under _TOPS-10_ and
> _WAITS_; they were understood to be the initials of
> (fictitious) programmers named \`J. Random Loser' and \`J. Random Nerd' (see
> _J. Random_). For example, if one said "To log
> in, type log one comma jay are en" (that is, "log
> 1,JRN"), the listener would have understood that he should use his
> own computer ID in place of \`JRN'. 

### Deleted before 4.3.0

**[computer geek][155]**

****

****computer geek**: n.**Revision 4.3.0??? 

Deleted: replaced by \`geek'

> 

> 1\. One who eats (computer) bugs for a living. One who fulfills all
> the dreariest negative stereotypes about hackers: an asocial, malodorous,
> pasty-faced monomaniac with all the personality of a cheese grater. Cannot
> be used by outsiders without implied insult to all hackers; compare
> black-on-black vs. white-on-black usage of 'nigger'. A
> computer geek may be either a fundamentally clueless individual or a
> proto-hacker in _larval stage_. Also called turbo nerd, turbo
> geek. See also _propeller head_,
> _clustergeeking_, _geek out_,
> _wannabee_, _terminal junkie_,
> _spod_, _weenie_. 

> 2\. Many self-described computer geeks use this term in a positive
> sense and protest sense 1; this seems to have been a post-1990 development
> which really started to gather steam after 1998\. For one such argument,
> see [http://www.darkwater.com/omni/geek.html][156]. See
> also _geek code_.

### Deleted before 4.3.1

**[Marginal Hacks][157]**

**[block transfer computations][158]**

**[bodysurf code][159]**

**[bot spot][160]**

**[branch to Fishkill][161]**

**[digit][162]**

**[DPB][163]**

**[gaseous][164]**

**[laundromat][165]**

**[Missed'em-five][166]**

**[NetBOLLIX][167]**

**[Pangloss parity][168]**

**[plingnet][169]**

**[pnambic][170]**

**[snivitz][171]**

**[twonkie][172]**

**[whalesong][173]**

**['Snooze][174]**

**[TechRef][175]**

**[TELNET][176]**

**[USG Unix][177]**

**[SysVile][178]**

**[moose call][179]**

**[mouse around][180]**

****

****Marginal Hacks**: n.**Revision 1.5.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.6.1??? 

Added

Revision 4.3.0??? 

Deleted

Revision 4.3.1??? 

Deleted: no longer relevant.

> Margaret Jacks Hall, a building into which the Stanford AI Lab was
> moved near the beginning of the 1980s (from the _D. C. Power
> Lab_).

****

****block transfer computations**: n.**Revision 2.1.1??? 

Added

Revision 4.3.0??? 

Deleted

Revision 4.3.1??? 

Deleted: March 2001 web search ddin't find usage outside of
Dr. Who fandom.

> \[from the television series _Dr. Who_\]
> Computations so fiendishly subtle and complex that they could not be
> performed by machines. Used to refer to any task that should be
> expressible as an algorithm in theory, but isn't. (The Z80's LDIR
> instruction, "Computed Block Transfer with increment", may
> also be relevant.)

****

****bodysurf code**: n.**Revision 3.2.0??? 

Added

Revision 4.3.1??? 

Deleted: March 2001 web search found no evidence of live
usage.

> A program or segment of code written quickly in the heat of
> inspiration without the benefit of formal design or deep thought. Like its
> namesake sport, the result is too often a wipeout that leaves the
> programmer eating sand.

****

****bot spot**: n.**Revision 4.1.1??? 

Added

Revision 4.3.0??? 

Deleted: MUD only.

Revision 4.3.1??? 

Deleted: MUD-specific, not enough
flavor.

> \[MUD\] The user on a MUD with the longest connect time. Derives from
> the fact that _bot_s on MUDs often stay constantly
> connected and appear at the bottom of the list.

****

****branch to Fishkill**: n.**Revision 2.1.1??? 

Added

Revision 4.3.0??? 

Deleted: March 2001 web search found no evidence of live
usage.

Revision 4.3.1??? 

Deleted: no evidence of live usage.

> \[IBM: from the location of one of the corporation's facilities\] Any
> unexpected jump in a program that produces catastrophic or just plain weird
> results. See _jump off into never-never land_,
> _hyperspace_.

****

****digit**: n.,obs.**Revision 2.3.1??? 

Added

Revision 4.3.0??? 

Deleted: DEC is gone

Revision 4.3.1??? 

Deleted: DEC is gone.

> An employee of Digital Equipment Corporation. See also
> _VAX_, _VMS_,
> _PDP-10_, _TOPS-10_,
> _field circus_.

****

****DPB**: /d@-pib'/, vt.**Revision 1.1.0??? 

Added

Revision 4.3.1??? 

Deleted: PDP-10 mnemonic; no longer live

> \[from the PDP-10 instruction set\] To plop something down in the
> middle. Usage: silly. "DPB yourself into that couch there."
> The connotation would be that the couch is full except for one slot just
> big enough for one last person to sit in. DPB means \`DePosit Byte', and
> was the name of a PDP-10 instruction that inserts some bits into the middle
> of some other bits. Hackish usage has been kept alive by the Common LISP
> function of the same name.

****

****gaseous**: adj.**Revision 1.5.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.6.3??? 

Added

Revision 4.3.1??? 

Deleted: long since passed out of live
use

> Deserving of being _gas_sed. Disseminated by
> Geoff Goodfellow while at SRI; became particularly popular after the
> Moscone-Milk killings in San Francisco, when it was learned that the
> defendant Dan White (a politician who had supported Proposition 7) would
> get the gas chamber under Proposition 7 if convicted of first-degree murder
> (he was eventually convicted of manslaughter).

****

****laundromat**: n.**Revision 2.7.1??? 

Added

Revision 4.3.1??? 

Deleted: seems to have passed out of live
use.

> Syn. _disk farm_; see _washing
> machine_.

****

****Missed'em-five**: n.**Revision 2.3.1??? 

Added

Revision 4.3.1??? 

Deleted: obsolete, along with its
referent

> Pejorative hackerism for AT&T System V Unix, generally used by
> _BSD_ partisans in a bigoted mood. (The synonym
> \`SysVile' is also encountered.) See _software bloat_,
> _Berzerkeley_.

****

****NetBOLLIX**: n.**Revision 2.9.10??? 

Added

Revision 4.3.1??? 

Deleted: flame war is long over.

> \[from bollix: to bungle, or British 'bollocks'\]
> _IBM_'s NetBIOS, an extremely
> _brain-damaged_ network protocol that, like
> _Blue Glue_, is used at commercial shops that don't
> know any better.

****

****Pangloss parity**: n.**Revision 3.3.0??? 

Added

Revision 4.3.1??? 

Deleted: no evidence of live use

> \[from Dr. Pangloss, the eternal optimist in Voltaire's
> _Candide_\] In corporate DP shops, a common condition
> of severe but equally shared _lossage_ resulting from
> the theory that as long as everyone in the organization has the exactly the
> _same_ model of obsolete computer, everything will be
> fine.

****

****plingnet**: /pling'net/, n.**Revision 2.2.1??? 

Added

Revision 4.3.1??? 

Deleted: obsolete now that UUCP is gone

> Syn. _UUCPNET_. Also see
> _Commonwealth Hackish_, which uses 'pling'
> for _bang_ (as in _bang
> path_).

****

****pnambic**: /p@-nam'bik/**Revision 2.9.6??? 

Added

Revision 4.3.1??? 

Deleted: no evidence of live usage

> \[Acronym from the scene in the film version of _The Wizard
> of Oz_ in which the true nature of the wizard is first
> discovered: "Pay no attention to the man behind the
> curtain."\]

> A stage of development of a process or function that, owing to
> incomplete implementation or to the complexity of the system, requires
> human interaction to simulate or replace some or all of the actions,
> inputs, or outputs of the process or function. 

> 2\. Of or pertaining to a process or function whose apparent
> operations are wholly or partially falsified.

> 3\. Requiring _prestidigitization_.

> The ultimate pnambic product was "Dan Bricklin's Demo",
> a program which supported flashy user-interface design prototyping. There
> is a related maxim among hackers: "Any sufficiently advanced
> technology is indistinguishable from a rigged demo." See
> _magic_, sense 1, for illumination of this
> point.

****

****snivitz**: /sniv'itz/, n.**Revision 2.4.1??? 

Added

Revision 4.3.1??? 

Deleted: no evidence of live usage

> A hiccup in hardware or software; a small, transient problem of
> unknown origin (less serious than a _snark_). Compare
> _glitch_.

****

****twonkie**: /twon'kee/, n.**Revision 2.3.1??? 

Added

Revision 4.3.1??? 

Deleted: no evidence of live usage

> The software equivalent of a Twinkie (a variety of sugar-loaded junk
> food, or (in gay slang with a small t) the male equivalent of
> 'chick'); a useless 'feature' added to look sexy
> and placate a _marketroid_ (compare
> _Saturday-night special_). The term may also be
> related to _The Twonky_, title menace of a classic SF
> short story by Lewis Padgett (Henry Kuttner and C. L. Moore), first
> published in the September 1942 _Astounding Science
> Fiction_ and subsequently much anthologized.

****

****whalesong**: n.**Revision 2.9.10??? 

Added

Revision 4.3.1??? 

Deleted: obsolete along with PEP modems

> The peculiar clicking and whooshing sounds made by a PEP modem such
> as the Telebit Trailblazer as it tries to synchronize with another PEP
> modem for their special high-speed mode. This sound isn't anything like
> the normal two-tone handshake between conventional V-series modems and is
> instantly recognizable to anyone who has heard it more than once. It
> sounds, in fact, very much like whale songs. This noise is also called
> "the moose call" or "moose tones".

****

****'Snooze**: /snooz/, n.**Revision 2.4.1??? 

Added

Revision 4.3.1??? 

Deleted: FidoNet is no longer
interesting.

> Fidonews, the weekly official on-line newsletter of FidoNet. As the
> editorial policy of Fidonews is "anything that arrives, we
> print", there are often large articles completely unrelated to
> FidoNet, which in turn tend to elicit _flamage_ in
> subsequent issues.

****

****TechRef**: /tek'ref/, n.**Revision 2.4.3??? 

Added

Revision 4.3.1??? 

Deleted: obsolete.

> \[MS-DOS\] The original _IBM PC Technical Reference
> Manual_, including the BIOS listing and complete schematics for
> the PC. The only PC documentation in the original-issue package that was
> considered serious by real hackers.

****

****TELNET**: /tel'net/, vt.**Revision 1.1.0??? 

Added

Revision 1.5.0??? 

Deleted

Revision 2.1.1??? 

Added

Revision 4.3.1??? 

Deleted: techspeak.

> (also commonly lowercased as telnet) To communicate with another Internet
> host using the TELNET (_RFC_ 854) protocol (usually
> using a program of the same name). TOPS-10 people used the word IMPCOM,
> since that was the program name for them. Sometimes abbreviated to TN
> /T-N/. "I usually TN over
> to SAIL just to read the AP News."

****

****USG Unix**: /U-S-G yoo'niks/, n.,obs.**Revision 2.1.1??? 

Added

Revision 4.3.1??? 

Deleted: long obsolete.

> Refers to AT&T Unix commercial versions after _Version
> 7_, especially System III and System V releases 1, 2, and 3\. So
> called because during most of the life­span of those versions
> AT&T's support crew was called the \`Unix Support Group', but it is
> applied to version that pre- and post-dated the USG group but were of the
> same lineage. This term is now historical. See
> _BSD_, _Unix_.

****

****SysVile**: /sis-vi:l'/, n.**Revision 2.9.6??? 

Added

Revision 4.3.1??? 

Deleted: old flamewar, no longer
interesting.

> See _Missed'em-five_.

****

****moose call**: n.**Revision 2.9.10??? 

Added

Revision 4.3.1??? 

Deleted: goes with 'whalesong'

> See _whalesong_.

****

****mouse around**: vi.**Revision 2.1.1??? 

Added

Revision 4.3.1??? 

Deleted: seems to have been ephemeral, no evidence of live
use.

> To explore public portions of a large system, esp.: a network such
> as Internet via _FTP_ or telnet, looking for
> interesting stuff to _snarf_.

### Deleted before 4.3.2

**[120 reset][181]**

**[Black Thursday][182]**

**[POPJ][183]**

**[Internet address][184]**

**[wallpaper][185]**

**[interrupt list][186]**

**[bum][187]**

****

****120 reset**: /wuhn-twen'tee ree'set/, n.**Revision 2.4.1??? 

Added

Revision 4.3.1??? 

Deleted

Revision 4.3.2??? 

Deleted: general to engineers.

> \[from 120 volts, U.S. wall voltage\] To cycle power on a machine in
> order to reset or unjam it. Compare _Big Red Switch_,
> _power cycle_.

****

****Black Thursday**: n.**Revision 3.3.2??? 

Added

Revision 4.3.2??? 

Deleted: passed out of use after CDA
repeal

> February 8th, 1996 -- the day of the signing into law of the
> _CDA_, so called by analogy with the catastrophic
> "Black Friday" in 1929 that began the Great Depression.

****

****POPJ**: /pop'J/, n.,v.**Revision 1.5.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.8.1??? 

Added

Revision 4.3.2??? 

Deleted: PDP-10 is long dead.

> \[from a _PDP-10_ return-from-subroutine
> instruction\] To return from a digression. By verb doubling, "Popj,
> popj" means roughly "Now let's see, where were we?" See
> _RTI_.

****

****Internet address**: n.**Revision 2.1.1??? 

Added

Revision 4.3.2??? 

Deleted: now too well known to need
rehearsing

> 1\. \[techspeak\] An absolute network address of the form foo@bar.baz, where foo is a user name, bar is
> a _sitename_, and baz is a domain name, possibly including periods itself.
> Contrast with _bang path_; see also _the
> network_ and _network address_. All
> Internet machines and most UUCP sites can now resolve these addresses,
> thanks to a large amount of behind-the-scenes magic and
> _PD_ software written since 1980 or so. See also
> _bang path_, _domainist_.

> 2\. More loosely, any network address reachable through Internet;
> this includes _bang path_ addresses and some internal
> corporate and government networks.
> 
> Reading Internet addresses is something of an art. Here are the four
> most important top-level functional Internet domains followed by a
> selection of geographical domains:
> 
> > comcommercial organizations
> > 
> > edueducational institutions
> > 
> > govU.S. government civilian sites
> > 
> > milU.S. military sites
> > 
> > 
> 
> Note that most of the sites in the com
> and edu domains are in the U.S. or
> Canada.
> 
> > ussites in the U.S. outside the functional domains
> > 
> > susites in the ex-Soviet Union (see _kremvax_).
> > 
> > uksites in the United Kingdom
> > 
> > 
> 
> Within the us domain, there
> are subdomains for the fifty states, each generally with a name identical
> to the state's postal abbreviation. Within the uk domain, there is an ac subdomain for academic sites and a
> co domain for commercial ones.
> Other top-level domains may be divided up in similar ways.

****

****wallpaper**: n.**Revision 1.1.0??? 

Added

Revision 4.3.2??? 

Deleted: long obsolete and out of use

> 1\. A file containing a listing (e.g., assembly listing) or a
> transcript, esp.: a file containing a transcript of all or part of a login
> session. (The idea was that the paper for such listings was essentially
> good only for wallpaper, as evidenced at Stanford, where it was used to
> cover windows.) Now rare, esp.: since other systems have developed other
> terms for it (e.g., PHOTO on TWENEX). However, the Unix world doesn't have
> an equivalent term, so perhaps _wallpaper_ will take
> hold there. The term probably originated on ITS, where the commands to
> begin and end transcript files were **:WALBEG**
> and **:WALEND**, with default file **WALL PAPER** (the space was a path delimiter).

> 2\. The background pattern used on graphical workstations (this is
> techspeak under the 'Windows' graphical user interface to
> MS-DOS). 

> 3\. wallpaper file n. The file that contains the wallpaper
> information before it is actually printed on paper. (Even if you don't
> intend ever to produce a real paper copy of the file, it is still called a
> wallpaper file.)

****

****interrupt list**: n.**Revision 2.4.1??? 

Added

Revision 4.3.2??? 

Deleted: obsolete along with MS-DOS

> \[MS-DOS\] The list of all known software interrupt calls (both
> documented and undocumented) for IBM PCs and compatibles, maintained and
> made available for free redistribution by Ralf Brown
> @email{}. As of late 1992, it had grown to
> approximately two megabytes in length.

****

****bum****Revision 1.1.0??? 

Added

Revision 4.3.2??? 

Deleted: It's 2002 and this is thoroughly
obsolete

> 1\. vt. To make highly efficient,
> either in time or space, often at the expense of clarity. "I managed
> to bum three more instructions out of that code." "I spent
> half the night bumming the interrupt code." In 1996, this term and
> the practice it describes are semi-obsolete. In _elder
> days_, John McCarthy (inventor of _LISP_)
> used to compare some efficiency-obsessed hackers among his students to
> "ski bums"; thus, optimization became "program
> bumming", and eventually just "bumming". 2\. To squeeze
> out excess; to remove something in order to improve whatever it was removed
> from (without changing function; this distinguishes the process from a
> _featurectomy_). 3\. n. A small change to an algorithm, program, or
> hardware device to make it more efficient. "This hardware bum makes
> the jump instruction faster." Usage: now uncommon, largely
> superseded by v.
> _tune_ (and n.
> _tweak_, _hack_), though none of
> these exactly capture sense 

> 2\. All these uses are rare in Commonwealth hackish, because in the
> parent dialects of English the noun 'bum' is a rude synonym for
> 'buttocks' and the verb 'bum' for buggery.

### Deleted before 4.3.3

**[all-elbows][188]**

****

****all-elbows**: adj.**Revision 2.4.3??? 

Added

Revision 4.3.3??? 

Deleted: as dead as MS/DOS

> \[MS-DOS\] Of a TSR (terminate-and-stay-resident) IBM PC program, such
> as the N pop-up calendar and calculator
> utilities that circulate on _BBS_ systems: unsociable.
> Used to describe a program that rudely steals the resources that it needs
> without considering that other TSRs may also be resident. One particularly
> common form of rudeness is lock-up due to programs fighting over the
> keyboard interrupt. See _rude_, also
> _mess-dos_.

### Deleted before 4.4.0

**[PPN][189]**

**[gurfle][190]**

**[cycle drought][191]**

**[dup loop][192]**

**[Nominal Semidestructor][193]**

**[acolyte][194]**

**[Ada][195]**

**[AIDS][196]**

**[AIDX][197]**

**[amoeba][198]**

**[ANSI][199]**

**[backspace and overstrike][200]**

**[banana label][201]**

**[baud barf][202]**

**[berklix][203]**

**[BITNET][204]**

**[bixen][205]**

**[blink][206]**

**[buglix][207]**

**[can][208]**

**[card walloper][209]**

**[corge][210]**

**[cray instability][211]**

**[crayola][212]**

**[crayon][213]**

**[cubing][214]**

**[cycle crunch][215]**

**[D. C. Power Lab][216]**

**[dead link][217]**

**[cray][218]**

**[domainist][219]**

**[donuts][220]**

**[dup killer][221]**

**[earthquake][222]**

**[farming][223]**

**[Fight-o-net][224]**

**[File Attach][225]**

**[File Request][226]**

**[firmy][227]**

**[FTP][228]**

**[FUD wars][229]**

**[fuzzball][230]**

**[gabriel][231]**

**[gripenet][232]**

**[gun][233]**

**[Gosperism][234]**

**[grault][235]**

**[haque][236]**

**[hobbit][237]**

**[humma][238]**

**[IBM discount][239]**

**[inc][240]**

**[jolix][241]**

**[lace card][242]**

**[lasherism][243]**

**[LDB][244]**

**[macrotape][245]**

**[microfloppies][246]**

**[minifloppies][247]**

**[GFR][248]**

**[multician][249]**

**[netrock][250]**

**[nroff][251]**

**[round tape][252]**

**[Telerat][253]**

**[ventilator card][254]**

**[PC-ism][255]**

**[Helen Keller mode][256]**

**[node][257]**

**[OSU][258]**

**[P-mail][259]**

**[square tape][260]**

**[PETSCII][261]**

**[rib site][262]**

**[rice box][263]**

**[rusty memory][264]**

**[ScumOS][265]**

**[sidecar][266]**

**[tall card][267]**

**[terpri][268]**

**[UUCPNET][269]**

**[VAXectomy][270]**

**[vaxherd][271]**

**[vaxism][272]**

**[W2K bug][273]**

**[woofer][274]**

**[Yellow Book][275]**

**[slap on the side][276]**

**[tweeter][277]**

**[SOS][278]**

**[stiffy][279]**

**[short card][280]**

**[Silver Book][281]**

**[Devil Book][282]**

**[crayola books][283]**

**[4.2][284]**

**[AI koans][285]**

**[Big Gray Wall][286]**

**[Blue Book][287]**

**[Green Book][288]**

**[Red Book][289]**

**[White Book][290]**

**[BQS][291]**

**[brochureware][292]**

**[desk check][293]**

**[echo][294]**

**[fd leak][295]**

**[g-file][296]**

**[gag][297]**

**[machinable][298]**

**[lexiphage][299]**

**[line starve][300]**

**[LPT][301]**

**[PDL][302]**

**[overflow pdl][303]**

**[pod][304]**

****

****PPN**: /pip'n/**Revision 1.1.0??? 

Added

Revision 4.4.0??? 

Deleted: as dead as TOPS-10\.

> 1\. A combination of a "project identifier" and
> "programmer name", used to identify a specific file directory
> belonging to that programmer. This was used in the TOPS-10 operating
> system that _DEC_ provided for the PDP-10\. The
> implicit assumption is that there will be many projects, each with several
> programmers working on it, and that a programmer may work on several
> projects. This is not a bad organization; what was totally
> _bogus_ is that projects and programmers were
> identified by octal (base eight) numbers! Hence the term
> Project-Programmer Number, or PPN. If you were programmer 72534 and wanted
> to work on project 306, you would have had to tell the computer
> "login 306,72534". This was absurd. At CMU the TOPS-10
> system was modified to be somewhat less ridiculous: projects were
> identified by a letter and three decimal (not octal) digits, and
> programmers were identified by his two initials, a digit indicating the
> first year he came to CMU, and a fourth character that is used to
> distinguish between, say, Fred Loser and Farley Luser who both happened to
> arrive the same year. So to use the PDP-10 at CMU one might have said
> "login A780GS70". The programmer name "GS70" was
> also called a "man number" at CMU, even though it isn't really
> a number. At Stanford, projects and programmers were identified by three
> letters or digits each: if Guy Steele werre to work on a LISP project at
> Stanford, he might log in as "login lsp,gls". This was much
> more mnemonic. Programmer identifiers at Stanford were usually the
> programmer's initials, though sometimes it is a nickname or other
> three-letter sequence. Even though the CMU and Stanford forms were not
> really (pairs of) numbers, the term PPN was used to refer to the
> combination.

> 2\. At Stanford, the term PPN was often used loosely to refer to the
> programmer name alone. "I want to send you some mail; what's your
> ppn?." This term is still used by old-timers on the commercial
> time-sharing service CompuServe (which uses PDP-10s) but has long since
> vanished from hackerdom. ITS and UNIX, of course, never used PPNs; ITS had
> six-character UNAMEs, and UNIX has 8 or 15-character \`usernames' and a
> hierarchical file system rather than project areas.

****

****gurfle**: /ger'fl/, interj.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: no evidence of live usage on
Google

> An expression of shocked disbelief. "He said we have to
> recode this thing in FORTRAN by next week. Gurfle!" Compare
> _weeble_.

****

****cycle drought**: n.**Revision 1.5.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: obsolete along with
time-sharing

> A scarcity of cycles. It may be due to a _cycle
> crunch_, but it could also occur because part of the computer is
> temporarily not working, leaving fewer cycles to go around. "The
> _high moby_ is _down_, so we're
> running with only half the usual amount of memory. There will be a cycle
> drought until it's fixed."

****

****dup loop**: /d\[y\]oop loop/, dupe loop, n.**Revision 2.4.1??? 

Added

Revision 4.4.0??? 

Deleted: long obsolete even on FidoNet

> \[FidoNet\] An infinite stream of duplicated, near-identical messages
> on a FidoNet _echo_, the only difference being unique
> or mangled identification information applied by a faulty or incorrectly
> configured system or network gateway, thus rendering _dup
> killer_s ineffective. If such a duplicate message eventually
> reaches a system through which it has already passed (with the original
> identification information), all systems passed on the way back to that
> system are said to be involved in a _dup loop_.

****

****Nominal Semidestructor**: n.**Revision 2.9.9??? 

Added

Revision 3.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: old flamewar, no longer
interesting.

> Soundalike slang for 'National Semiconductor', found
> among other places in the Networking/2 networking sources. During the late
> 1970s to mid-1980s this company marketed a series of microprocessors
> including the NS16000 and NS32000 and several variants. At one point early
> in the great microprocessor race, the specs on these chips made them look
> like serious competition for the rising Intel 80x86 and Motorola 680x0
> series. Unfortunately, the actual parts were notoriously flaky and never
> implemented the full instruction set promised in their literature,
> apparently because the company couldn't get any of the mask steppings to
> work as designed. They eventually sank without trace, joining the Zilog
> Z8000 and a few even more obscure also-rans in the graveyard of forgotten
> microprocessors. Compare _HP-SUX_,
> _AIDX_, _buglix_,
> _Macintrash_, _Telerat_,
> _ScumOS_, _sun-stools_,
> _Slowlaris_, _Internet
> Exploder_.

****

****acolyte**: n. obs.**Revision 3.1.0??? 

Added

Revision 4.4.0??? 

Deleted: stone-dead along with glass-walled machine
rooms.

> \[TMRC\] An _OSU_ privileged enough to submit
> data and programs to a member of the
> _priesthood_.

****

****Ada**: n.**Revision 2.5.1??? 

Added

Revision 4.2.2??? 

Changed

Revision 4.3.2??? 

Changed

Revision 4.4.0??? 

Deleted: Ada is so dead in 2002\. No point in fighting old
wars.

> A _Pascal_-descended language that was at one
> time made mandatory for Department of Defense software projects by the
> Pentagon. Hackers are nearly unanimous in observing that, technically, it
> is precisely what one might expect given that kind of endorsement by fiat;
> bloated, crockish, difficult to use, and overall a disastrous,
> multi-billion-dollar boondoggle (one common description was "The PL/I
> of the 1980s"). The kindest thing that has been said about it is
> that there is probably a good small language screaming to get out from
> inside its vast, _elephantine_ bulk.
> 
> ![](http://www.catb.org/jargon/graphics/fortran.png)
> 
> Nowadays we say this of Ada.

****

****AIDS**: /aydz/, n.**Revision 2.4.1??? 

Added

Revision 4.4.0??? 

Deleted: this slang is as dead as the floppy
disk.

> Short for A\* Infected Disk Syndrome (\`A\*' is a
> _glob_ pattern that matches, but is not limited to,
> Apple or Amiga), this condition is quite often the result of practicing
> unsafe _SEX_. See _virus_,
> _worm_, _Trojan horse_,
> _virgin_.

****

****AIDX**: /ayd'k@z/, n.**Revision 2.9.9??? 

Added

Revision 2.9.10??? 

Added

Revision 3.0.0??? 

Changed

Revision 4.4.0??? 

Deleted: Yet another remnant from a decade-old flamewar.
Linux won.

> Derogatory term for IBM's perverted version of Unix, AIX, especially
> for the AIX 3.? used in the IBM RS/6000 series (some hackers think it is
> funnier just to pronounce "AIX" as "aches"). A
> victim of the dreaded "hybridism" disease, this attempt to
> combine the two main currents of the Unix stream
> (_BSD_ and USG Unix) became a
> _monstrosity_ to haunt system administrators' dreams.
> For example, if new accounts are created while many users are logged on,
> the load average jumps quickly over 20 due to silly implementation of the
> user databases. For a quite similar disease, compare
> _HP-SUX_. Also, compare
> _Macintrash_, _ScumOS_,
> _sun-stools_.

****

****amoeba**: n.**Revision 2.3.1??? 

Added

Revision 4.4.0??? 

Deleted: no evidence of live use on the Web in in
2002\.

> Humorous term for the Commodore Amiga personal computer.

****

****ANSI**: /an'see/**Revision 3.2.0??? 

Added

Revision 3.3.1??? 

Changed

Revision 4.4.0??? 

Deleted: dead along with green-screen
terminals.

> 1\. n. \[techspeak\] The American
> National Standards Institute. ANSI, along with the International
> Organization for Standards (ISO), standardized the C programming language
> (see _K&R_, _Classic C_), and
> promulgates many other important software standards. 

> 2\. n. \[techspeak\] A terminal may
> be said to be \`ANSI' if it meets the ANSI X3.64 standard for terminal
> control. Unfortunately, this standard was both over-complicated and too
> permissive. It has been retired and replaced by the ECMA-48 standard,
> which shares both flaws. 

> 3\. n. \[BBS jargon\] The set of
> screen-painting codes that most MS-DOS/Windows and Amiga computers accept.
> This comes from the ANSI.SYS device driver that had to be loaded on an
> MS-DOS computer to view such codes. Unfortunately, neither DOS ANSI nor
> the BBS ANSIs derived from it exactly match the ANSI X3.64 terminal
> standard. For example, the ESC-\[1m code turns on the bold highlight on
> large machines, but in IBM PC/MS-DOS ANSI, it turns on \`intense' (bright)
> colors. Also, in BBS-land, the term \`ANSI' is often used to imply that a
> particular computer uses or can emulate the IBM high-half character set
> from MS-DOS/Windows. Particular use depends on context. Occasionally, the
> vanilla ASCII character set is used with the color codes, but on BBSs, ANSI
> and \`IBM characters' tend to go together.

****

****backspace and overstrike**: interj.**Revision 2.4.3??? 

Added

Revision 4.1.1??? 

Changed

Revision 4.4.0??? 

Deleted: as dead as printing terminals.

> \[rare\] Whoa! Back up. Used to suggest that someone just said or
> did something wrong. Once common among APL programmers; may now be
> obsolete.

****

****banana label**: n.**Revision 2.4.3??? 

Added

Revision 4.4.0??? 

Deleted: macrotape drives are museum pieces
now.

> The labels often used on the sides of
> _macrotape_ reels, so called because they are shaped
> roughly like blunt-ended bananas. This term, like macrotapes themselves,
> is still current but visibly headed for obsolescence.

****

****baud barf**: /bawd barf/, n.**Revision 2.1.1??? 

Added

Revision 4.2.0??? 

Changed

Revision 4.4.0??? 

Deleted: Who uses serial terminals with modems any
more?

> The garbage one gets on a terminal (or terminal emulator) when using
> a modem connection with some protocol setting (esp.: line speed) incorrect,
> or when someone picks up a voice extension on the same line, or when really
> bad line noise disrupts the connection. Baud barf is not completely
> _random_, by the way; hackers with a lot of
> serial-line experience can usually tell whether the device at the other end
> is expecting a higher or lower speed than the terminal is set to.
> _Really_ experienced ones can identify particular
> speeds.

****

****berklix**: /berk'liks/, n.,adj.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: Dead along with the UC Berkeley releases.
Everybody says BSD now.

> \[contraction of \`Berkeley Unix'\] See _BSD_.
> Not used at Berkeley itself. May be more common among
> _suit_s attempting to sound like cognoscenti than
> among hackers, who usually just say \`BSD'.

****

****BITNET**: /bit'net/, n., obs.**Revision 2.8.1??? 

Added

Revision 4.1.0??? 

Changed

Revision 4.1.1??? 

Changed

Revision 4.4.0??? 

Deleted: Long dead at this point.

> \[acronym: Because It's Time NETwork\] Everybody's least favorite
> piece of the network (see _the network_) -- until AOL
> happened. The BITNET hosts were a collection of IBM dinosaurs and VAXen
> (the latter with lobotomized comm hardware) that communicated using
> 80-character _EBCDIC_ card images (see
> _eighty-column mind_); thus, they tended to mangle the
> headers and text of third-party traffic from the rest of the
> ASCII/_RFC_-822 world with annoying regularity.
> BITNET was also notorious as the apparent home of
> _B1FF_. By 1995 it had, much to everyone's relief,
> been obsolesced and absorbed into the Internet. Unfortunately, around this
> time we also got AOL.

****

****bixen**: pl.n.**Revision 4.1.1??? 

Added

Revision 4.4.0??? 

Deleted: BIX is dead

> Users of BIX (the BIX Information eXchange, formerly the Byte
> Information eXchange). Parallels other plurals like boxen,
> _VAXen_, oxen.

****

****blink**: vi.,n.**Revision 3.1.0??? 

Added

Revision 4.1.2??? 

Changed

Revision 4.2.2??? 

Changed

Revision 4.4.0??? 

Deleted: Killed by Internet access

> To use a navigator or off-line message reader to minimize time spent
> on-line to a commercial network service (a necessity in many places outside
> the U.S. where the telecoms monopolies charge per-minute for local calls).
> This term attained wide use in the UK, but is rare or unknown in the
> US.

****

****buglix**: /buhg'liks/, n.**Revision 2.5.1??? 

Added

Revision 4.4.0??? 

Deleted: Ultrix is dead.

> \[uncommon\] Pejorative term referring to _DEC_'s
> ULTRIX operating system in its earlier _severely_ buggy
> versions. Still used to describe ULTRIX, but without nearly so much venom.
> Compare _AIDX_, _HP-SUX_,
> _Telerat_, _sun-stools_.

****

****can**: vt.**Revision 2.1.1??? 

Added

Revision 2.9.12??? 

Changed

Revision 4.2.3??? 

Changed

Revision 4.4.0??? 

Deleted: Dead along with timesharing.

> To abort a job on a time-sharing system. Used esp.: when the person
> doing the deed is an operator, as in "canned from the
> _console_". Frequently used in an imperative
> sense, as in "Can that print job, the LPT just popped a
> sprocket!" Synonymous with _gun_. It is said
> that the ASCII character with mnemonic CAN (0011000) was used as a kill-job
> character on some early OSes, but this is more likely to be short for
> cancel. Alternatively, this term may
> derive from mainstream slang 'canned' for being laid off or
> fired.

****

****card walloper**: n.**Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: obsolete along with punched
cards.

> An EDP programmer who grinds out batch programs that do stupid
> things like print people's paychecks. Compare _code
> grinder_. See also _punched card_,
> _eighty-column mind_.

****

****corge**: /korj/, n.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: no evidence of live use in
2002\.

> \[originally, the name of a cat\] Yet another _metasyntactic
> variable_, invented by Mike Gallaher and propagated by the
> _GOSMACS_ documentation. See
> _grault_.

****

****cray instability**: n.**Revision 2.3.1??? 

Added

Revision 3.2.0??? 

Changed

Revision 4.4.0??? 

Deleted: Cray is dead and there is no evidence of live use
on the Web.

> 1\. A shortcoming of a program or algorithm that manifests itself
> only when a large problem is being run on a powerful machine (see
> _cray_). Generally more subtle than bugs that can be
> detected in smaller problems running on a workstation or mini. 

> 2\. More specifically, a shortcoming of algorithms which are well
> behaved when run on gentle floating point hardware (such as IEEE-standard
> or PDP-series machines) but which break down badly when exposed to a Cray's
> unique \`rounding' rules.

****

****crayola**: /kray-oh'l@/, n.**Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: Cray is dead and there is no evidence of live use
on the Web.

> A super-mini or -micro computer that provides some reasonable
> percentage of supercomputer performance for an unreasonably low price.
> Might also be a _killer micro_.

****

****crayon**: n.**Revision 2.1.1??? 

Added

Revision 4.1.3??? 

Changed

Revision 4.2.3??? 

Changed

Revision 4.4.0??? 

Deleted: Cray is dead and there is no evidence of live use
on the Web.

> 1\. Someone who works on Cray supercomputers. More specifically, it
> implies a programmer, probably of the CDC ilk, probably male, and almost
> certainly wearing a tie (irrespective of gender). Systems types who have a
> Unix background tend not to be described as crayons. 

> 2\. Formerly, anyone who worked for Cray Research; since the buyout
> by SGI, anyone they inherited from Cray. Nowadays, often applied to any SGI
> employee who either works at one of the former Cray Research facilities
> (i.e. Eagan Minnesota and Chippewa Falls Wisconsin) or works primarily in
> vector computing aspects of the business. Sometimes considered mildly
> offensive by those to whom it is applied, particularly those whose work has
> nothing to do with vector computing. 

> 3\. A _computron_ (sense 2) that participates
> only in _number-crunching_. 

> 4\. A unit of computational power equal to that of a single Cray-1\.
> There is a standard joke about this usage that derives from an old Crayola
> crayon promotional gimmick: When you buy 64 crayons you get a free
> sharpener.

****

****cubing**: vi.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use on the Web,
2002\.

> \[parallel with 'tubing'\] 

> 1\. Hacking on an IPSC (Intel Personal SuperComputer) hypercube.
> "Louella's gone cubing _again_!!" 

> 2\. Hacking Rubik's Cube or related puzzles, either physically or
> mathematically. 

> 3\. An indescribable form of self-torture (see sense 1 or 2).

****

****cycle crunch**: n.,obs.**Revision 1.5.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.2.1??? 

Added

Revision 4.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: Nobody time-shares anymore. Even PCs don't get
this loaded.

> A situation wherein the number of people trying to use a computer
> simultaneously has reached the point where no one can get enough cycles
> because they are spread too thin and the system has probably begun to
> _thrash_. This scenario is an inevitable result of
> Parkinson's Law applied to timesharing. Usually the only solution is to
> buy more computer. Happily, this has rapidly become easier since the
> mid-1980s, so much so that the very term \`cycle crunch' now has a faintly
> archaic flavor; most hackers now use workstations or personal computers as
> opposed to traditional timesharing systems, and are far more likely to
> complain of \`bandwidth crunch' on their shared networks rather than cycle
> crunch.

****

****D. C. Power Lab**: n.**Revision 2.6.1??? 

Added

Revision 2.7.1??? 

Renamed: 'DC Power Lab' -\> 'D. C. Power Lab' (deduced from
diffs)

Revision 4.4.0??? 

Deleted: It's gone.

> The former site of _SAIL_. Hackers thought
> this was very funny because the obvious connection to electrical
> engineering was nonexistent --- the lab was named for a Donald
> C. Power.

****

****dead link**: n.**Revision 3.3.0??? 

Added

Revision 4.4.0??? 

Deleted: This is so mainstream now.

> \[very common\] A World-Wide-Web URL that no longer points to the
> information it was written to reach. Usually this happens because the
> document has been moved or deleted. Lots of dead links make a WWW page
> frustrating and useless and are the \#1 sign of poor page
> maintainance. Compare _dangling pointer_,
> _link rot_.

****

****cray**: /kray/, n.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: Cray is long gone.

> 1\. (properly, capitalized) One of the line of supercomputers
> designed by Cray Research. 

> 2\. Any supercomputer at all. 

> 3\. The _canonical_
> _number-crunching_ machine.

> The term is actually the lowercased last name of Seymour Cray, a
> noted computer architect and co-founder of the company. Numerous vivid
> legends surround him, some true and some admittedly invented by Cray
> Research brass to shape their corporate culture and image.

****

****domainist**: /doh-mayn'ist/, adj.**Revision 2.4.3??? 

Added

Revision 3.3.0??? 

Changed

Revision 3.3.2??? 

Changed

Revision 4.4.0??? 

Deleted: Obsolete. The Great Internet Explosion did it
in.

> 1\. \[Usenet, by pointed analogy with "sexist",
> "racist", etc.\] Someone who judges people by the domain of
> their email addresses; esp. someone who dismisses anyone who posts from a
> public internet provider. "What do you expect from an article posted
> from aol.com?" 

> 2\. Said of an Internet address (as opposed to a _bang
> path_) because the part to the right of the @
> specifies a nested series of domains;
> for example, @email{esr@snark.thyrsus.com} specifies the machine called
> snark in the subdomain called
> thyrsus within the top-level
> domain called com. See also
> _big-endian_, sense 2\.

> The meaning of this term has drifted. At one time sense 2 was
> primary. In elder days it was also used of a site, mailer, or routing
> program which knew how to handle domainist addresses; or of a person (esp.:
> a site admin) who preferred domain addressing, supported a domainist
> mailer, or proselytized for domainist addressing and disdained
> _bang path_s. These senses are now (1996) obsolete,
> as effectively all sites have converted.

****

****donuts**: n**Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use on the
net.

> \[obs.\] A collective noun for any set of memory bits. This usage is
> extremely archaic and may no longer be live jargon; it dates from the days
> of ferrite-_core_ memories in which each bit was
> implemented by a doughnut-shaped magnetic flip-flop.

****

****dup killer**: /d\[y\]oop kill'r/, n.**Revision 2.4.1??? 

Added

Revision 4.4.0??? 

Deleted: FidoNet is no longer
interesting.

> \[FidoNet\] Software that is supposed to detect and delete duplicates
> of a message that may have reached the FidoNet system via different
> routes.

****

****earthquake**: n.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: Over a decade old...

> \[IBM\] The ultimate real-world shock test for computer hardware.
> Hackish sources at IBM deny the rumor that the Bay Area quake of 1989 was
> initiated by the company to test quality-assurance procedures at its
> California plants.

****

****farming**: n.**Revision 2.3.1??? 

Added

Revision 4.1.0??? 

Changed

Revision 4.3.2??? 

Changed

Revision 4.4.0??? 

Deleted: This failure mode is no longer.

> \[Adelaide University, Australia\] What the heads of a disk drive are
> said to do when they plow little furrows in the magnetic media. Associated
> with a _crash_. Typically used as follows: "Oh
> no, the machine has just crashed; I hope the hard drive hasn't gone
> _farming_ again." Now rare; modern drives
> automatically park their heads in a safe zone on power-down, so it takes a
> real mechanical problem to induce this.

****

****Fight-o-net**: n.**Revision 2.4.1??? 

Added

Revision 4.4.0??? 

Deleted: FidoNet is no longer
interesting.

> \[FidoNet\] Deliberate distortion of _FidoNet_,
> often applied after a flurry of _flamage_ in a
> particular _echo_, especially the SYSOP echo or
> Fidonews.

****

****File Attach**: **Revision 2.4.1??? 

Added

Revision 4.4.0??? 

Deleted: FidoNet is history

> 1\. n. A file sent along with a
> mail message from one FidoNet to another. 

> 2\. vt. Sending someone a file by
> using the File Attach option in a FidoNet mailer.

****

****File Request****Revision 2.4.1??? 

Added

Revision 4.4.0??? 

Deleted: FidoNet is no longer
interesting.

> \[FidoNet\]

> 1\. n. The
> _FidoNet_ equivalent of _FTP_, in
> which one FidoNet system automatically dials another and
> _snarf_s one or more files. Often abbreviated
> FReq; files are often announced as
> being "available for FReq" in the same way that files are
> announced as being "available for/by anonymous FTP" on the
> Internet. 

> 2\. vt. The act of getting a copy
> of a file by using the File Request option of the FidoNet mailer.

****

****firmy**: /fer'mee/, n.**Revision 2.9.6??? 

Added

Revision 4.4.0??? 

Deleted: All floppies are now firmies; this has passed out
of use.

> Syn. _stiffy_ (a 3.5-inch floppy disk).

****

****FTP**: /F-T-P/, _not_, /fit'ip/**Revision 1.1.0??? 

Added

Revision 4.4.0??? 

Deleted: Generic sense of FTP is dying along with the
protocol.

> 1\. \[techspeak\] n. The File
> Transfer Protocol for transmitting files between systems on the Internet.
> 

> 2\. vt. To
> _beam_ a file using the File Transfer Protocol.
> 

> 3\. Sometimes used as a generic even for file transfers not using
> _FTP_. "Lemme get a copy of
> _Wuthering Heights_ ftp'd from uunet."

****

****FUD wars**: /fuhd worz/, n.**Revision 2.1.1??? 

Added

Revision 4.1.0??? 

Changed

Revision 4.4.0??? 

Changed: added new primary sense

Revision 4.4.0??? 

Deleted: The FUD wars are over, though FUD remains. (The
old-time standards wars have been replaced by closed vs, open source.)

> \[from _FUD_\] Political posturing engaged in by
> hardware and software vendors ostensibly committed to standardization but
> actually willing to fragment the market to protect their own shares. The
> Unix International vs.: OSF conflict about Unix standards was one
> outstanding example; Microsoft vs. Netscape vs. W3C about HTML standards is
> another.

****

****fuzzball**: n.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: Long gone and dead.

> \[TCP/IP hackers\] A DEC LSI-11 running a particular suite of
> homebrewed software written by Dave Mills and assorted co-conspirators,
> used in the early 1980s for Internet protocol testbedding and
> experimentation. These were used as NSFnet backbone sites in its early
> 56kb-line days; a few were still active on the Internet as late as
> mid-1993, doing odd jobs such as network time service.

****

****gabriel**: /gay'bree-@l/, n.**Revision 1.1.0??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use.

> \[for Dick Gabriel, SAIL LISP hacker and volleyball fanatic\] An
> unnecessary (in the opinion of the opponent) stalling tactic, e.g., tying
> one's shoelaces or combing one's hair repeatedly, asking the time, etc.
> Also used to refer to the perpetrator of such tactics. Also, pulling a Gabriel, Gabriel mode.

****

****gripenet**: n.**Revision 2.9.10??? 

Added

Revision 4.4.0??? 

Deleted: They've gone Internet, like everybody
else.

> \[IBM\] A wry (and thoroughly unofficial) name for IBM's internal VNET
> system, deriving from its common use by IBMers to voice pointed criticism
> of IBM management that would be taboo in more formal channels.

****

****gun**: vt.**Revision 1.2.0??? 

Added

Revision 4.4.0??? 

Deleted: A decade obsolete along with the rest of the ITS
slang.

> \[ITS, now rare: from the **:GUN**
> command\] To forcibly terminate a program or job (computer, not career).
> "Some idiot left a background process running soaking up half the
> cycles, so I gunned it." Compare _can_,
> _blammo_.

****

****Gosperism**: /gos'p@r-izm/, n.**Revision 1.5.0??? 

Added

Revision 2.1.1??? 

Deleted

Revision 2.2.1??? 

Added

Revision 4.1.1??? 

Changed

Revision 4.4.0??? 

Deleted: No evidence of live usage.

> A hack, invention, or saying due to _elder
> days_ arch-hacker R. William (Bill) Gosper. This notion merits
> its own term because there are so many of them. Many of the entries in
> _HAKMEM_ are Gosperisms; see also
> _life_.

****

****grault**: /grawlt/, n.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use.

> Yet another _metasyntactic variable_, invented
> by Mike Gallaher and propagated by the _GOSMACS_
> documentation. See _corge_.

****

****haque**: /hak/, n.**Revision 2.9.9??? 

Added

Revision 2.9.10??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use.

> \[Usenet\] Variant spelling of _hack_, used only
> for the noun form and connoting an _elegant_ hack,
> that is a _hack_ in sense 2\.

****

****hobbit**: n.**Revision 2.5.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence that sense 1 is still in live
use.

> 1\. \[rare\] The High Order BIT of a byte; same as the _meta
> bit_ or _high bit_. 

> 2\. The non-ITS name of @email{vad@ai.mit.edu} (\*Hobbit\*), master of
> lasers.

****

****humma**: //, excl.**Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use.

> A filler word used on various chat and talk programs when you had nothing to say but
> felt that it was important to say something. The word apparently
> originated (at least with this definition) on the MECC Timeshare System
> (MTS, a now-defunct educational time-sharing system running in Minnesota
> during the 1970s and the early 1980s) but was later sighted on early Unix
> systems. Compare the U.K's _wibble_.

****

****IBM discount**: n.**Revision 2.5.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use.

> A price increase. Outside IBM, this derives from the common
> perception that IBM products are generally overpriced (see
> _clone_); inside, it is said to spring from a belief
> that large numbers of IBM employees living in an area cause prices to
> rise.

****

****inc**: /ink/, v.**Revision 2.9.12??? 

Added

Revision 4.4.0??? 

Deleted: Gone along with assembler
programming

> Verbal (and only rarely written) shorthand for increment, i.e. 'increase by one'.
> Especially used by assembly programmers, as many assembly languages have an
> **inc** mnemonic. Antonym: dec (see
> _DEC_).

****

****jolix**: /joh'liks/, n.,adj.**Revision 2.9.10??? 

Added

Revision 3.3.2??? 

Changed

Revision 4.2.0??? 

Changed

Revision 4.4.0??? 

Deleted: No evidence of live use.

> 386BSD, the freeware port of the BSD Net/2 release to the Intel i386
> architecture by Bill Jolitz, Lynne Greer Jolitz, and friends. Used to
> differentiate from BSDI's port based on the same source tape, which used to
> be called BSD/386 and is now BSD/OS. See
> _BSD_.

****

****lace card**: n. obs.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: Dead along with punched cards.

> A _punched card_ with all holes punched (also
> called a whoopee card or ventilator card). Card readers tended to jam
> when they got to one of these, as the resulting card had too little
> structural strength to avoid buckling inside the mechanism. Card punches
> could also jam trying to produce these things owing to power-supply
> problems. When some practical joker fed a lace card through the reader,
> you needed to clear the jam with a card
> knife --- which you used on the joker first.

****

****lasherism**: n.**Revision 2.9.10??? 

Added

Revision 2.9.12??? 

Changed

Revision 4.4.0??? 

Deleted: No evidence of live use.

> \[Harvard\] A program that solves a standard problem (such as the
> Eight Queens puzzle or implementing the _life_
> algorithm) in a deliberately nonstandard way. Distinguished from a
> _crock_ or _kluge_ by the fact
> that the programmer did it on purpose as a mental exercise. Such
> constructions are quite popular in exercises such as the
> _Obfuscated C Contest_, and occasionally in
> _retrocomputing_. Lew Lasher was a student at Harvard
> around 1980 who became notorious for such behavior.

****

****LDB**: /l@'d@b/, vt.**Revision 1.1.0??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use.

> \[from the PDP-10 instruction set\] To extract from the middle.
> "LDB me a slice of cake, please." This usage has been kept
> alive by Common LISP's function of the same name. Considered silly.

****

****macrotape**: /mak'roh-tayp/, n.**Revision 1.1.0??? 

Added

Revision 4.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: This technology is dead.

> An industry-standard reel of tape. Originally, as opposed to a DEC
> microtape; nowadays, as opposed to modern QIC and DDS tapes.
> Syn. _round tape_.

****

****microfloppies**: n.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: 5.25-inch floppies are gone.

> 3.5-inch floppies, as opposed to 5.25-inch
> _vanilla_ or mini-floppies and the now-obsolete 8-inch
> variety. This term may be headed for obsolescence as 5.25-inchers pass out
> of use, only to be revived if anybody floats a sub-3-inch floppy standard.
> See _stiffy_,
> _minifloppies_.

****

****minifloppies**: n.,obs.**Revision 2.6.1??? 

Added

Revision 4.2.2??? 

Changed

Revision 4.4.0??? 

Deleted: They're gone.

> 5.25-inch floppy disks, as opposed to 3.5-inch or
> _microfloppies_ and the long-obsolescent 8-inch
> variety (if there is ever a smaller size, they will undoubtedly be tagged
> nanofloppies). At one time, this
> term was a trademark of Shugart Associates for their SA-400 minifloppy
> drive. Nobody paid any attention. See
> _stiffy_.

****

****GFR**: /G-F-R/, vt.**Revision 2.1.5??? 

Added

Revision 4.4.0??? 

Deleted: ITS slang has been pretty much dead for twelve
years.

> \[ITS: from \`Grim File Reaper', an ITS and LISP Machine utility\] To
> remove a file or files according to some program-automated or
> semi-automatic manual procedure, especially one designed to reclaim mass
> storage space or reduce name-space clutter (the original GFR actually moved
> files to tape). Often generalized to pieces of data below file level.
> "I used to have his phone number, but I guess I
> _GFR_ed it." See also
> _prowler_, _reaper_. Compare
> _GC_, which discards only provably worthless
> stuff.

****

****multician**: /muhl-ti'shn/, n.**Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: Multics is gone.

> \[coined at Honeywell, ca. 1970\] Competent user of
> _Multics_. Perhaps oddly, no one has ever promoted
> the analogous \`Unician'.

****

****netrock**: /net'rok/, n.**Revision 2.4.3??? 

Added

Revision 4.4.0??? 

Deleted: The Web provides no evidence that VNET still
exists.

> \[IBM\] A _flame_; used esp.: on VNET, IBM's
> internal corporate network.

****

****nroff**: /N'rof/**Revision 2.9.10??? 

Added

Revision 4.4.0??? 

Deleted: I fixed 'troff' so it doesn't need this.

> n. \[Unix, from "new
> roff" (see _troff_)\] A companion program to the
> Unix typesetter _troff_, accepting identical input but
> preparing output for terminals and line printers.

****

****round tape**: n.**Revision 2.9.10??? 

Added

Revision 4.4.0??? 

Deleted: Round tape is dead.

> Industry-standard 1/2-inch magnetic tape (7- or 9-track) on
> traditional circular reels. See _macrotape_, oppose
> _square tape_.

****

****Telerat**: /tel'@-rat/, n. obs.**Revision 2.1.5??? 

Added

Revision 4.4.0??? 

Deleted: Long dead.

> Unflattering hackerism for \`Teleray', a now-extinct line of
> extremely losing terminals. Compare _AIDX_,
> _Macintrash_ _ScumOS_,
> _sun-stools_, _HP-SUX_,
> _Slowlaris_.

****

****ventilator card**: n.**Revision 2.9.12??? 

Added

Revision 4.4.0??? 

Deleted: Dead along with lace card.

> Syn. _lace card_.

****

****PC-ism**: /P-C-izm/, n.**Revision 2.2.1??? 

Added

Revision 4.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: This doesn't happen any more.

> A piece of code or coding technique that takes advantage of the
> unprotected single-tasking environment in IBM PCs and the like running DOS,
> e.g., by busy-waiting on a hardware register, direct diddling of screen
> memory, or using hard timing loops. Compare
> _ill-behaved_, _vaxism_,
> _unixism_. Also, PC-ware n., a program full of PC-isms on a
> machine with a more capable operating system. Pejorative.

****

****Helen Keller mode**: n.**Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: sense 2 is dead, sense 1 is not enough to carry
the entry.

> 1\. State of a hardware or software system that is deaf, dumb, and
> blind, i.e., accepting no input and generating no output, usually due to an
> infinite loop or some other excursion into _deep
> space_. (Unfair to the real Helen Keller, whose success at
> learning speech was triumphant.) See also _go
> flatline_, _catatonic_. 

> 2\. On IBM PCs under DOS, refers to a specific failure mode in which
> a screen saver has kicked in over an _ill-behaved_
> application which bypasses the very interrupts the screen saver watches for
> activity. Your choices are to try to get from the program's current state
> through a successful save-and-exit without being able to see what you're
> doing, or to re-boot the machine. This isn't (strictly speaking) a
> crash.

****

****node**: n.**Revision 3.3.2??? 

Added

Revision 4.4.0??? 

Deleted: UUCP and serial-line BBSses are both
obsolete.

> 1\. \[Internet, UUCP\] A host machine on the network.

> 2\. \[MS-DOS BBSes\] A dial-in line on a BBS. Thus an MS-DOS
> _sysop_ might say that his BBS has 4 nodes even though
> it has a single machine and no Internet link, confusing an Internet hacker
> no end.

****

****OSU**: /O-S-U/, n. obs.**Revision 3.1.0??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live usage.

> \[TMRC\] Acronym for Officially Sanctioned User; a user who is
> recognized as such by the computer authorities and allowed to use the
> computer above the objections of the security monitor.

****

****P-mail**: n.**Revision 2.9.12??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live use.

> \[rare\] Physical mail, as opposed to _email_.
> Synonymous with _snail-mail_, but much less
> common.

****

****square tape**: n.**Revision 2.9.10??? 

Added

Revision 2.9.12??? 

Changed

Revision 4.4.0??? 

Deleted: All tape is square (e.g. DLTs)
now.

> Mainframe magnetic tape cartridges for use with IBM 3480 or
> compatible tape drives; or QIC tapes used on workstations and micros. The
> term comes from the square (actually rectangular) shape of the cartridges;
> contrast _round tape_.

****

****PETSCII**: /pet'skee/, n. obs.**Revision 2.4.3??? 

Added

Revision 4.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: Long dead along with the Commodore
PET

> \[abbreviation of PET ASCII\] The variation (many would say
> perversion) of the _ASCII_ character set used by the
> Commodore Business Machines PET series of personal computers and the later
> Commodore C64, C16, C128, and VIC20 machines. The PETSCII set used
> left-arrow and up-arrow (as in old-style ASCII) instead of underscore and
> caret, placed the unshifted alphabet at positions 65--90, put the shifted
> alphabet at positions 193--218, and added graphics characters.

****

****rib site**: n.**Revision 2.5.1??? 

Added

Revision 4.4.0??? 

Deleted: Obsolete along with UUCP.

> \[by analogy with _backbone site_\] A machine
> that has an on-demand high-speed link to a _backbone
> site_ and serves as a regional distribution point for lots of
> third-party traffic in email and Usenet news. Compare _leaf
> site_, _backbone site_.

****

****rice box**: n.**Revision 2.1.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live usage.

> \[from ham radio slang\] Any Asian-made commodity computer, esp.: an
> 80x86-based machine built to IBM PC-compatible ISA or EISA-bus
> standards.

****

****rusty memory**: n.**Revision 2.5.1??? 

Added

Revision 4.4.0??? 

Deleted: No evidence of live usage.

> Mass-storage that uses iron-oxide-based magnetic media (esp.: tape
> and the pre-Winchester removable disk packs used in _washing
> machine_s).

****

****ScumOS**: /skuhm'os/, /skuhm'O-S/, n.**Revision 2.9.10??? 

Added

Revision 4.4.0??? 

Deleted: It's dead.

> Unflattering hackerism for SunOS, the BSD Unix variant supported on
> Sun Microsystems's Unix workstations (see also
> _sun-stools_), and compare
> _Macintrash_, _HP-SUX_. Despite
> what this term might suggest, Sun was founded by hackers and still enjoys
> excellent relations with hackerdom; usage is more often in exasperation
> than outright loathing.

****

****sidecar**: n.**Revision 2.5.1??? 

Added

Revision 4.4.0??? 

Deleted: Obsolete along with the micros it refers
to.

> 1\. Syn. _slap on the side_. Esp.: used of
> add-ons for the late and unlamented IBM PCjr. 

> 2\. The IBM PC compatibility box that could be bolted onto the side
> of an Amiga. Designed and produced by Commodore, it broke all of the
> company's own design rules. If it worked with any other peripherals, it
> was by _magic_. 

> 3\. More generally, any of various devices designed to be connected
> to the expansion slot on the left side of the Amiga 500 (and later, 600
> & 1200), which included a hard drive controller, a hard drive, and
> additional memory.

****

****tall card**: n.**Revision 2.4.3??? 

Added

Revision 4.4.0??? 

Deleted: AT-sized expansion cards are now
standard.

> A PC/AT-size expansion card (these can be larger than IBM PC or XT
> cards because the AT case is bigger). See also _short
> card_. When IBM introduced the PS/2 model 30 (its last gasp at
> supporting the ISA) they made the case lower and many industry-standard
> tall cards wouldn't fit; this was felt to be a reincarnation of the
> _connector conspiracy_, done with less style.

****

****terpri**: /ter'pree/, vi.**Revision 1.1.0??? 

Added

Revision 2.9.10??? 

Changed

Revision 4.4.0??? 

Deleted: archaic as jargon even in CLISP, whicg still has
the function.

> \[from LISP 1.5 (and later, MacLISP)\] To output a
> _newline_. Now rare as jargon, though still used as
> techspeak in Common LISP. It is a contraction of \`TERminate PRInt line',
> named for the fact that, on some early OSes and hardware, no characters
> would be printed until a complete line was formed, so this operation
> terminated the line and emitted the output.

****

****UUCPNET**: n. obs.**Revision 2.2.1??? 

Added

Revision 4.0.0??? 

Changed

Revision 4.4.0??? 

Deleted: UUCP is dead.

> The store-and-forward network consisting of all the world's
> connected Unix machines (and others running some clone of the UUCP
> (Unix-to-Unix CoPy) software). Any machine reachable only via a
> _bang path_ is on UUCPNET. This term has been
> rendered obsolescent by the spread of cheap Internet connections in the
> 1990s; the few remaining UUCP links are essentially slow channels to the
> Internet rather than an autonomous network. See _network
> address_.

****

****VAXectomy**: /vak-sek't@-mee/, n.**Revision 2.7.1??? 

Added

Revision 4.4.0??? 

Deleted: Pretty much everybody is VAXectomized by
now.

> \[by analogy with 'vasectomy'\] A VAX removal.
> _DEC_'s Microvaxen, especially, are much slower than
> newer RISC-based workstations such as the SPARC. Thus, if one knows one
> has a replacement coming, VAX removal can be cause for celebration.

****

****vaxherd**: /vaks'herd/, n. obs.**Revision 2.9.6??? 

Added

Revision 3.3.2??? 

Changed

Revision 4.4.0??? 

Deleted: Today's VAXen don't have
operators.

> \[from 'oxherd'\] A VAX operator. The image is reinforced
> because VAXen actually did tend to come in herds, technically known as
> clusters.

****

****vaxism**: /vak'sizm/, n.**Revision 2.2.1??? 

Added

Revision 4.4.0??? 

Deleted: The variety of architectures has decreased.
Almost all machines (and, in particular, micros) look like VAXes
now.

> A piece of code that exhibits _vaxocentrism_ in
> critical areas. Compare _unixism_.

****

****W2K bug****Revision 4.1.3??? 

Added

Revision 4.4.0??? 

Deleted: It was. And nobody noticed.

> \[from \`Y2K bug' for the Year 2000 problem\] The deployment of
> Microsoft's Windows 2000 operating system, which hackers generally expect
> will turn out to have been among the worst train wrecks in the history of
> software engineering. Such is the power of Microsoft marketing, however,
> that it is also expected this will not become obvious until it has incurred
> hundreds of millions of dollars in downtime and lost opportunity
> costs.

****

****woofer**: n.**Revision 2.9.7??? 

Added

Revision 2.9.12??? 

Changed

Revision 4.4.0??? 

Deleted: Pin-feed printers are dead.

> \[University of Waterloo\] Some varieties of wide paper for printers
> have a perforation 8.5 inches from the left margin that allows the excess
> on the right-hand side to be torn off when the print format is 80 columns
> or less wide. The right-hand excess may be called 'woofer'.
> This term (like _tweeter_) has been in use at Waterloo
> since 1972, but is elsewhere unknown. In audio jargon, the word refers to
> the bass speaker(s) on a hi-fi.

****

****Yellow Book**: n.**Revision 2.6.1??? 

Added

Revision 3.1.0??? 

Changed

Revision 3.3.3??? 

Changed

Revision 4.4.0??? 

Deleted: Seems to no longer be in any live
use.

> The print version of this Jargon File; _The New Hacker's
> Dictionary_ from MIT Press; The book includes essentially all
> the material in the File, plus a Foreword by Guy L.: Steele Jr. and a
> Preface by Eric S. Raymond. Most importantly, the book version is nicely
> typeset and includes almost all of the infamous Crunchly cartoons by the
> Great Quux, each attached to an appropriate entry. The first edition
> (1991, ISBN 0-262-68069-6) corresponded to the Jargon File version 2.9.6\.
> The second edition (1993, ISBN 0-262-68079-3) corresponded to the Jargon
> File 3.0.0\. The third (1996, ISBN 0-262-68092-0) corresponded to
> 4.0.0\.

****

****slap on the side**: n.**Revision 2.3.1??? 

Added

Revision 4.4.0??? 

Deleted: Dead along with the micros that used
it.

> (also called a _sidecar_, or abbreviated
> SOTS.) A type of external expansion
> hardware marketed by computer manufacturers (e.g., Commodore for the Amiga
> 500/1000 series and IBM for the hideous failure called 'PCjr').
> Various SOTS boxes provided necessities such as memory, hard drive
> controllers, and conventional expansion slots.

****

****tweeter**: n.**Revision 2.9.7??? 

Added

Revision 4.4.0??? 

Deleted: Goes with woofer

> \[University of Waterloo\] Syn. _perf_,
> _chad_ (sense 1). This term (like
> _woofer_) has been in use at Waterloo since 1972 but
> is elsewhere unknown. In audio jargon, the word refers to the treble
> speaker(s) on a hi-fi.

****

****SOS**: /S-O-S/**Revision 1.1.0??? 

Added: sense 1 only

Revision 4.1.1??? 

Changed: dropped PDP-10 instruction sense
2

Revision 4.2.0??? 

Changed

Revision 4.4.0??? 

Deleted: It's been pushing two decades since anyone used
SOS for production.

> n.,obs. An infamously
> _losing_ text editor. Once, back in the 1960s, when a
> text editor was needed for the PDP-6, a hacker crufted together a
> _quick-and-dirty_ \`stopgap editor' to be used until a
> better one was written. Unfortunately, the old one was never really
> discarded when new ones came along. SOS is a descendant (\`Son of Stopgap')
> of that editor, and many PDP-10 users gained the dubious pleasure of its
> acquaintance. Since then other programs similar in style to SOS have been
> written, notably the early font editor BILOS /bye'lohs/, the Brother-In-Law Of Stopgap
> (the alternate expansion \`Bastard Issue, Loins of Stopgap' has been
> proposed).

> 1\. /sos/ vt. To decrease; inverse of
> _AOS_, from the PDP-10 instruction set.

****

****stiffy**: n.**Revision 2.3.1??? 

Added

Revision 4.2.0??? 

Changed

Revision 4.4.0??? 

Deleted: Floppies are dead.

> 3.5-inch floppies, so called because their jackets are more rigid
> than those of the 5.25-inch and the (now totally obsolete) 8-inch floppy.
> Elsewhere this might be called a firmy. For some odd reason, several sources
> have taken the trouble to inform us that this term is widespread in South
> Africa. Australians, on the other hand, suggest being careful with it when
> Down Under, as it is there universally slang for an erection.

****

****short card**: n.**Revision 2.4.3??? 

Added

Revision 3.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: Goes with 'tall card'

> A half-length IBM XT expansion card or adapter that will fit in one
> of the two short slots located towards the right rear of a standard chassis
> (tucked behind the floppy disk drives). See also _tall
> card_.

****

****Silver Book**: n.**Revision 2.1.1??? 

Added: (deduced from diffs)

> Jensen and Wirth's infamous _Pascal User Manual and
> Report_, so called because of the silver cover of the widely
> distributed Springer-Verlag second edition of 1978 (ISBN 0-387-90144-2).
> See _book titles_,
> _Pascal_.

****

****Devil Book**: n.**Revision 2.8.3??? 

Added: (deduced from diffs)

Revision 3.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: No evidence of live use, 2002\.

> See _daemon book_, the term preferred by its
> authors.

****

****crayola books**: n.**Revision 2.9.11??? 

Added

Revision 4.3.1??? 

Changed

Revision 4.4.0??? 

Deleted: Long obsolete; no evidence of live
use.

> The _rainbow series_ of National Computer
> Security Center (NCSC) computer security standards (see _Orange
> Book_), now obsolete and discontinued. Usage: humorous and/or
> disparaging.

****

****4.2**: /for' poynt too'/, n.**Revision 3.1.0??? 

Added

Revision 4.4.0??? 

Deleted: Over a decade dead.

> \[now obs.\] Without a prefix, this almost invariably refers to
> _BSD_ Unix release 4.2\. Note that it is an indication
> of cluelessness to say "version 4.2", and "release
> 4.2" is rare; the number stands on its own, or is used in the more
> explicit forms 4.2BSD or (less commonly) BSD 4.2\. Similar remarks apply to
> "4.3", "4.4" and to earlier, less-widespread
> releases 4.1 and 2.9\.

****

****AI koans**: /A-I koh'anz/, pl.n.**Revision 2.2.1??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: Duplicates 'koan'

> A series of pastiches of Zen teaching riddles created by Danny
> Hillis at the MIT AI Lab around various major figures of the Lab's culture
> (several are included under _Some AI Koans_ in
> Appendix A). See also _ha ha only serious_,
> _mu_, and _hacker humor_.

****

****Big Gray Wall**: n.**Revision 2.3.1??? 

Added: (deduced from diffs)

Revision 2.9.6??? 

Renamed: 'Big Grey Wall' -\> 'Big Gray Wall' (deduced from
diffs)

Revision 2.9.10??? 

Changed

Revision 4.4.0??? 

Deleted: No evidence of live use on the Web, October
2002\.

> What faces a _VMS_ user searching for
> documentation. A full VMS kit comes on a pallet, the documentation taking
> up around 15 feet of shelf space before the addition of layered products
> such as compilers, databases, multivendor networking, and programming
> tools. Recent (since VMS version 5) documentation comes with gray binders;
> under VMS version 4 the binders were orange (big
> orange wall), and under version 3 they were blue. See
> _VMS_. Often contracted to Gray Wall.

****

****Blue Book**: n.**Revision 2.1.5??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: All three books are obsolete or superseded by more
recent versions.

> 1\. Informal name for one of the four standard references on the
> page-layout and graphics-control language _PostScript_
> (_PostScript Language Tutorial and Cookbook_, Adobe
> Systems, Addison-Wesley 1985, QA76.73.P67P68, ISBN 0-201-10179-3); the
> other three official guides are known as the _Green
> Book_, the _Red Book_, and the
> _White Book_ (sense 2). 

> 2\. Informal name for one of the three standard references on
> Smalltalk: _Smalltalk-80: The Language and its
> Implementation_, David Robson, Addison-Wesley 1983,
> QA76.8.S635G64, ISBN 0-201-11371-63 (this book also has green and red
> siblings).

> 3\. Any of the 1988 standards issued by the CCITT's ninth plenary
> assembly. These include, among other things, the X.400 email spec and the
> Group 1 through 4 fax standards. See also _book
> titles_.

****

****Green Book**: n.**Revision 2.1.5??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: These Green Books are obsolete or
superseded.

> 1\. One of the four standard _PostScript_
> references: _PostScript Language Program Design_,
> bylined \`Adobe Systems' (Addison-Wesley, 1988; QA76.73.P67P66 ISBN
> 0-201-14396-8); see also _Red Book_, _Blue
> Book_, and the _White Book_ (sense 2).
> 

> 2\. Informal name for one of the three standard references on
> SmallTalk: _Smalltalk-80: Bits of History, Words of
> Advice_, by Glenn Krasner (Addison-Wesley, 1983; QA76.8.S635S58;
> ISBN 0-201-11669-3) (this, too, is associated with blue and red books).
> 

> 3\. The _X/Open Compatibility Guide_, which
> defines an international standard _Unix_ environment
> that is a proper superset of POSIX/SVID; also includes descriptions of a
> standard utility toolkit, systems administration features, and the like.
> This grimoire is taken with particular seriousness in Europe. See
> _Purple Book_. 

> 4\. The IEEE 1003.1 POSIX Operating Systems Interface standard has
> been dubbed "The Ugly Green Book".

> 5\. Any of the 1992 standards issued by the CCITT's tenth plenary
> assembly. These include, among other things, the X.400 email standard and
> the Group 1 through 4 fax standards. See also _book
> titles_.

****

****Red Book**: n.**Revision 2.1.5??? 

Added: (deduced from diffs)

Revision 2.9.10??? 

Changed

Revision 4.1.1??? 

Changed

Revision 4.4.0??? 

Deleted: These Red Books are now too old to be useful
examples.

> 1\. Informal name for one of the four standard references on
> _PostScript_ (_PostScript Language Reference
> Manual_, Adobe Systems (Addison-Wesley, 1985; QA76.73.P67P67;
> ISBN 0-201-10174-2, or the 1990 second edition ISBN 0-201-18127-4); the
> others are known as the _Green Book_, the
> _Blue Book_, and the _White Book_
> (sense 2). 

> 2\. Informal name for one of the 3 standard references on Smalltalk
> (_Smalltalk-80: The Interactive Programming
> Environment_ by Adele Goldberg (Addison-Wesley, 1984;
> QA76.8.S635G638; ISBN 0-201-11372-4); this too is associated with blue and
> green books).

> 3\. Any of the 1984 standards issued by the CCITT eighth plenary
> assembly. These include, among other things, the X.400 email spec and the
> Group 1 through 4 fax standards. 

> 4\. The new version of the _Green Book_ (sense
> 4) --- IEEE 1003.1-1990, a.k.a ISO 9945-1 --- is (because of the
> color and the fact that it is printed on A4 paper) known in the USA as
> "the Ugly Red Book That Won't Fit On The Shelf" and in Europe
> as "the Ugly Red Book That's A Sensible Size". 

> 5\. The NSA _Trusted Network Interpretation_
> companion to the _Orange Book_. 

> 6\. Nemeth, Snyder, Seebass, Hein; _Unix System
> Administration Handbook, Second Edition_ (Prentice Hall PTR, New
> Jersey; 1995; QA76.76.063N45; ISBN 0-13-151051-7). See also
> _book titles_.

****

****White Book**: n.**Revision 2.1.1??? 

Added: (deduced from diffs)

Revision 2.9.10??? 

Changed

Revision 4.4.0??? 

Deleted: Sense 1 merged to K&R

> 1\. Syn. _K&R_. 

> 2\. Adobe's fourth book in the PostScript series, describing the
> previously-secret format of Type 1 fonts; _Adobe Type 1 Font
> Format, version 1.1_, (Addison-Wesley, 1990, ISBN
> 0-201-57044-0). See also _Red Book_, _Green
> Book_, _Blue Book_.

****

****BQS**: /B-Q-S/, adj.**Revision 2.7.1??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: No evidence of live use in
2002\.

> Syn. _Berkeley Quality Software_.

****

****brochureware**: n.**Revision 2.9.11??? 

Added

Revision 4.4.0??? 

Deleted: According to an Oct 2002 Google search, this sense
no longer seems to be live.

> Planned but non-existent product like
> _vaporware_, but with the added implication that
> marketing is actively selling and promoting it (they've printed brochures).
> Brochureware is often deployed as a strategic weapon; the idea is to con
> customers into not committing to an existing product of the competition's.
> It is a safe bet that when a brochureware product finally becomes real, it
> will be more expensive than and inferior to the alternatives that had been
> available for years.

****

****desk check**: n.,v.**Revision 2.5.1??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: Techspeak.

> To _grovel_ over hardcopy of source code,
> mentally simulating the control flow; a method of catching bugs. No longer
> common practice in this age of on-screen editing, fast compiles, and
> sophisticated debuggers --- though some maintain stoutly that it ought
> to be. Compare _eyeball search_,
> _vdiff_, _vgrep_.

****

****echo**: n.**Revision 2.4.1??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: FidoNet slang, no longer
interesting.

> A _topic group_ on
> _FidoNet_'s echomail system. Compare
> _newsgroup_.

****

****fd leak**: /F-D leek/, n.**Revision 2.1.5??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: Readily scrutable from its component
parts.

> A kind of programming bug analogous to a _core
> leak_, in which a program fails to close file descriptors
> (fds) after file operations are
> completed, and thus eventually runs out of them. See
> _leak_.

****

****g-file**: n.**Revision 3.2.0??? 

Added

Revision 4.4.0??? 

Deleted: No live usage revealed by Oct 2002 Google
search.

> \[Commodore BBS culture\] Any file that is written with the intention
> of being read by a human rather than a machine, such as the Jargon File,
> documentation, humor files, hacker lore, and technical materials.
> 
> This term survives from the nearly forgotten Commodore 64 underground
> and BBS community. In the early 80s, C-Net had emerged as the most popular
> C64 BBS software for systems which encouraged messaging (as opposed to file
> transfer). There were three main options for files: Program files
> (p-files), which served the same function as \`doors' in today's systems, UD
> files (the user upload/download section), and g-files. Anything that was
> meant to be read was included in g-files.

****

****gag**: vi.**Revision 2.1.1??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: mainstream

> Equivalent to _choke_, but connotes more
> disgust. "Hey, this is FORTRAN code. No wonder the C compiler
> gagged." See also _barf_.

****

****machinable**: adj.**Revision 2.8.1??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: No evidence of live use, 2002\.

> Machine-readable. Having the _softcopy_
> nature.

****

****lexiphage**: /lek'si-fayj\`/, n.**Revision 2.9.6??? 

Added: (deduced from diffs)

Revision 3.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: dead along with ITS

> A notorious word _chomper_ on ITS. See
> _bagbiter_. This program would draw on a selected
> victim's bitmapped terminal the words "THE BAG" in ornate
> letters, followed by a pair of jaws biting pieces of it off.

****

****line starve****Revision 1.1.0??? 

Added: (deduced from diffs)

Revision 2.9.10??? 

Changed

Revision 4.2.0??? 

Changed

Revision 4.4.0??? 

Deleted: Obsolete along with line
printers.

> 1\. \[MIT\] vi. To feed paper
> through a printer the wrong way by one line (most printers can't do this).
> On a display terminal, to move the cursor up to the previous line of the
> screen. "To print \`X squared', you just output \`X', line starve,
> \`2', line feed." (The line starve causes the \`2' to appear on the
> line above the \`X', and the line feed gets back to the original line.)
> 

> 2\. n. A character (or character
> sequence) that causes a terminal to perform this action. ASCII 0011010,
> also called SUB or control-Z, was one common line-starve character in the
> days before microcomputers and the X3.64 terminal standard. Today, the
> term might be used for the ISO reverse line feed character 0x8D. Unlike
> line feed, line starve is _not_
> standard _ASCII_ terminology. Even among hackers it
> is considered a bit silly.

> 3\. \[proposed\] A sequence such as \\c (used in System V echo, as well
> as _troff_) that suppresses a
> _newline_ or other character(s) that would normally be
> emitted.

****

****LPT**: /L-P-T/, /lip'it/, /lip-it'/, n.**Revision 1.1.0??? 

Added: (deduced from diffs)

Revision 4.1.0??? 

Changed

Revision 4.4.0??? 

Deleted: Seems to be thoroughly dead at this
point.

> 1\. Line printer (originally Line Printing Terminal). Rare under
> Unix, more common among hackers who grew up with ITS, MS-DOS, CP/M and
> other operating systems that were strongly influenced by early
> _DEC_ conventions. 

> 2\. Local PorT. Used among MS-DOS/Windows programmers (and so
> expanded in the MS-DOS 5 manual). It seems likely this is a
> _backronym_.

****

****PDL**: /P-D-L/, /pid'l/, /p@d'l/, /puhd'l/**Revision 1.1.0??? 

Added: (deduced from diffs)

Revision 2.9.7??? 

Changed

Revision 2.9.10??? 

Changed

Revision 2.9.12??? 

Added

Revision 4.4.0??? 

Deleted: Senses 4 and 5 are no longer live; remainder are
not enough to carry the entry.

> 

> 1\. n. \`Program Design Language'.
> Any of a large class of formal and profoundly useless pseudo-languages in
> which _management_ forces one to design programs. Too
> often, management expects PDL descriptions to be maintained in parallel
> with the code, imposing massive overhead to little or no benefit. See also
> _flowchart_.

> 2\. v. To design using a program
> design language. "I've been pdling so long my eyes won't focus
> beyond 2 feet." 

> 3\. n. \`Page Description
> Language'. Refers to any language which is used to control a graphics
> device, usually a laserprinter. The most common example is, of course,
> Adobe's _PostScript_ language, but there are many
> others, such as Xerox InterPress, etc.

> 4\. In ITS days, the preferred MITism for
> _stack_. See _overflow pdl_.
> 

> 5\. Dave Lebling, one of the co-authors of
> _Zork_; (his _network address_ on
> the ITS machines was at one time pdl@dms).

****

****overflow pdl**: n.**Revision 1.5.0??? 

Added: (deduced from diffs)

Revision 2.1.1??? 

Deleted: (deduced from diffs)

Revision 2.9.7??? 

Added

Revision 2.9.12??? 

Changed

Revision 4.4.0??? 

Deleted: Goes with PDL

> \[MIT\] The place where you put things when your
> _PDL_ is full. If you don't have one and too many
> things get pushed, you forget something. The overflow pdl for a person's
> memory might be a memo pad. This usage inspired the following
> doggerel:
> 
>   
> Hey, diddle, diddle  
> The overflow pdl  
> To get a little more stack;  
> If that's not enough  
> Then you lose it all,  
> And have to pop all the way back.  
> --The Great Quux  
> 
> The term \`pdl' (see _PDL_) seems to be primarily
> an MITism; outside MIT this term is replaced by 'overflow
> _stack_' (but that wouldn't rhyme with
> \`diddle').

****

****pod**: n.**Revision 2.2.1??? 

Added: (deduced from diffs)

Revision 4.4.0??? 

Deleted: Seems to be dead in 2002\.

> \[allegedly from abbreviation POD for \`Prince Of Darkness'\] A Diablo
> 630 (or, latterly, any letter-quality impact printer). From the DEC-10
> PODTYPE program used to feed formatted text to it. Not to be confused with
> _P.O.D._.



[0]: http://www.catb.org/jargon/chaff.html#ALGOL
[1]: http://www.catb.org/jargon/chaff.html#ALGOL
[2]: http://www.catb.org/jargon/chaff.html#archiver
[3]: http://www.catb.org/jargon/chaff.html#balanced
[4]: http://www.catb.org/jargon/chaff.html#bit-mask
[5]: http://www.catb.org/jargon/chaff.html#bit-vector
[6]: http://www.catb.org/jargon/chaff.html#escape
[7]: http://www.catb.org/jargon/chaff.html#giant-blue-lobster
[8]: http://www.catb.org/jargon/chaff.html#GUI
[9]: http://www.catb.org/jargon/chaff.html#IPL
[10]: http://www.catb.org/jargon/chaff.html#kernel
[11]: http://www.catb.org/jargon/chaff.html#native-mode
[12]: http://www.catb.org/jargon/chaff.html#pass-by-name
[13]: http://www.catb.org/jargon/chaff.html#pass-by-reference
[14]: http://www.catb.org/jargon/chaff.html#pass-by-value
[15]: http://www.catb.org/jargon/chaff.html#race-condition
[16]: http://www.catb.org/jargon/chaff.html#RISC
[17]: http://www.catb.org/jargon/chaff.html#RMS
[18]: http://www.catb.org/jargon/chaff.html#signal
[19]: http://www.catb.org/jargon/chaff.html#spoofing
[20]: http://www.catb.org/jargon/chaff.html#stub
[21]: http://www.catb.org/jargon/chaff.html#Symbolics
[22]: http://www.catb.org/jargon/chaff.html#seer
[23]: http://www.catb.org/jargon/chaff.html#whitespace
[24]: http://www.catb.org/jargon/chaff.html#write-behind
[25]: http://www.catb.org/jargon/chaff.html#write-through
[26]: http://www.catb.org/jargon/chaff.html#spazz
[27]: http://www.catb.org/jargon/chaff.html#waterbottle-soccer
[28]: http://www.catb.org/jargon/chaff.html#sixty-nine
[29]: http://www.catb.org/jargon/chaff.html#PTY
[30]: http://www.catb.org/jargon/chaff.html#moon
[31]: http://www.catb.org/jargon/chaff.html#line-feed
[32]: http://www.catb.org/jargon/chaff.html#Cambridge-notation
[33]: http://www.catb.org/jargon/chaff.html#gateway
[34]: http://www.catb.org/jargon/chaff.html#Kleene-star
[35]: http://www.catb.org/jargon/chaff.html#snog
[36]: http://www.catb.org/jargon/chaff.html#assembler
[37]: http://www.catb.org/jargon/chaff.html#binary
[38]: http://www.catb.org/jargon/chaff.html#pointer-arithmetic
[39]: http://www.catb.org/jargon/chaff.html#religious-war
[40]: http://www.catb.org/jargon/chaff.html#cell-repair-machines
[41]: http://www.catb.org/jargon/chaff.html#big-BLT--the
[42]: http://www.catb.org/jargon/chaff.html#BIN
[43]: http://www.catb.org/jargon/chaff.html#cryonics
[44]: http://www.catb.org/jargon/chaff.html#diablo
[45]: http://www.catb.org/jargon/chaff.html#DMP
[46]: http://www.catb.org/jargon/chaff.html#dragon
[47]: http://www.catb.org/jargon/chaff.html#fuzz
[48]: http://www.catb.org/jargon/chaff.html#JRN--JRL
[49]: http://www.catb.org/jargon/chaff.html#IMPCOM
[50]: http://www.catb.org/jargon/chaff.html#JSYS
[51]: http://www.catb.org/jargon/chaff.html#output-spy
[52]: http://www.catb.org/jargon/chaff.html#phantom
[53]: http://www.catb.org/jargon/chaff.html#REL
[54]: http://www.catb.org/jargon/chaff.html#SAV
[55]: http://www.catb.org/jargon/chaff.html#SHR
[56]: http://www.catb.org/jargon/chaff.html#STY
[57]: http://www.catb.org/jargon/chaff.html#UUO
[58]: http://www.catb.org/jargon/chaff.html#XGP
[59]: http://www.catb.org/jargon/chaff.html#yoyo
[60]: http://www.catb.org/jargon/chaff.html#follow-on
[61]: http://www.catb.org/jargon/chaff.html#go-away
[62]: http://www.catb.org/jargon/chaff.html#How-hard-would-it-be
[63]: http://www.catb.org/jargon/chaff.html#IRP
[64]: http://www.catb.org/jargon/chaff.html#layer
[65]: http://www.catb.org/jargon/chaff.html#leading-edge
[66]: http://www.catb.org/jargon/chaff.html#organic-debugging
[67]: http://www.catb.org/jargon/chaff.html#price-performance
[68]: http://www.catb.org/jargon/chaff.html#utility
[69]: http://www.catb.org/jargon/chaff.html#wait-state
[70]: http://www.catb.org/jargon/chaff.html#belly-up
[71]: http://www.catb.org/jargon/chaff.html#black-box
[72]: http://www.catb.org/jargon/chaff.html#bottleneck
[73]: http://www.catb.org/jargon/chaff.html#close
[74]: http://www.catb.org/jargon/chaff.html#hot-key
[75]: http://www.catb.org/jargon/chaff.html#link
[76]: http://www.catb.org/jargon/chaff.html#listing
[77]: http://www.catb.org/jargon/chaff.html#mixed-case
[78]: http://www.catb.org/jargon/chaff.html#mount
[79]: http://www.catb.org/jargon/chaff.html#null-device
[80]: http://www.catb.org/jargon/chaff.html#panic
[81]: http://www.catb.org/jargon/chaff.html#port
[82]: http://www.catb.org/jargon/chaff.html#retrofit
[83]: http://www.catb.org/jargon/chaff.html#sadistics
[84]: http://www.catb.org/jargon/chaff.html#script
[85]: http://www.catb.org/jargon/chaff.html#SUPDUP
[86]: http://www.catb.org/jargon/chaff.html#grungy
[87]: http://www.catb.org/jargon/chaff.html#wow
[88]: http://www.catb.org/jargon/chaff.html#asymptotic
[89]: http://www.catb.org/jargon/chaff.html#bat-file
[90]: http://www.catb.org/jargon/chaff.html#sluggy
[91]: http://www.catb.org/jargon/chaff.html#spin-lock
[92]: http://www.catb.org/jargon/chaff.html#swapped
[93]: http://www.catb.org/jargon/chaff.html#what
[94]: http://www.catb.org/jargon/chaff.html#humongous
[95]: http://www.catb.org/jargon/chaff.html#blazer
[96]: http://www.catb.org/jargon/chaff.html#breakage
[97]: http://www.catb.org/jargon/chaff.html#FAtt
[98]: http://www.catb.org/jargon/chaff.html#firmware
[99]: http://www.catb.org/jargon/chaff.html#FReq
[100]: http://www.catb.org/jargon/chaff.html#ONE-BELL-SYSTEM-IT-WORKS
[101]: http://www.catb.org/jargon/chaff.html#pipeline
[102]: http://www.catb.org/jargon/chaff.html#salsman
[103]: http://www.catb.org/jargon/chaff.html#archive
[104]: http://www.catb.org/jargon/chaff.html#arc-wars
[105]: http://www.catb.org/jargon/chaff.html#berserking
[106]: http://www.catb.org/jargon/chaff.html#i14y
[107]: http://www.catb.org/jargon/chaff.html#i18n
[108]: http://www.catb.org/jargon/chaff.html#lame
[109]: http://www.catb.org/jargon/chaff.html#BartleMUD
[110]: http://www.catb.org/jargon/chaff.html#posing
[111]: http://www.catb.org/jargon/chaff.html#tinycrud
[112]: http://www.catb.org/jargon/chaff.html#K-line
[113]: http://www.catb.org/jargon/chaff.html#Q-line
[114]: http://www.catb.org/jargon/chaff.html#reset
[115]: http://www.catb.org/jargon/chaff.html#subshell
[116]: http://www.catb.org/jargon/chaff.html#brand-brand-brand
[117]: http://www.catb.org/jargon/chaff.html#fuggly
[118]: http://www.catb.org/jargon/chaff.html#hack-and-slay
[119]: http://www.catb.org/jargon/chaff.html#arc
[120]: http://www.catb.org/jargon/chaff.html#card
[121]: http://www.catb.org/jargon/chaff.html#silicon-foundry
[122]: http://www.catb.org/jargon/chaff.html#essentials
[123]: http://www.catb.org/jargon/chaff.html#fab
[124]: http://www.catb.org/jargon/chaff.html#unroll
[125]: http://www.catb.org/jargon/chaff.html#toto
[126]: http://www.catb.org/jargon/chaff.html#unleaded
[127]: http://www.catb.org/jargon/chaff.html#spoo
[128]: http://www.catb.org/jargon/chaff.html#spooge
[129]: http://www.catb.org/jargon/chaff.html#mango
[130]: http://www.catb.org/jargon/chaff.html#doco
[131]: http://www.catb.org/jargon/chaff.html#devo
[132]: http://www.catb.org/jargon/chaff.html#sendmail
[133]: http://www.catb.org/jargon/chaff.html#DEChead
[134]: http://www.catb.org/jargon/chaff.html#double-DECkers
[135]: http://www.catb.org/jargon/chaff.html#Open-DeathTrap
[136]: http://www.catb.org/jargon/chaff.html#microtape
[137]: http://www.catb.org/jargon/chaff.html#pig--run-like-a
[138]: http://www.catb.org/jargon/chaff.html#altmode
[139]: http://www.catb.org/jargon/chaff.html#AOS
[140]: http://www.catb.org/jargon/chaff.html#chine-nual
[141]: http://www.catb.org/jargon/chaff.html#blow-away
[142]: http://www.catb.org/jargon/chaff.html#cruncha-cruncha-cruncha
[143]: http://www.catb.org/jargon/chaff.html#CTY
[144]: http://www.catb.org/jargon/chaff.html#JRST
[145]: http://www.catb.org/jargon/chaff.html#news
[146]: http://www.catb.org/jargon/chaff.html#fepped-out
[147]: http://www.catb.org/jargon/chaff.html#JFCL
[148]: http://www.catb.org/jargon/chaff.html#PIP
[149]: http://www.catb.org/jargon/chaff.html#NOMEX-underwear
[150]: http://www.catb.org/jargon/chaff.html#Pink-Shirt-Book
[151]: http://www.catb.org/jargon/chaff.html#at-Begin
[152]: http://www.catb.org/jargon/chaff.html#backslash-begin
[153]: http://www.catb.org/jargon/chaff.html#bobbit
[154]: http://www.catb.org/jargon/chaff.html#JRLN
[155]: http://www.catb.org/jargon/chaff.html#computer-geek
[156]: http://www.darkwater.com/omni/geek.html
[157]: http://www.catb.org/jargon/chaff.html#Marginal-Hacks
[158]: http://www.catb.org/jargon/chaff.html#block-transfer-computations
[159]: http://www.catb.org/jargon/chaff.html#bodysurf-code
[160]: http://www.catb.org/jargon/chaff.html#bot-spot
[161]: http://www.catb.org/jargon/chaff.html#branch-to-Fishkill
[162]: http://www.catb.org/jargon/chaff.html#digit
[163]: http://www.catb.org/jargon/chaff.html#DPB
[164]: http://www.catb.org/jargon/chaff.html#gaseous
[165]: http://www.catb.org/jargon/chaff.html#laundromat
[166]: http://www.catb.org/jargon/chaff.html#Missed-em-five
[167]: http://www.catb.org/jargon/chaff.html#NetBOLLIX
[168]: http://www.catb.org/jargon/chaff.html#Pangloss-parity
[169]: http://www.catb.org/jargon/chaff.html#plingnet
[170]: http://www.catb.org/jargon/chaff.html#pnambic
[171]: http://www.catb.org/jargon/chaff.html#snivitz
[172]: http://www.catb.org/jargon/chaff.html#twonkie
[173]: http://www.catb.org/jargon/chaff.html#whalesong
[174]: http://www.catb.org/jargon/chaff.html#Snooze
[175]: http://www.catb.org/jargon/chaff.html#TechRef
[176]: http://www.catb.org/jargon/chaff.html#TELNET
[177]: http://www.catb.org/jargon/chaff.html#USG-Unix
[178]: http://www.catb.org/jargon/chaff.html#SysVile
[179]: http://www.catb.org/jargon/chaff.html#moose-call
[180]: http://www.catb.org/jargon/chaff.html#mouse-around
[181]: http://www.catb.org/jargon/chaff.html#one-twenty-reset
[182]: http://www.catb.org/jargon/chaff.html#Black-Thursday
[183]: http://www.catb.org/jargon/chaff.html#POPJ
[184]: http://www.catb.org/jargon/chaff.html#Internet-address
[185]: http://www.catb.org/jargon/chaff.html#wallpaper
[186]: http://www.catb.org/jargon/chaff.html#interrupt-list
[187]: http://www.catb.org/jargon/chaff.html#bum
[188]: http://www.catb.org/jargon/chaff.html#all-elbows
[189]: http://www.catb.org/jargon/chaff.html#PPN
[190]: http://www.catb.org/jargon/chaff.html#gurfle
[191]: http://www.catb.org/jargon/chaff.html#cycle-drought
[192]: http://www.catb.org/jargon/chaff.html#dup-loop
[193]: http://www.catb.org/jargon/chaff.html#Nominal-Semidestructor
[194]: http://www.catb.org/jargon/chaff.html#acolyte
[195]: http://www.catb.org/jargon/chaff.html#Ada
[196]: http://www.catb.org/jargon/chaff.html#AIDS
[197]: http://www.catb.org/jargon/chaff.html#AIDX
[198]: http://www.catb.org/jargon/chaff.html#amoeba
[199]: http://www.catb.org/jargon/chaff.html#ANSI
[200]: http://www.catb.org/jargon/chaff.html#backspace-and-overstrike
[201]: http://www.catb.org/jargon/chaff.html#banana-label
[202]: http://www.catb.org/jargon/chaff.html#baud-barf
[203]: http://www.catb.org/jargon/chaff.html#berklix
[204]: http://www.catb.org/jargon/chaff.html#BITNET
[205]: http://www.catb.org/jargon/chaff.html#bixen
[206]: http://www.catb.org/jargon/chaff.html#blink
[207]: http://www.catb.org/jargon/chaff.html#buglix
[208]: http://www.catb.org/jargon/chaff.html#can
[209]: http://www.catb.org/jargon/chaff.html#card-walloper
[210]: http://www.catb.org/jargon/chaff.html#corge
[211]: http://www.catb.org/jargon/chaff.html#cray-instability
[212]: http://www.catb.org/jargon/chaff.html#crayola
[213]: http://www.catb.org/jargon/chaff.html#crayon
[214]: http://www.catb.org/jargon/chaff.html#cubing
[215]: http://www.catb.org/jargon/chaff.html#cycle-crunch
[216]: http://www.catb.org/jargon/chaff.html#D--C--Power-Lab
[217]: http://www.catb.org/jargon/chaff.html#dead-link
[218]: http://www.catb.org/jargon/chaff.html#cray
[219]: http://www.catb.org/jargon/chaff.html#domainist
[220]: http://www.catb.org/jargon/chaff.html#donuts
[221]: http://www.catb.org/jargon/chaff.html#dup-killer
[222]: http://www.catb.org/jargon/chaff.html#earthquake
[223]: http://www.catb.org/jargon/chaff.html#farming
[224]: http://www.catb.org/jargon/chaff.html#Fight-o-net
[225]: http://www.catb.org/jargon/chaff.html#File-Attach
[226]: http://www.catb.org/jargon/chaff.html#File-Request
[227]: http://www.catb.org/jargon/chaff.html#firmy
[228]: http://www.catb.org/jargon/chaff.html#FTP
[229]: http://www.catb.org/jargon/chaff.html#FUD-wars
[230]: http://www.catb.org/jargon/chaff.html#fuzzball
[231]: http://www.catb.org/jargon/chaff.html#gabriel
[232]: http://www.catb.org/jargon/chaff.html#gripenet
[233]: http://www.catb.org/jargon/chaff.html#gun
[234]: http://www.catb.org/jargon/chaff.html#Gosperism
[235]: http://www.catb.org/jargon/chaff.html#grault
[236]: http://www.catb.org/jargon/chaff.html#haque
[237]: http://www.catb.org/jargon/chaff.html#hobbit
[238]: http://www.catb.org/jargon/chaff.html#humma
[239]: http://www.catb.org/jargon/chaff.html#IBM-discount
[240]: http://www.catb.org/jargon/chaff.html#inc
[241]: http://www.catb.org/jargon/chaff.html#jolix
[242]: http://www.catb.org/jargon/chaff.html#lace-card
[243]: http://www.catb.org/jargon/chaff.html#lasherism
[244]: http://www.catb.org/jargon/chaff.html#LDB
[245]: http://www.catb.org/jargon/chaff.html#macrotape
[246]: http://www.catb.org/jargon/chaff.html#microfloppies
[247]: http://www.catb.org/jargon/chaff.html#minifloppies
[248]: http://www.catb.org/jargon/chaff.html#GFR
[249]: http://www.catb.org/jargon/chaff.html#multician
[250]: http://www.catb.org/jargon/chaff.html#netrock
[251]: http://www.catb.org/jargon/chaff.html#nroff
[252]: http://www.catb.org/jargon/chaff.html#round-tape
[253]: http://www.catb.org/jargon/chaff.html#Telerat
[254]: http://www.catb.org/jargon/chaff.html#ventilator-card
[255]: http://www.catb.org/jargon/chaff.html#PC-ism
[256]: http://www.catb.org/jargon/chaff.html#Helen-Keller-mode
[257]: http://www.catb.org/jargon/chaff.html#node
[258]: http://www.catb.org/jargon/chaff.html#OSU
[259]: http://www.catb.org/jargon/chaff.html#P-mail
[260]: http://www.catb.org/jargon/chaff.html#square-tape
[261]: http://www.catb.org/jargon/chaff.html#PETSCII
[262]: http://www.catb.org/jargon/chaff.html#rib-site
[263]: http://www.catb.org/jargon/chaff.html#rice-box
[264]: http://www.catb.org/jargon/chaff.html#rusty-memory
[265]: http://www.catb.org/jargon/chaff.html#ScumOS
[266]: http://www.catb.org/jargon/chaff.html#sidecar
[267]: http://www.catb.org/jargon/chaff.html#tall-card
[268]: http://www.catb.org/jargon/chaff.html#terpri
[269]: http://www.catb.org/jargon/chaff.html#UUCPNET
[270]: http://www.catb.org/jargon/chaff.html#VAXectomy
[271]: http://www.catb.org/jargon/chaff.html#vaxherd
[272]: http://www.catb.org/jargon/chaff.html#vaxism
[273]: http://www.catb.org/jargon/chaff.html#W2K-bug
[274]: http://www.catb.org/jargon/chaff.html#woofer
[275]: http://www.catb.org/jargon/chaff.html#Yellow-Book
[276]: http://www.catb.org/jargon/chaff.html#slap-on-the-side
[277]: http://www.catb.org/jargon/chaff.html#tweeter
[278]: http://www.catb.org/jargon/chaff.html#SOS
[279]: http://www.catb.org/jargon/chaff.html#stiffy
[280]: http://www.catb.org/jargon/chaff.html#short-card
[281]: http://www.catb.org/jargon/chaff.html#Silver-Book
[282]: http://www.catb.org/jargon/chaff.html#Devil-Book
[283]: http://www.catb.org/jargon/chaff.html#crayola-books
[284]: http://www.catb.org/jargon/chaff.html#four-two
[285]: http://www.catb.org/jargon/chaff.html#AI-koans
[286]: http://www.catb.org/jargon/chaff.html#Big-Gray-Wall
[287]: http://www.catb.org/jargon/chaff.html#Blue-Book
[288]: http://www.catb.org/jargon/chaff.html#Green-Book
[289]: http://www.catb.org/jargon/chaff.html#Red-Book
[290]: http://www.catb.org/jargon/chaff.html#White-Book
[291]: http://www.catb.org/jargon/chaff.html#BQS
[292]: http://www.catb.org/jargon/chaff.html#brochureware
[293]: http://www.catb.org/jargon/chaff.html#desk-check
[294]: http://www.catb.org/jargon/chaff.html#echo
[295]: http://www.catb.org/jargon/chaff.html#fd-leak
[296]: http://www.catb.org/jargon/chaff.html#g-file
[297]: http://www.catb.org/jargon/chaff.html#gag
[298]: http://www.catb.org/jargon/chaff.html#machinable
[299]: http://www.catb.org/jargon/chaff.html#lexiphage
[300]: http://www.catb.org/jargon/chaff.html#line-starve
[301]: http://www.catb.org/jargon/chaff.html#LPT
[302]: http://www.catb.org/jargon/chaff.html#PDL
[303]: http://www.catb.org/jargon/chaff.html#overflow-pdl
[304]: http://www.catb.org/jargon/chaff.html#pod
