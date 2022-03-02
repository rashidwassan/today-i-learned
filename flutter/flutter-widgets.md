# This is the list of different Flutter widgets that I know about.
# Just a widget a day

## Animated CrossFade
A widget that cross-fades between two given children and animates itself between their sizes.

### Code Snippet
``` dart
AnimatedCrossFade(
  duration: const Duration(seconds: 3),
  firstChild: const FlutterLogo(style: FlutterLogoStyle.horizontal, size: 100.0),
  secondChild: const FlutterLogo(style: FlutterLogoStyle.stacked, size: 100.0),
  crossFadeState: _first ? CrossFadeState.showFirst : CrossFadeState.showSecond,
)
```

## AlertDialog
Dialog is the way to go if there is a lot of content to display on single page.
link: https://api.flutter.dev/flutter/material/AlertDialog-class.html

### Code Snippet
``` dart
Future<void> _showMyDialog() async {

  return showDialog<void>(
    context: context,
    barrierDismissible: false, // user must tap button!
    builder: (BuildContext context) {
      // returning alter dialog, there are other dialogs as well
      return AlertDialog(
        title: const Text('AlertDialog Title'),
        content: SingleChildScrollView(
          child: ListBody(
            children: const <Widget>[
              Text('This is a demo alert dialog.'),
              Text('Would you like to approve of this message?'),
            ],
          ),
        ),
        // These are the buttons that you want to show in that dialog.
        actions: <Widget>[
          TextButton(
            child: const Text('Approve'),
            onPressed: () {
              Navigator.of(context).pop();
            },
          ),
        ],
      );
    },
  );
}
```