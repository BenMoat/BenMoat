What I am currently working on 🔨...

# VinMind

VinMind is a web application designed for the management of one or more vehicles. It focuses on keeping track of vehicle modifications, insurance, servicing, tax and MOT.
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

This tab provides an overview of your vehicle's data, depending on how you have populated the vehicle's information in the web app: 
![overview](https://github.com/BenMoat/BenMoat/assets/43743754/13cfc8b6-34c4-4a3b-8114-db89a304eca4)

> This screenshot shows a vehicle where the user has opted to input their reg to retrieve their tax and MOT status via the DVLA RES API.
> The user has also supplied a comprehensive list of modifications added to their vehicle.
> This provides the user with a daily reminder of how much money they have ~~wasted~~ *spent on modifications. 💸

### Card Visibility Menu
A card menu has now been added, allowing the user to show or hide cards on the Overview tab. This is independently configurable for each vehicle:
![card-menu](https://github.com/BenMoat/BenMoat/assets/43743754/fa10d425-d0dc-45b8-8ee6-0decbf26b3e0)
> I know you want to hide the total costs of the modifications. You're welcome.

## Vehicle Switcher 
Seamlessly switch between any vehicle at any time, or add a new vehicle to your garage: 

![vehicle-switcher](https://github.com/BenMoat/BenMoat/assets/43743754/7fd16811-0d07-44e0-9bfe-1a8a30c1f826)
![new-vehicle](https://github.com/BenMoat/BenMoat/assets/43743754/e5c7e5d0-a724-43de-8fe7-fcbb97e40615)
> I own an identity-confused Toyota "Zupr4" so I had to cover both options. 

## Modifications 

Display a list of modifications with multiple ways of filtering them: 
![modifications](https://github.com/BenMoat/BenMoat/assets/43743754/166dcaa3-edc8-4066-af9e-2987bf7e5fbc)
> The user has 17 modifications all with either one or more attachments, as highlighted by the Files column. He sure knows how to waste money.
> You thought you could escape the total cost of your modifications, didn't you. 

### Modification
Invoices or any relevant files related to the modification can be attached:
![modification](https://github.com/BenMoat/BenMoat/assets/43743754/29a98e9f-46e9-4277-8f25-ee23640b0b0e)

> The user has created a non-obsolete modification and has attached torque spec instructions that they are highly unlikely to follow. 

## Modification Types
Catergorise your modifications by what type they are: exterior, interior, performance etc:
![modification-types](https://github.com/BenMoat/BenMoat/assets/43743754/2142bd1c-b683-4b13-9edf-d94ba49c894e)
> The user is able to see all related modifications to this type. They are able to click on one to view or edit it. I don't have a shit joke for this one, sorry. 

## Servicing
Keep track of your vehicle's service history. If the user has added more than one service, it will display the mileage and time in between each service in an 
intermediate card:

![servicing](https://github.com/BenMoat/BenMoat/assets/43743754/a0d93064-b7c6-477c-9491-a6666572c999)

## Settings 
Change your vehicle's name, supply the registration number or delete data associated with this vehicle:
![settings](https://github.com/BenMoat/BenMoat/assets/43743754/2e583946-a37d-45ca-b6c7-53c73abf5d71)

> The user can change their vehicle's name or delete the vehicle entirely at any time.
> Protection features are built in so a user cannot delete all modification types unless there are no modifications associated with that type. 
> The developer wants to ensure you that he **definitely, 100%, no cap on a stack, did not** do this multiple times throughout development.  

## Responsiveness
Recently, I have been working on making the site more mobile-friendly, including adding a Burger Menu for smaller devices:

![menu-mobile](https://github.com/BenMoat/BenMoat/assets/43743754/3bd88434-98bc-4865-9e5b-b527c29c34c8)

![overvew-mobile](https://github.com/BenMoat/BenMoat/assets/43743754/531f8174-b3b9-42b9-8b5b-f4933075737d)

![modifications-mobile](https://github.com/BenMoat/BenMoat/assets/43743754/8a974b9b-0ef9-40da-88f7-b5737700416d)

> The app has been made fully mobile-responsive with the expensive of the developer's remaining sanity. 

## Tax, MOT and Insurance
Mistakenly, the government trusted me with some API keys. <br>
Enter your vehicle's registration number to view its up-to-date tax and MOT status in the Overview tab. This is directly sourced from the [DVLA RES API](https://developer-portal.driver-vehicle-licensing.api.gov.uk/apis/vehicle-enquiry-service/vehicle-enquiry-service-description.html#response). 

To avoid getting 429'd, a request is only sent to the RES API if the user has **added/changed** their registration or it has been **24 hours** since the API was last called:

![last-updated-badge](https://github.com/BenMoat/BenMoat/assets/43743754/22695da7-92d4-46d4-9fe5-6d964cb88173)
> The user is able to see how recent the tax and MOT status is by clicking on the question mark icon. 

The insurance is dependant on the user manually inputting the data. This still follows the same principal of calling an api once every 24 hours to ensure its reflecting the correct data. In this instance, the API is called to determine whether to update the insurance status as "Insured" or "Not Insured":

![insurance-reminder](https://github.com/BenMoat/BenMoat/assets/43743754/9e74f2ee-7841-4eef-9cb9-4fccd084bd39)
![insurance-card](https://github.com/BenMoat/BenMoat/assets/43743754/2e367eb6-9397-4818-af81-79723141ec98)

> Now the 89 year old Margret can eagerly await to pay £4300 on her 2003 Micra. 

## Light and Dark Mode:
For some reason, some people _(who I do not want to be associated with)_ prefer light mode so I reluctantly added this option:
![light-dark-mode](https://github.com/BenMoat/BenMoat/assets/43743754/100b6abe-4f85-4697-b0b8-fc75e3346cb1)

> It is automatically set depending on your system theme, however, you can change the web app's theme **TO DARK MODE** at any time and your preference will be retained. Thank you for making the right decision. 

## Accessibility
Although I am not directly affected by a website's command of accessible features, I think it should be an absolute priority to make every website easily accessible to everyone. 
93% is the lowest score from a page on this web app... for now. 

![accessibility](https://github.com/BenMoat/BenMoat/assets/43743754/a05edefc-4791-4ade-a6c9-48ff24486c62)

</details>

## Project Chronology
### Technical Documentation During Project Creation
If you're a true neckbeard, you can read through how I began developing this application here: https://1drv.ms/u/s!AmL6ph_olh5BlrJ-VBDoD6iCUCrrhQ?e=lCjA5c <br>
⚠️ It is best read in a Markdown editor. 
