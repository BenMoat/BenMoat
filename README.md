What I am currently working on 🔨...

# VinMind

VinMind is a web application designed for the management of one or more vehicles. It focuses on tracking vehicle modifications, insurance, tax and MOT.
<details>
<summary><h2>Tech Stack</h2></summary>

### Frontend

- **[Next.js](https://nextjs.org/)**: Utilised for server-side rendering, enhancing performance and SEO.
- **[TypeScript](https://www.typescriptlang.org/)**: Employed for static type checking, improving code reliability.
- **[Shadcn/UI](https://ui.shadcn.com/)**: A minimal yet beautifully designed UI component library.
- **[Tailwind CSS](https://tailwindcss.com/)**: Used for utility-first styling, ensuring a modern and responsive UI.
- **[Cloudinary](https://cloudinary.com/)**: Used for hosting the files uploaded to a modification. 

### Backend

- **[Prisma](https://www.prisma.io/)**: Handles database interactions.
- **[PlanetScale](https://planetscale.com/)**: MySQL database platform.
- **[Node.js](https://nodejs.org/en)**: Serves as the backend runtime.

### Authentication
- **[Clerk](https://clerk.com/)**: Integrated for user authentication and session management.

</details>
  
<details>
<summary><h2>Features</h2></summary>

## Vehicle Overview

This tab provides an overview of your vehicle's data, depending on how you have populated the vehicle's information in the web app.
![overview](https://github.com/BenMoat/BenMoat/assets/43743754/7e8fca69-b53f-4dc5-8f3b-44da89ff027f)
> This screenshot shows a vehicle where the user has opted to input their reg to retrieve their tax and MOT status via the DVLA RES API.
> The user has also supplied a comprehensive list of modifications added to their vehicle.
> This provides the user with a daily reminder of how much money they have ~~wasted~~ *spent on modifications. 💸

## Modifications 

Display a list of modifications with multiple ways of filtering them: 
![modifications](https://github.com/BenMoat/BenMoat/assets/43743754/61c4152d-4a22-4b6f-a70a-5099adb08e0a)
> The user has 17 modifications, all with either one or more attachments, as highlighted by the Files column. 

### Modification
Invoices or any relevant files related to the modification can be attached:
![modification](https://github.com/BenMoat/BenMoat/assets/43743754/2a44cef8-8101-446a-9439-9fab1076e7e9)
> The user has created a non-obsolete modification and has attached torque spec instructions that they are highly unlikely to follow. 

## Modification Types
Catergorise your modifications by what type they are: exterior, interior, performance etc:
![modification-types](https://github.com/BenMoat/BenMoat/assets/43743754/70d9a5cf-7b59-4a06-8687-c5d5bde4ae36)
> The user is able to see all modifications related to this modification type and is able to click on one to view or edit it. 

## Settings 
Change your vehicle's name, supply the registration number or delete data associated with this vehicle:
![settings](https://github.com/BenMoat/BenMoat/assets/43743754/786acc41-28d4-4f92-9cd3-19c0f77f3733)
> The user can change their vehicle's name or delete the vehicle entirely at any time.
> Security features are built in so a user cannot delete all modification types unless there are no modifications associated with that type. 

## Tax, MOT and Insurance
Mistakenly, the government trusted me with some API keys. <br>
Enter your vehicle's registration number to view its up-to-date tax and MOT status in the Overview tab. This is directly sourced from the [DVLA RES API](https://developer-portal.driver-vehicle-licensing.api.gov.uk/apis/vehicle-enquiry-service/vehicle-enquiry-service-description.html#response). 

To avoid getting 429'd, a request is only sent to the RES API if the user has **added/changed** their registration or it has been **24 hours** since the API was last called:

![last-updated-badge](https://github.com/BenMoat/BenMoat/assets/43743754/69daa833-8007-4dc1-9114-2c62427abb4b)
> The user is able to see how up-to-date the tax and MOT status is by clicking on the question mark icon. 

The insurance is dependant on the user selecting the date. This still follows the same principal of calling an api once evert 24 hours to ensure its reflecting the correct data. In this instance, the API is called to determine whether to update the insurance status as "Insured" or "Not Insured":

![insurance-reminder](https://github.com/BenMoat/BenMoat/assets/43743754/fc14ec3d-eb13-4692-873f-01ddb9eda374)
![insurance-card](https://github.com/BenMoat/BenMoat/assets/43743754/060c6edd-c503-446f-882f-a76606e95d2a)


## Light and Dark Mode:
For some reason, people prefer light mode so I reluctantly added this option:
![light-dark-mode](https://github.com/BenMoat/BenMoat/assets/43743754/61c2fffc-f803-484e-b2af-9004a81fc21e)
> It is automatically set depending on your system theme, however, you can change the web app's theme at any time and your preference will be retained. 

</details>

## Project Chronology
### Technical Documentation During Project Creation
If you're a true neckbeard, you can read through how I began developing this application here: https://1drv.ms/u/s!AmL6ph_olh5BlrJ-VBDoD6iCUCrrhQ?e=lCjA5c <br>
⚠️ It is best read in a Markdown editor. 
