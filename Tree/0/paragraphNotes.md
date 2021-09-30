An Alternative to Endnotes, Footnotes, or Parenthetical Notes
=============================================================

The problem with endnotes is that they are at the end, far away from the context.

The problem with footnotes is that they are at the bottom of the page, far away from the context.

The problem with parenthetical notes is that they are (interrupting and) or can be distracting.

End-of-paragraph notes strike a balance.

By way of example
-----------------

> Rescheduling per John Does's request.
> If IT allows us to have a call-in number,
> according to this page,\* it will be available at some point.
> I suppose I could schedule a webex meeting for the same time,
> and we could use that for the audio.<br/>
> (_Notes_:&mdash;<br/>\* this page:
> "Add a dial-in number for a meeting in Teams"
> https://support.microsoft.com/en-us/office/add-a-dial-in-number-for-a-meeting-in-teams-7c33e972-e5a2-4b32-aabd-09c0c5f18424)

Description
-----------

After the main text of the paragraph, make a soft line break.
Within a parenthetical, write an indication that what follows are notes.
Then, for each note, make a soft line break, repeat the note symbol (e.g., \*), and write the note.
It may be helpful to the reader if the few words to which the note applies are repeated at the beginning of the note.

A BNF
-----

    <annotated text> ::= <text> <note symbol>
    ################################################################
    <tag> ::= <> | <some text that enables the reader to distinguish
    which note belongs to which part of the main text, which may be
    especially helpful if the same note symbol is used for all notes.>
    
    <annotation> ::= <soft-line-break> <note-symbol> <tag> <text>
    
    <annotations> ::= <annotation> | <annotations> <annotation>
    
    <paragraph-with-notes> ::= <start-of-paragraph> <annotated-text>
        <soft line break>
        ( <notes-heading> <soft line break>
        <annotations> )
