# Task 2

Locate and fix technical bugs contained in translated messages contained in git repositories.

## Aim

This task aims to help participants gain advanced understanding of text markup and translation
file formats, as well as the open source quality check tools available for the file format.

DO NOT translate messages. That is not the objective of this task.

## WARNING

During the entire elimination phase, participants must not interact with a GitHub repository
that was selected by another participant for this task until after the other participant
has successfully completed this task.

## Find 10 bugs in a translation project

Bugs in translated messages include:

-  semantic problems, such as missing grammatical structure,
   like a missing period at the end of a sentence.

-  syntax errors, such as invariant parts of the source message
   that have been translated when they should not be translated.

There are existing open source tools that find and even fix
these problems automatically.  An example of an existing open source tool is
[`translate-toolkit`](https://en.wikipedia.org/wiki/Translate_Toolkit),
which is included in most Linux distributions.

On the repository wiki is a page "Existing tools", which has more
tools that may be useful.

It is recommended that you look for translation bugs in projects
that use a [Weblate](https://en.wikipedia.org/wiki/Weblate) service.
Weblate allows anyone to contribute translations that are
[lazy-committed](https://docs.weblate.org/en/latest/admin/continuous.html#lazy-commit)
to the repository.

If the weblate project is linked with a GitHub repository, the changes that are
made in the weblate service will appear on the GitHub profile of the person
who made the changes in weblate, *if* their email address in GitHub and weblate
are identical.

Some weblate services allow authentication using GitHub, which presets the
email address to be identical.

On the wiki is a page "Weblate" that contains more information about weblate
services.  Two of the largest weblate services containing many varied
projects connected to GitHub repositories are:

- https://hosted.weblate.org/ [projects](https://hosted.weblate.org/projects/)
- https://l10n.opensuse.org/ [projects](https://l10n.opensuse.org/projects/)

### Register your project

Only one participant may work on a GitHub repository at a time.
This is to avoid multiple conflicting changes.

Once you have found a project with technical bugs, first search `<x>`
to check if someone else has already chosen the same project.

If nobody else has already selected the project you found,
do `<x>` to register that you are working on the project.

If someone else has registered the repository, then you must
not choose it, or you will be eliminated.

## Fix 10 bugs

1. Fix the translation bugs in the repository
2. Give _star_ to the repo

If you do not find and fix the 10 problematic messages in
your first registered repository, you can choose another repository
and repeat it until you have successfully fixed 10 messages.
