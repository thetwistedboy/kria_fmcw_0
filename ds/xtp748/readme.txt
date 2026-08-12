*************************************************************************

© Copyright 2022–2024 Advanced Micro Devices, Inc. AMD, the AMD Arrow logo, 
Kria, Vivado, Zynq, and combinations thereof are trademarks of Advanced 
Micro Devices, Inc. Other product names used in this publication are for 
identification purposes only and may be trademarks of their respective
companies.

*************************************************************************

Vendor: AMD
Reference Design Version: 1.3
readme.txt Version: 1.3
Date Last Modified: 03JUL2024
Date Created: 06JUL2022
Associated Filename: xtp748-kria-som-schematic-review-checklist.zip

Supported Device(s): Kria SOM
Purpose: This ZIP file contains the Kria SOM schematic review checklist
Document Reference: XTP748
   
*************************************************************************

Disclaimer:

The information presented in this document is for informational purposes 
only and may contain technical inaccuracies, omissions, and typographical 
errors. The information contained herein is subject to change and may be 
rendered inaccurate for many reasons, including but not limited to product 
and roadmap changes, component and motherboard version changes, new model 
and/or product releases, product differences between differing 
manufacturers, software changes, BIOS flashes, firmware upgrades, or the 
like. Any computer system has risks of security vulnerabilities that cannot 
be completely prevented or mitigated. AMD assumes no obligation to update 
or otherwise correct or revise this information. However, AMD reserves the 
right to revise this information and to make changes from time to time to 
the content hereof without obligation of AMD to notify any person of such 
revisions or changes. THIS INFORMATION IS PROVIDED "AS IS." AMD MAKES NO 
REPRESENTATIONS OR WARRANTIES WITH RESPECT TO THE CONTENTS HEREOF AND 
ASSUMES NO RESPONSIBILITY FOR ANY INACCURACIES, ERRORS, OR OMISSIONS THAT 
MAY APPEAR IN THIS INFORMATION. AMD SPECIFICALLY DISCLAIMS ANY IMPLIED 
WARRANTIES OF NON-INFRINGEMENT, MERCHANTABILITY, OR FITNESS FOR ANY 
PARTICULAR PURPOSE. IN NO EVENT WILL AMD BE LIABLE TO ANY PERSON FOR ANY 
RELIANCE, DIRECT, INDIRECT, SPECIAL, OR OTHER CONSEQUENTIAL DAMAGES ARISING 
FROM THE USE OF ANY INFORMATION CONTAINED HEREIN, EVEN IF AMD IS EXPRESSLY 
ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

Critical Applications:

AMD products are not designed or intended to be fail-safe, or 
for use in any application requiring fail-safe performance, such as 
life-support or safety devices or systems, Class III medical 
devices, nuclear facilities, applications related to the deployment 
of airbags, or any other applications that could lead to death, 
personal injury, or severe property or environmental damage 
(individually and collectively, "Critical Applications"). Customer 
assumes the sole risk and liability of any use of AMD products 
in Critical Applications, subject only to applicable laws and 
regulations governing limitations on product liability.

THIS COPYRIGHT NOTICE AND DISCLAIMER MUST BE RETAINED AS PART OF THIS 
FILE AT ALL TIMES.

*************************************************************************

This readme file contains the following sections:

1. Revision History
2. Operating Instructions

*************************************************************************
1. Revision History 
*************************************************************************
Date		Version			Revision

12JUL2022	1.0			Initial release.

27JUN2023	1.1			Added K24 SOM
					Corrected reference name for PWROFF_C2M_L
					Corrected reference name for SCL and SDA
					Updated connector decoupling recommendations
					Changed power rail current ratings from minimum to maximum
09JAN2024	1.2			Corrected Additional Information for GTR_DP pins
					Updated VRP & DCI IO Standards
					Added status summary
03JUL2024	1.3			Added note about combining rails for VCCO_HDA
					Removed statement that PS_ERROR_OUT_M2C and PS_ERROR_STATUS_M2C are pulled up through a resistor
					Added note for PMU interface on MIO35 regarding WD monitor
					
*************************************************************************
2. Operating Instructions 
*************************************************************************

!	Macros must be enabled for full functionality.

1.	This spreadsheet is intended to provide a list of what has been checked (and what has not been checked) during a customer schematic review. It is not intended to be a comprehensive checklist.

2.	The Project Info page gives an overview of the schematic that is being reviewed and the person(s) performing the review. It also contains the Purpose and Disclaimer paragraphs.

3.	The checklist pages contain some of the more common items that should be checked. In some cases, these items might not apply to a specific schematic review and can be ignored. In other cases, there might be additional items that need to be checked.

4	The checklist pages are intended to collect information for a single ACAP and its supporting device (such as configuration memory, Ethernet, PCIe, UART, USB, etc.). At the top of the checklist page, the device part number and reference designator need to be recorded.

5	"Each cell in the Status column has a pull-down menu with the color-coded selections PASS, CHECK, and PROBLEM. The Status column allows the customer to quickly see the results of the schematic review.
· PASS: The item receives reviewer approval.
· CHECK: The reviewer does not have sufficient information to determine if the item is PASS or poses a PROBLEM. The designer must research the item and provide additional information.
· PROBLEM: There is an issue with the item. PROBLEM flags the item for the designer, who needs to research the issue and find a solution.
· NOT CHECKED: The item has not been checked and might require additional attention.
· NOT USED: The item is not used in this design.
· N/A: The item is not applicable to this device or design."

6	The Actual Implementation column can be used to provide additional clarification. This information is especially important if the item is tagged with CHECK or PROBLEM.
Notes	When running a search for a keyword (ctrl-f), press the Options button and choose "Values" from the "Look in:" dropdown.
