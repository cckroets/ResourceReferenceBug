# ResourceReferenceBug
Displays bug where a resource can be referenced from another module where it shouldn't be accessible.

App Structure:
app depends on library1 and library2


@layout/library2_text_layout from library2 references @string/secret_library1_resource declared in library1

This referencing should not be possible and should fail the build. Even Android Studio is unable to resolve the references and highlights the reference in red. However we are able to still build and run the app as if the reference was valid.

