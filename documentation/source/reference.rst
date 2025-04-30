**************************
The MIME library reference
**************************

.. current-library:: mime

The MIME module
***************

.. current-module:: mime

.. constant:: $default-mime-type-map

.. class:: <invalid-mime-type-error>
   :open:

   :superclasses: :class:`<mime-error>`

.. class:: <mime-error>
   :open:

   :superclasses: `<format-string-condition>`, :drm:`<error>`

.. class:: <mime-type-map>
   :open:

   :superclasses: :drm:`<table>`

.. class:: <mime-type>
   :open:

   :superclasses: :drm:`<object>`

   :keyword required subtype: An instance of :drm:`<byte-string>`.
   :keyword required type: An instance of :drm:`<byte-string>`.

.. generic-function:: extension-to-mime-type
   :open:

   :signature: extension-to-mime-type (extension type-map) => (mt)

   :parameter extension: An instance of :drm:`<string>`.
   :parameter type-map: An instance of :class:`<mime-type-map>`.
   :value mt: An instance of ``false-or(<mime-type>)``.

.. method:: extension-to-mime-type
   :specializer: <byte-string>, <mime-type-map>

.. generic-function:: extension-to-mime-type-setter
   :open:

   :signature: extension-to-mime-type-setter (mt extension type-map) => (mt)

   :parameter mt: An instance of :class:`<mime-type>`.
   :parameter extension: An instance of :drm:`<string>`.
   :parameter type-map: An instance of :class:`<mime-type-map>`.
   :value mt: An instance of :class:`<mime-type>`.

.. method:: extension-to-mime-type-setter
   :specializer: <mime-type>, <byte-string>, <mime-type-map>

.. generic-function:: load-mime-types
   :open:

   :signature: load-mime-types (type-map pathname) => ()

   :parameter type-map: An instance of :class:`<mime-type-map>`.
   :parameter pathname: An instance of ``<pathname>``.

.. method:: load-mime-types
   :specializer: <mime-type-map>, <pathname>

.. generic-function:: mime-name
   :open:

   :signature: mime-name (mt) => (name)

   :parameter mt: An instance of :class:`<mime-type>`.
   :value name: An instance of :drm:`<byte-string>`.

.. method:: mime-name
   :specializer: {<mime-type> in mime}

.. generic-function:: mime-subtype
   :open:

   :signature: mime-subtype (mt) => (subtype)

   :parameter mt: An instance of :class:`<mime-type>`.
   :value subtype: An instance of :drm:`<byte-string>`.

.. method:: mime-subtype
   :specializer: {<mime-type> in mime}

.. generic-function:: mime-type
   :open:

   :signature: mime-type (mt) => (type)

   :parameter mt: An instance of :class:`<mime-type>`.
   :value type: An instance of :drm:`<byte-string>`.

.. method:: mime-type
   :specializer: {<mime-type> in mime}

.. generic-function:: mime-type-to-string

   :signature: mime-type-to-string (mtype) => (string)

   :parameter mtype: An instance of :class:`<mime-type>`.
   :value string: An instance of :drm:`<byte-string>`.

.. generic-function:: string-to-mime-type

   :signature: string-to-mime-type (string #key class) => (mime-type)

   :parameter string: An instance of :drm:`<string>`.
   :parameter #key class: An instance of ``subclass(<mime-type>)``.
   :value mime-type: An instance of :class:`<mime-type>`.
