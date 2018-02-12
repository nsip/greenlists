# greenlists

The privacy work [NSIP](http://www.nsip.edu.au) is undertaking with [A4L](https://www.a4l.org) involves authorisation to view information at the element level, and not just the object level. Such authorisation for [SIF/XML](http://specification.sifassociation.org/Implementation/AU/) requires us to be able to specify individual XML elements as authorised for access; risk is minimised by specifying only those elements which a party is authorised to see (_whitelist, greenlist_), rather than specifying those they are not authorised to see (_blacklist, redlist_). 

The https://github.com/nsip/sif_privacy_controls_xslt repository exemplifies the technical approach taken to specify greenlists: a list of XPaths of the permitted elements is specified, and various filters can then be generated with that greenlist as input (including XSLT and XQuery).

The greenlist approach relies on authorising applications and users by role; but the domain of the authorised application also has a bearing on what objects and elements the application has a business need to view. We can establish at least a default notion that timetabling applications may need to access student names, but have no business need to access student visa information, for example. So the likely use cases that an application expects to service can also serve as inputs into what information they should be authorised to access.

To support use case-based authorisation, we are proposing some baseline greenlists. These artefacts are intended for discussion, and have not at this stage been vetted by any party.
