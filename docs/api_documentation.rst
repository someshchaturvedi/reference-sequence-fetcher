*****************
API Documentation
*****************
.. class:: Fetcher(base_url)

    Act as a factory class for sequence and metadata

    :param base_url: Base url of the server from which data to be fetched
    :type base_url: string

    .. py:method:: get_base_url()

        Return base_url of the Fetcher object

        :rtype: string

    .. py:method:: set_base_url(base_url)

        Set base_url of the Fetcher object. Used to change the base url of already instantiated object on the fly.

        :param base_url: Base url of the server from which data to be fetched
        :type base_url: string

        :rtype: void

    .. py:method:: fetch_info()

        Returns the service information of the server being queried

        :rtype: dict

    .. py:method:: fetch_sequence(checksum, [start=None, end=None])

        Act as factory method for retrieving sequences

        :param checksum: Checksum identifier of the sequence to be retrieved
        :type checksum: string

        :param start: Used to define start location of the sequence to be retrieved (inclusive)
        :type start: integer

        :param end: Used to define end location of the sequence to be retrieved (exclusive)
        :type end: integer

        :rtype: string

    .. py:method:: fetch_metadata(checksum)

        Act as factory method for retrieving sequences

        param checksum: Checksum identifier of the sequence to be retrieved
        :type checksum: string

        :rtype: dict

    .. py:classmethod:: info(base_url)

        A class method for easily fetching single service info without creating Fetcher object.

        :rtype: dict

    .. py:classmethod:: sequence(base_url, checksum, [start=None, end=None])

        A class method for easily fetching single sequence without creating Fetcher object.
        Parameters definitions as per defined above

        :rtype: string

    .. py:classmethod:: metdata(base_url, checksum)

        A class method for easily fetching single metadata without creating Fetcher object.
        Parameters definitions as per defined above

        :rtype: dict
