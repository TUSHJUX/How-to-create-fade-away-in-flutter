# How-to-create-fade-away-in-flutter

import 'package:flutter/material.dart';
import 'package:transparent_image/transparent_image.dart';

class LFadeInImage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Container(
      child: Column(
        children: <Widget>[
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Text("Image from Network"),
          ),
          FadeInImage.memoryNetwork(
            placeholder: kTransparentImage,
            height: MediaQuery.of(context).size.height / 3,
            fadeInDuration: Duration(seconds: 2),
            image:
                'https://miro.medium.com/max/3200/1*mMJ3IvaAuMAmqjtyistCog.png',
          ),
          FadeInImage.assetNetwork(
            height: MediaQuery.of(context).size.height / 3,
            fadeInDuration: Duration(seconds: 5),
            fadeInCurve: Curves.bounceIn,
            image:
                'https://miro.medium.com/max/3200/1*mMJ3IvaAuMAmqjtyistCog.png',
            placeholder: 'image/loading.gif',
          ),
        ],
      ),
    );
  }
}

/*
**********
**********
**********
**********
*** END***
**********
**********
**********
**********
 */
