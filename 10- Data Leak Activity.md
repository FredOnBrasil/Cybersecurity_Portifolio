# Data Leak Worksheet

## Incident Summary

A sales manager shared access to a folder of internal-only documents with their team during a meeting. [cite: 1, 2] The folder contained files associated with a new product that has not been publicly announced. [cite: 2, 3] It also included customer analytics and promotional materials. [cite: 3] After the meeting, the manager did not revoke access to the internal folder, but warned the team to wait for approval before sharing the promotional materials with others. [cite: 3, 4]

During a video call with a business partner, a member of the sales team forgot the warning from their manager. [cite: 4, 5, 6] The sales representative intended to share a link to the promotional materials so that the business partner could circulate the materials to their customers. [cite: 5, 6, 7] However, the sales representative accidentally shared a link to the internal folder instead. [cite: 5, 6, 7] Later, the business partner posted the link on their company's social media page assuming that it was the promotional materials. [cite: 6, 7]

## Control: Least Privilege

| Control            | Least privilege          |  
| :------- | :---------------- |
| Issue(s) | **What factors contributed to the information leak?** The manager's failure to revoke folder access and the representative's accidental sharing of the entire folder instead of just marketing materials led to the leak. This was compounded by the business partner's subsequent social media post.|
| Review | **What does NIST SP 800-53: AC-6 address?** addresses providing only the minimum necessary access to users to perform their tasks. It emphasizes enforcing processes, user accounts, and roles to achieve least privilege.|
| Recommendation | **How might the principle of least privilege be improved at the company?** Implement role-based access to restrict access to sensitive resources and automatically revoke access after a defined period.|
| Justification | **How might these improvements address the issues?** Role-based access would prevent unauthorized access to internal documents, and automatic revocation would reduce the risk of lingering access rights 1 . These measures enforce least privilege and limit the scope of potential leaks.|

# Security plan snapshot

The NIST Cybersecurity Framework (CSF) uses a hierarchical, tree-like structure to organize information. [cite: 9, 10] From left to right, it describes a broad security function, then becomes more specific as it branches out to a category, subcategory, and individual security controls. [cite: 9, 10]

| Function | Category          | Subcategory                       | Reference(s)           |
| :------- | :---------------- | :-------------------------------- | :--------------------- |
| Protect  | PR.DS: Data security | PR.DS-5: Protections against data leaks. | NIST SP 800-53: AC-6 |

In this example, the implemented controls that are used by the manufacturer to protect against data leaks are defined in NIST SP 800-53—a set of guidelines for securing the privacy of information systems. [cite: 11, 12, 13, 14, 15] Note: References are commonly hyperlinked to the guidelines or regulations they relate to. [cite: 11, 12, 13, 14, 15] This makes it easy to learn more about how a particular control should be implemented. [cite: 13, 14, 15] It's common to find multiple links to different sources in the references columns. [cite: 13, 14, 15]

## NIST SP 800-53: AC-6

NIST developed SP 800-53 to provide businesses with a customizable information privacy plan. [cite: 16, 17, 18, 19, 20, 21, 22] It's a comprehensive resource that describes a wide range of control categories. [cite: 16, 17, 18, 19, 20, 21, 22] Each control provides a few key pieces of information:

* Control: A definition of the security control. [cite: 18, 19, 20, 21, 22]
* Discussion: A description of how the control should be implemented. [cite: 18, 19, 20, 21, 22]
* Control enhancements: A list of suggestions to improve the effectiveness of the control. [cite: 18, 19, 20, 21, 22]
