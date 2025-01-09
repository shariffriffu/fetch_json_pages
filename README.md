<!--
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/tools/pub/writing-package-pages).

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/to/develop-packages).
-->

Using this package you can directly render page using navigator.push , as input you have to pass json string as shown in the below example

## Features

TODO: List what your package can do. Maybe include images, gifs, or videos.

## Getting started

## Usage

TODO: Include short and useful examples for package users. Add longer examples
to `/example` folder.

```dart
String screen =
              await rootBundle.loadString('assets/json/screen.json');

navigatorKey.currentState?.push(MaterialPageRoute(
            builder: (context) =>
                renderingPage(jsonString: screen),
          ));
```

```json
<!-- assets/json/screen.json -->

{
    "type": "scaffold",
    "args": {
        "appBar": {
            "type": "app_bar",
            "args": {
                "title": {
                    "type": "text",
                    "args": {
                        "text": "Sign Up",
                        "style": {
                            "color": "#000000",
                            "fontWeight": "bold"
                        }
                    }
                },
                "backgroundColor": "#1569C7"
            }
        },
        "body": {
            "type": "single_child_scroll_view",
            "args": {
                "child": {
                    "type": "column",
                    "args": {
                        "children": [


                            {
                                "type": "container",
                                "args": {
                                    "padding": [
                                        20,
                                        20,
                                        20,
                                        20
                                    ],
                                    "child": {
                                        "type": "safe_area",
                                        "args": {
                                            "child": {
                                                "type": "form",
                                                "args": {
                                                    "child": {
                                                        "type": "column",
                                                        "args": {
                                                            "crossAxisAlignment": "center",
                                                            "mainAxisAlignment": "center",
                                                            "children": [
                                                                {
                                                                    "type": "row",
                                                                    "args": {
                                                                        "children": [
                                                                            {
                                                                                "type": "asset_image",
                                                                                "args": {
                                                                                    "height": 30,
                                                                                    "width": 30,
                                                                                    "name": "assets/images/Prefix_mobile.png"
                                                                                }
                                                                            },
                                                                            {
                                                                                "type": "sized_box",
                                                                                "args": {
                                                                                    "width": 10
                                                                                }
                                                                            },
                                                                            {
                                                                                "type": "expanded",
                                                                                "args": {
                                                                                    "child": {
                                                                                        "type": "stack",
                                                                                        "args": {
                                                                                            "children": [
                                                                                                {
                                                                                                    "type": "text_form_field",
                                                                                                    "id": "password",
                                                                                                    "args": {
                                                                                                        "keyboardType": "number",
                                                                                                        "controller": "${text1FieldController}",
                                                                                                        "obscureText": "true",
                                                                                                        "decoration": {
                                                                                                            "labelText": "Enter your PIN",
                                                                                                            "labelStyle": {
                                                                                                                "color": "#1569C7",
                                                                                                                "fontWeight": "bold",
                                                                                                                "fontSize": 15
                                                                                                            }
                                                                                                        }
                                                                                                    }
                                                                                                },
                                                                                                {
                                                                                                    "type": "positioned",
                                                                                                    "args": {
                                                                                                        "right": 0,
                                                                                                        "bottom": 10,
                                                                                                        "child": {
                                                                                                            "type": "row",
                                                                                                            "args": {
                                                                                                                "mainAxisSize": "min",
                                                                                                                "children": [
                                                                                                                    {
                                                                                                                        "type": "asset_image",
                                                                                                                        "args": {
                                                                                                                            "height": 30,
                                                                                                                            "width": 30,
                                                                                                                            "name": "assets/images/eyeon.png"
                                                                                                                        }
                                                                                                                    }
                                                                                                                ]
                                                                                                            }
                                                                                                        }
                                                                                                    }
                                                                                                }
                                                                                            ]
                                                                                        }
                                                                                    }
                                                                                }
                                                                            }
                                                                        ]
                                                                    }
                                                                },
                                                                {
                                                                    "type": "sized_box",
                                                                    "args": {
                                                                        "height": 40
                                                                    }
                                                                },
                                                                {
                                                                    "type": "elevated_button",
                                                                    "args": {
                                                                        "child": {
                                                                            "type": "text",
                                                                            "args": {
                                                                                "text": "Login",
                                                                                "style": {
                                                                                    "color": "#FFFFFF"
                                                                                }
                                                                            }
                                                                        },
                                                                        "style": {
                                                                            "backgroundColor": "#1569C7"
                                                                        },
                                                                        "onPressed": "${pin('form_context')}"
                                                                    }
                                                                }
                                                            ]
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        ]
                    }
                }
            }
        }
    }
}
```
