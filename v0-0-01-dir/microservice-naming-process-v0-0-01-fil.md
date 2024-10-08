### SAMBAR Microservice Naming Process

Sambar Web Application employ a specific naming convention for microservices to ensure clarity, organization, and efficient management. The convention follows a structured format that incorporates essential information about the microservice.

**Microservice Name Structure**
A Sambar Web Application microservice name consists of multiple segments separated by hyphens:

**`<Microservice Identifier>-<Subscription Plan>-<Country>-<Language>-<Environment>-<Region>`**

**`ub02130-no-us-en-sd2-lo`**

**Breakdown of Segments**

| Segment    | Description                                                  | Example |
| ---------- | ------------------------------------------------------------ | ------- |
| `ub02130-` | **Microservice Identifier**: Composed of an alphabetic prefix and a numeric suffix. The alphabetic prefix is constructed by concatenating the initial letter of each word comprising the full microservice name (e.g., "ub" for "user board"). The numeric suffix, a four or five digit number (e.g., "02130"), correlates to the specific Flow and BLOCK within the system where the microservice is originally defined. | ub02130 |
| `-no-`     | **Subscription Plan**: Specifies the target user group based on subscription plans (e.g., "no" for no subscription). | no      |
| `-us-`     | **Country**: Indicates the geographical region for which the microservice is designed (e.g., "us" for the United States). | us      |
| `-en-`     | **Language**: Specifies the language supported by the microservice (e.g., "en" for English). | en      |
| `-sd2-`    | **Environment**: Identifies the operational environment (e.g., "sd2" for Sambar Web Application development). | sd2     |
| `-lo`      | **Region**: Specifies the AWS region where the microservice is deployed (e.g., "lo" for London). | lo      |

**Example**

The microservice name `ub02130-no-us-en-sd2-lo` :

`ub02130`: User board microservice, Flow `021`, BLOCK `30`

`no`: No subscription plan

`us`: United States

`en`: English

`sd2`: Sambar Web Application development environment

`lo`: London AWS region

**Purpose of the Naming Convention**

The naming convention serves several key purposes:

- Clarity and Understanding: Provides a clear and concise description of the microservice's purpose and characteristics.
- Organization: Enables efficient categorization and grouping of microservices based on various criteria.
- Management: Facilitates microservice lifecycle management, including deployment, scaling, and monitoring.
- Debugging and Troubleshooting: Aids in identifying the specific microservice involved in issues.

### Order of Segments in Microservice Naming Process

| Segment    | Placement | Rationale                                                    |
| ---------- | --------- | ------------------------------------------------------------ |
| `ub02130-` | 1st       | This segment uniquely identifies the microservice, including its type and internal reference. Placing it first establishes the core identity of the service. |
| `-no-`     | 2nd       | Following the microservice identifier, the subscription plan segment specifies the target user group. This order allows for easy grouping of microservices based on subscription plans. |
| `-us-`     | 3rd       | After specifying the target user group, indicating the geographical region helps in categorizing microservices based on location. This order facilitates management of region-specific functionalities. |
| `-en-`     | 4rd       | Following the country, the language segment defines the supported language. This sequence logically builds on the geographical targeting and specifies the user language preference. |
| `-sd2-`    | 5th       | The environment segment indicates the operational context of the microservice. Placing it after the language suggests that the environment might influence the language or regional aspects of the service. |
| `-lo`      | 6th       | The region segment specifies the physical location of the microservice. Placing it at the end emphasizes the deployment location, differentiating between microservices with identical configurations but deployed in different regions. |

**Importance of the Order**

The specific order of segments in the microservice naming convention offers several advantages:

- Logical Grouping: Microservices can be grouped based on subscription plans, countries, languages, environments, or regions for efficient management.
- Search and Filtering: The ordered structure facilitates searching and filtering for specific microservices based on various criteria.
- Scalability: As the system grows, new microservices can be added while maintaining a consistent naming structure.
- Understanding: The order provides a clear and intuitive way to understand the purpose and characteristics of a microservice at a glance.

**Important Note:**

The environment ID for the Sambar Web Application must be a two-character code commencing with the letter `s`, followed by a single letter designating the particular environment:	

- `d`: development	
- `t`: testing	
- `p`: production
- `s`: staging
and so on.

Generally, Sambar Web Application avoids using numerical digits within environment identifiers (e.g., `sd` for development, `sp` for production, `st` for testing). The inclusion of `sd2` as the environment in the example above represents a specific exception due to the need for a second development environment.

By adhering to this naming convention, Sambar Web Application ensures a well-structured and manageable microservice ecosystem. The specific order of segments in a Sambar Web Application microservice name is crucial for effective organization, identification, and management.
