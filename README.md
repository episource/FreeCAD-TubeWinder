# FreeCAD Tube Winder
The tube winder is suitable for (PE) water tubes having a diameter up to
approx. 40mm. The winder should be used by two people for smaller tubes and
three people for larger tubes.

![TubeWinder Preview](TubeWinder.png)

## Parts

| Quantity | Type                             | Label      | Description                                                                                                                                   |
|----------|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 4        | AP3030S8                         | 42,00 mm   |                                                                                                                                               |
| 4        | AP3030S8                         | 400,00 mm  |                                                                                                                                               |
| 4        | AP3030S8                         | 427,46 mm  |                                                                                                                                               |
| 2        | AP3030S8                         | 450,00 mm  |                                                                                                                                               |
| 4        | AP3030S8                         | 560,00 mm  |                                                                                                                                               |
| 2        | AP3030S8                         | 1150,00 mm |                                                                                                                                               |
| 8        | AP3030S8_AngleConnector45        |            |                                                                                                                                               |
| 15       | AP3030S8_BracketSmall            |            |                                                                                                                                               |
| 16       | AP3030S8_Cap                     |            |                                                                                                                                               |
| 2        | AP3030S8_ConnectorSquare         |            |                                                                                                                                               |
| 9        | AP3030S8_InnerBracketWithScrews  |            | Inner bracket usually shipped including two set screws.                                                                                       |
| 2        | AP3030S8_Joint                   |            |                                                                                                                                               |
| 39       | AP3030S8_StoneM6Heavy            |            |                                                                                                                                               |
| 22       | AP3030S8_StoneM8Heavy            |            |                                                                                                                                               |
| 1        | AP3030S8_TNutM6                  |            |                                                                                                                                               |
| 6        | KnuckleFoot_M8x50                |            |                                                                                                                                               |
| 1        | Nomis_C-Clamp_WithMod            |            | Spigot removed. Two additional 6,5mm holes need to be drilled. Availble via Amazon or ebay, look for "NOMIS C-Klemme mit Spigot".             |
| 1        | Screw/Bolt ISO4762               | M6x12      |                                                                                                                                               |
| 4        | Screw/Bolt ISO4762               | M8x25      |                                                                                                                                               |
| 8        | Screw/Bolt ISO7380-1             | M8x12      |                                                                                                                                               |
| 8        | Screw/Bolt ISO7380-1             | M8x25      |                                                                                                                                               |
| 39       | Screw/Bolt ISO7380-2             | M6x12      |                                                                                                                                               |
| 8        | Screw/Bolt ISO7380-2             | M8x10      |                                                                                                                                               |
| 1        | SwivelPlate_WeihuaC16049_156x156 |            | Hole with diameter 8,5mm-9mm (M8) needs to be drilled at end of slot holes. Available via Amazon, search for "Drehteller für TDS Bootssitz". |

## Compatibility
Prerelease builds of FreeCAD have been used to create the models. Therefore,
incompatibilities with older or newer FreeCAD builds might occur. The following
software builds haven been used and are known to be compatible:
 - [FreeCAD v0.19.21329](https://www.freecadweb.org/downloads.php)
 - [Assembly4 Workbench v0.9.0](https://github.com/Zolko-123/FreeCAD_Assembly4)
 
Partial loading of linked files should be disabled. If not, some files need to
be reloaded manually to fix some glitches.
 
Content created with the TechDraw workbench might seem broken (content shifted
out of the drawing area) when first viewed after loading the file. If so, switch
to 3D view and then back to the TechDraw content or right click the TechDraw
document in tree view to fix the layout issues.

Before commiting to this repository, [_setup.sh](_setup.sh) should be run to
setup a [git smudge filter](https://www.git-scm.com/docs/gitattributes#_filter),
that decompresses `FCStd` files during commit: `FCStd` files are zip compressed
archives of mostly `xml` formatted plaintext files. Git's delta compression
works very well for xml files, but not if compressed. For security reasons, the
filter needs to be configured explicitly. Therefore, it cannot be shared in a
way that does need user interaction. Decompressing is done using compression
level `store` which preserves full FreeCAD compatibility. A clean filter is not
used, therefore files in working tree are slightly bigger after checkout
compared with the initial file size.