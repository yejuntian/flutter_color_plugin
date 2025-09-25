### flutter_color_plugin2

// Usage hex from string and alternative color systems

HexColor('000000')                 // -> Color(0xFF000000)
HslColor(164, 100, 88)             // -> Color(0xFFC2FFEF)
XyzColor(0.1669, 0.2293, 0.0434)   // -> Color(0xFF659027)
CielabColor(36.80, 55.20, -95.61)  // -> Color(0xFF4832F7)

// Make color darker or lighter
Color(0xFF000000).lighter(100)     // -> Color(0xFFFFFFFF)
Color(0xFF000000).darker(50)       // -> Color(0xFF808080)

// Mix with other colors
Color(0xFFFF0000).mix(Color(0xFF00FF00), .25) // -> Color(0xFFBF3F00)

// Colors conversion
Color.fromRGBO(255, 255, 255, 1).hexColor // -> '#FFFFFFFF'

## Getting started

dependencies:
flutter_color_plugin: any

## Usage

// HexColor
assert(HexColor('000000')    == Color(0xFF000000));
assert(HexColor('#000000')   == Color(0xFF000000));
assert(HexColor('FFFFFFFF')  == Color(0xFFFFFFFF));
assert(HexColor('#B1000000') == Color(0xB1000000));
assert(HexColor('#B1000000').hexColor, '#B1000000');

// HslColor
assert(HslColor(164, 100, 88) == Color(0xFFC2FFEF));

// HyzColor
assert(XyzColor(0.1669, 0.2293, 0.0434) == Color(0xFF659027));

/// CielabColor
assert(CielabColor(36.80, 55.20, -95.61) == Color(0xFF4832F7));

### Make color darker or lighter

// [black -> white] lighter by 100 percents
assert(Color(0xFF000000).lighter(100), Color(0xFFFFFFFF));
// Another lighter example
assert(Color.fromARGB(255, 64, 64, 64).lighter(50), Color.fromARGB(255, 192, 192, 192));

// [white -> grey] darker by 50 percents
assert(Color(0xFF000000).darker(50), Color(0xFF808080));
// Another darker example
assert(Color.fromARGB(255, 192, 192, 192).darker(25), Color.fromARGB(255, 128, 128, 128));