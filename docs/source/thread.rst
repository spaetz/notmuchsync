Constants: :class:`Opcode` & :class:`Type`
==========================================

.. currentmodule:: DNS

:class:`Opcode` -- Query opcode
------------------------------------------
.. class:: Opcode

      Constants of the Opcode module represent DNS query opcodes. 
      Some of the opcodes are described in 
      `RFC 1035 <http://www.ietf.org/rfc/rfc1035.txt>`_. 
      The following constants are defined:
      **QUERY**, **IQUERY**, **STATUS**, **NOTIFY**, **UPDATE**.

      The standard query is for example Opcode.QUERY.


:class:`Type` -- Query type
------------------------------------------

.. class:: Type

      Constants of the Type module represent DNS query types. 
      The following constants are defined:

      .. data:: A

         a host address

      .. data:: NS

         an authoritative name server

      .. data:: MD

         a mail destination (Obsolete - use MX)

      .. data:: MF

         a mail forwarder (Obsolete - use MX)

      .. data:: CNAME

         the canonical name for an alias

      .. data:: SOA

         marks the start of a zone of authority

      .. data:: MB

         mailbox domain name (EXPERIMENTAL)

      .. data:: MG

         mail group member (EXPERIMENTAL)

      .. data:: MR

         mail rename domain name (EXPERIMENTAL)

      .. data:: NULL

         null RR (EXPERIMENTAL)

      .. data:: WKS

         well known service description

PTR = 12        # a domain name pointer
HINFO = 13      # host information
MINFO = 14      # mailbox or mail list information
MX = 15         # mail exchange
TXT = 16        # text strings
AAAA = 28       # IPv6 AAAA records (RFC 1886)
SRV = 33        # DNS RR for specifying the location of services (RFC 2782)
UNAME = 110
MP = 240
AXFR = 252      # A request for a transfer of an entire zone
MAILB = 253     # A request for mailbox-related records (MB, MG or MR)
MAILA = 254     # A request for mail agent RRs (Obsolete - see MX)
ANY = 255       # A request for all records
