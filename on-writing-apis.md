# On Writing APIs

## A release means you are ready to go

Everyone has bugs. If you are going to tag a version and make it a release,
you are telling the world that it's ready to go. The only person with the hand
on the release-trigger is the maintainer. If it's not ready, don't do it.

## The developer is the end user. You are providing the user interface

When writing an API, you should refer to the programmers using it as "your
users" and the thing you provide as "your interface". All of the rules of
designing an intuitive consistent end product still apply when providing a
documented interface for fellow programmers.

## Don't do things pre-emptively or frivolously

When designing something that people will use, you can either put things in
liberally and then have no qualms about breaking things a few weeks later, put
things in liberally and then feel the terrible burden of support, or create a
wall between supported (conservative) things and unsupported (liberal) things.

The last option is the only sensible one if you anticipate on supporting a
large number of users.

## You are providing a tool

Developers are utilizing your tool to solve a problem, not deal with a bunch
of new ones presented by the presumptions or constraints of the technology.
There is no merit to providing a solution that takes just as long to implement
due to obtuse design then it would to do directly. You are effectively burning
your user base every time you do this.

The worst thing you can do is make your users think they've made a mistake
after sinking significant time and effort and then either holding their nose
as they try to just "make it work", or worse, abandon their efforts entirely
and think terrible thoughts about you.

## Conclusion

Nobody builds things to make enemies. We're in this to help people. We write
APIs for people to make better software -- not waste their time unraveling our
implementation to finish theirs. The whole point is to remove a problem, not
create new ones. Exhausting time, effort, and mind-share due to poor release
management is a terrible shame.

Their are real people behind every project and we must never forget that. It's
easy to remove the human from the experience and think evil malevolent
thoughts as you sip that third cup of coffee trying to get that thing done
that _should have been 15 seconds_.

We must do better.
