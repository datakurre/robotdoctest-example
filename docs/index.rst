Example documentation
=====================

..  include:: _robot.rst

Getting started
---------------

..  figure:: _screenshots/pyconfi.png
..  code:: robotframework

    Show PyConFI

        Go to  http://fi.pycon.org/
        Page should contain  PyCon Finland
        Highlight  css=#news h1
        ${note1} =  Add note
        ...    css=#news h1
        ...    News are the most important thing.
        ...    width=120  position=right

        Highlight  jquery=h3:contains('Registration closed')
        ${note2} =  Add note
        ...    jquery=h3:contains('Registration closed')
        ...    It seems, it's too late now to make your mind.
        ...    width=120  position=right

        Capture page screenshot
        ...  _screenshots/pyconfi.png
