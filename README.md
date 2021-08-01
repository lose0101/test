
[![Join the chat at https://gitter.im/lose0101/test](https://badges.gitter.im/lose0101/test.svg)](https://gitter.im/lose0101/test?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Sends a POST request. Returns :class:`Response` object.

        :param url: URL for the new :class:`Request` object.
        :param data: (optional) Dictionary, bytes, or file-like object to send in the body of the :class:`Request`.
        :param json: (optional) json to send in the body of the :class:`Request`.
        :param \*\*kwargs: Optional arguments that ``request`` takes.
        :rtype: requests.Response
