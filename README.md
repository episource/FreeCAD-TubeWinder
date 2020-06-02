# FreeCAD Tube Winder
The tube winder is suitable for (PE) water tubes having a diameter up to
approx. 40mm. The winder should be used by two people for smaller tubes and
three people for larger tubes.

![TubeWinder Preview](TubeWinder.png)

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