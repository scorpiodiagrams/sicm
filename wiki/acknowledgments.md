!!Polyglot
## Acknowledgments

#### Acknowledgments
We would like to thank the many people who have helped us to develop this book and the curriculum it is designed to support. We have had substantial help from the wonderful students who studied with us in our classical mechanics class. They have forced us to be clear; they have found bugs that we had to fix in the software, in the presentation, and in our thinking.

We have had considerable technical help in the development and presentation of the subject matter from Harold Abelson. Abelson is one of the developers of the Scmutils software system. He put mighty effort into some sections of the code. We also consulted him when we were desperately trying to understand the logic of mechanics. He often could propose a direction to lead out of an intellectual maze.

Matthew Halfant started us on the development of the Scmutils system. He encouraged us to get into scientific computation, using Scheme and functional style as an active way to explain the ideas, without the distractions of imperative languages such as C. In the 1980s he wrote some of the early Scheme procedures for numerical computation that we still use.

Dan Zuras helped us with the invention of the unique organization of the Scmutils system. It is because of his insight that the system is organized around a generic extension of the chain rule for taking derivatives. He also helped in the heavy lifting that was required to make a really good polynomial GCD algorithm, based on ideas we learned from Richard Zippel.

This book, and a great deal of other work of our laboratory, could not have been done without the outstanding work of Chris Hanson. Chris developed and maintained the Scheme system underlying this work. More recently, Taylor Campbell and others have continued the development of MIT#/GNU Scheme. In addition, Chris took us through a pass of reorganization of the Scmutils system that forced the clarification of many of the ideas of types and of generic operations that make our system as good as it is.
#page(xx)
Guillermo Juan Rozas, co-developer of the Scheme system, made major contributions to the Scheme compiler, and implemented a number of other arcane mechanisms that make our system efficient enough to support our work.

Besides contributing to some of the methods for the solution of linear equations in the Scmutils system, Jacob Katzenelson provided valuable feedback that improved the presentation of the material.

Julie Sussman, PPA, provided careful reading and serious criticism that forced us to reorganize and rewrite major parts of the text. Julie worked with first-edition coauthor Meinhard (Hardy) Mayer to create the index. She also developed and maintained Gerald Jay Sussman over these many years.

Cecile Wisdom, saint, is a constant reminder, by her faith and example, of what is really important. This project would not have been possible without the loving support and unfailing encouragement she has given Jack Wisdom. Their children, William, Edward, Thomas, John, and Elizabeth Wisdom, daily enrich his life with theirs.

Many have contributed to our understanding of dynamics over the years. Boris Chirikov, Michel Hénon, Peter Goldreich, and Stan Peale have had particular influence. We also acknowledge the influence of the late Res Jost.

Numerous others have contributed to this work, either in the development of the software or in the development of the content, including Bill Siebert, Panayotis Skordos, Kleanthes Koniaris, Kevin Lin, James McBride, Rebecca Frankel, Thomas F. Knight, Pawan Kumar, Elizabeth Bradley, Alice Seckel, Jihad Touma, and Kenneth Yip. We have had extremely useful feedback from and discussions with Piet Hut, Jon Doyle, David Finkelstein, Peter Fisher, Guy Lewis Steele Jr., and Robert Hermann.

We want to thank the generations of students who have taken our classes and worked through our problems. They have provided exceptional feedback and encouragement. Our students Will Farr, Mark Tobenkin, Keith Winstein, Alexey Radul, Micah Brodsky, Damon Vander Lind, Peter Iannucci, William Throwe, and Leo Stein were especially helpful.

We thank the MIT Computer Science and Artificial Intelligence Laboratory for its hospitality and logistical support. We acknowledge the Panasonic Corporation for support of Gerald Jay Sussman through an endowed chair. We thank Breene M. Kerr for
#page(pxxi)
support of Jack Wisdom through an endowed chair. We thank the MIT Mathematics and EECS departments for sabbatical support for Meinhard Mayer, who collaborated with us on the first edition. We are sad to report that Hardy is no longer with us. We sorely miss him.

#page(xxii) 