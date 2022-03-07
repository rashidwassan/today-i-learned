# MultiProvider

Multiprovider is a solution for combining multilpe providers in a much cleaner way. It merges multiple providers in single linear widget tree.
Suppose you are sending some data to child widget, but want to pass another data coming from another provider, multiProvider comes in handy in this situation.
Makes code easier to read.
- Last provider in the list of multiprovider will be used by default (if multiple providers are providing same type of value).

``` dart

MultiProvider(
  providers: [
    Provider<Something>(create: (_) => Something()),
    Provider<SomethingElse>(create: (_) => SomethingElse()),
    Provider<AnotherThing>(create: (_) => AnotherThing()),
  ],
  child: someWidget,
)

```