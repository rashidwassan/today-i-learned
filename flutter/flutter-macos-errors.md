# Error: CocoaPods's specs repository is too out-of-date to satisfy dependencies. To update the CocoaPods specs, run: pod repo update

## Sol:

```
It can be solved by executing the following commands in the terminal.

1: Go to /ios folder inside your Project.

2: Delete Podfile.lock (YourPoject/ios/Podfile.lock)

For Intel chip users
Run pod install --repo-update (Make sure your cd into the iOS directory of the flutter app)

For M1 chip Users
install ffi first (if not) In regular terminal using command: sudo arch -x86_64 gem install ffi then arch -x86_64 pod install --repo-update
Run flutter clean

Once complete, rebuild your Flutter application: flutter run

P.S - If you have done all the process the first time and it still doesn't get resolved your issue. then run this command pod repo remove trunk after step 2. thanks @drpawelo for identified this
```