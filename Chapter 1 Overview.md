# Chapter 1 : Overview

## Review Questions

**Q.1** What is the OSI security architecture?

**Answer:** The [OSI Security Architecture](https://www.itu.int/rec/dologin_pub.asp?lang=e&id=T-REC-X.800-199103-I!!PDF-E) is a framework that provides a systematic approach to defining the requirements for security and characterizing the approaches to satisfying those requirements. The OSI security architecture focuses on security attacks, mechanisms, services and the relationships among these categories. These can be defined briefly as

- **Security attack:** Any action that compromises the security of information owned by an organization.
- **Security mechanism:** A process (or a device incorporating such a process) that is designed to detect, prevent, or recover from a security attack.
- **Security service:** A processing or communication service that enhances the security of the data processing systems and the information transfers of an organization. The services are intended to counter security attacks, and they make use of one or more security mechanisms to provide the service.

**Q.2** What is the difference between passive and active security threats?

**Answer:** The following table shows the difference between passive & active attacks.

|             Passive Attacks              |              Active Attacks              |
| :--------------------------------------: | :--------------------------------------: |
| Passive attacks involve eavesdropping on, or monitoring of, transmissions. | Active attacks involve some modification of the data stream or the creation of a false stream. |
| The goal of the attacker is to obtain information that is being transmitted. | The goals of attacker include the modification of transmitted data and attempts to gain unauthorizedaccess to computer systems. |
| There are two types of passive attacks:                       release of message contents and traffic analysis. | There are four categories of active attacks:                masquerade, replay, modification and denial-of service |
|    Hard to detect & easy to prevent.     |    Easy to detect & hard to prevent.     |
| **Example**: learning the content of telephone conversation or email message. | **Example**: making services unavailable to legitimate users. |

**Q.3** List and briefly define categories of passive and active security attacks.

Following are the categories of ***active attacks***.

1. **Masquerade**: A masquerade takes place when one entity pretends to be a different entity. A masquerade attack usually includes one of the other forms of active attack. For example, authentication sequences can be captured and replayed after a  valid authentication sequence has taken place, thus enabling an authorized entity with few privileges to obtain extra privileges by impersonating an entity that has those privileges.
2. **Replay**: Replay involves the passive capture of a data unit and its subsequent retransmission to produce an unauthorized effect.
3. **Modification**:Modification of messages simply means that some portion of a legitimate message is altered, or that messages are delayed or reordered, to produce an unauthorized effect. For example, a message meaning “Allow Sanket  to read confidential file accounts” is modified to mean “Allow Pradip to read confidential file accounts.”
4. **Denial-of-Service**: The denial of service prevents or inhibits the normal use or management of communications facilities . This attack may have a specific target; for example, an entity may suppress all messages directed to a particular destination(e.g., the security audit service). Another form of service denial is the disruption of an
   entire network, either by disabling the network or by overloading it with messages so as to degrade performance.

Following are the categories of ***passive attacks***.

1. **Release of Message Contents** : The release of message contents encompasses a telephone conversation, an electronic mail message, and a transferred file that may contain sensitive or confidential information.We would like to prevent an attacker from learning the contents of these transmissions.
2. **Traffic Analysis** : A second type of passive attack, traffic analysis, is subtler.Suppose that we had a way of masking the contents of messages or other information traffic so that attackers, even if they captured the message, could not extract the information from the message. The common technique for masking contents is *encryption*. If we had encryption protection in place, an opponent might still be able to observe the pattern of these  messages. The opponent could determine the location and identity of communicating hosts and could observe  the frequency and length of messages being exchanged. This information might be useful in guessing the nature of the communication that was taking place.

**Q.4** List and briefly define categories of security services.

Following are the categories of security services.

1. **Authentication**: The assurance that the communicating entity is the one that it claims to be.
   - **Peer Entity Authentication**:Used in association with a logical connection to provide confidence in the identity of the entities connected.
   - **Data Origin Authentication**: In a connectionless transfer, provides assurance that the source of received data is same as claimed.


2. **Access Control**: The prevention of unauthorized use of a resource (this service controls who can have access to a resource, under what conditions access can occur, and what those accessing the resource are allowed to do).

3. **Data Confidentiality**: The protection of data from unauthorized disclosure.
   - **Connection Confidentiality**: The protection of all user data on a connection.
   - **Connectionless Confidentiality**: The protection of all user data in a single data block
   - **Selective-Field Confidentiality**: The confidentiality of selected fields within the user data on a connection or in a single data block.
   - **Traffic-Flow Confidentiality**: The protection of the information that might be derived from observation of traffic flows.

4. **Data Integrity**:The assurance that data received are exactly as sent by an authorized entity (i.e., contain no modification, insertion, deletion, or replay).

   - **Connection Integrity with Recovery:**Provides for the integrity of all user data on a connection and detects any modification, insertion, deletion, or replay of any data within an entire data sequence, with recovery attempted.

   - **Connection Integrity without Recovery**:As above, but provides only detection without recovery.

   - **Selective-Field Connection Integrity**: Provides for the integrity of selected fields within the user data of a data block transferred over a connection and takes the form of determination of whether the selected fields have been modified, inserted, deleted, or replayed.

   - **Connectionless Integrity**: Provides for the integrity of a single connectionless data block and may take the form of detection of data modification. Additionally, a limited form of replay detection may be provided.

   - **Selective-Field Connectionless Integrity**:Provides for the integrity of selected fields within a single connectionless data block; takes the form of  determination of whether the selected fields have been modified.

     ​

5. **Nonrepudiation**: Provides protection against denial by one of the entities involved in a communication of having participated in all or part of the communication.
   - **Nonrepudiation, Origin**: Proof that the message was sent by the specified party.
   - **Nonrepudiation, Destination**: Proof that the message was received by the specified party.

**Q.5** List and briefly define categories of security mechanisms.

Following are the categories of security mechanisms:

1. **Specific Security Mechanisms**:May be incorporated into the appropriate protocol layer in order to provide some of the OSI security services.

      - **Encipherment:**The use of mathematical algorithms to transform data into a form that is not readily intelligible.The
        transformation and subsequent recovery of the data depend on an algorithm and zero or more encryption keys.
      - **Digital Signature**: Data appended to, or a cryptographic transformation of, a data unit that allows a recipient of the data unit to prove the source and integrity of the data unit and protect against forgery (e.g., by the recipient).
      - **Access Control**: A variety of mechanisms that enforce access rights to resources. 
      - **Data Integrity**: A variety of mechanisms used to assure the integrity of a data unit or stream of data units.
      - **Authentication Exchange**: A mechanism intended to ensure the identity of an entity by means of information exchange.
      - **Traffic Padding**: The insertion of bits into gaps in a data stream to frustrate traffic analysis attempts.
      - **Routing Control**: Enables selection of particular physically secure routes for certain data and allows routing changes,
        especially when a breach of security is suspected.
      - **Notarization**: The use of a trusted third party to assure certain properties of a data exchange.

2. **Pervasive Security Mechanism**: Mechanism that are not specific to any particular OSI security service or protocol layer.
      - **Trusted Functionality**: That which is perceived to be correct with respect to some criteria (e.g., as established by a security policy).
      - **Security Label**: The marking bound to a resource (which may be a data unit) that names or designates the security
        attributes of that resource.
      - **Event Detection**: Detection of security-relevant events.
      - **Security Audit Trail**: Data collected and potentially used to facilitate a security audit, which is an independent review and examination of system records and activities.
      - **Security Recovery**: Deals with requests from mechanisms, such as event handling and management functions, and takes recovery actions.

