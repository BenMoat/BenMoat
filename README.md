What I am currently working on 🔨...

# VinMind

### VinMind is a web application designed for the management of one or more vehicles. It focuses on keeping track of vehicle modifications, insurance, servicing, tax and MOT.

![landing](https://github.com/BenMoat/vin-mind/assets/43743754/74801cbd-3ed4-4a05-9cc1-b2e3e3b9a2e7)

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
![overview](https://github.com/BenMoat/vin-mind/assets/43743754/f17c6fd4-a1ef-40b8-a6b9-545f6d0d6c86)
> This screenshot shows a vehicle where the user has opted to input their reg to retrieve their tax and MOT status via the DVLA RES API.
> The user has also supplied a comprehensive list of modifications added to their vehicle.
> This provides the user with a daily reminder of how much money they have ~~wasted~~ *spent on modifications. 💸

Here is how a newly-added vehicle will look:
![overview-new](https://github.com/BenMoat/vin-mind/assets/43743754/1ada6fac-6473-4c49-bd33-26b8c9a44256)

## Light and Dark Mode:
Switch between light and dark mode at any time and your preference will be retained. 
![light-dark-mode](https://github.com/BenMoat/vin-mind/assets/43743754/6f6d2b17-a34a-48c9-bf30-25f165a3dd68)

> It is automatically set depending on your system theme. 

## Card Visibility Menu
A card menu has now been added, allowing the user to show or hide cards on the Overview tab. This is independently configurable for each vehicle:
![card-menu](https://github.com/BenMoat/vin-mind/assets/43743754/2f26cfaf-55c5-49db-a3c1-44500e033f0d)
> I know you want to hide the total costs of the modifications. You're welcome.

## Vehicle Switcher 
Seamlessly switch between any vehicle at any time, or add a new vehicle to your garage: 

![vehicle-switcher](https://github.com/BenMoat/vin-mind/assets/43743754/d9c2e7b5-7212-42eb-a877-4228b9653b88)
![new-vehicle](https://github.com/BenMoat/BenMoat/assets/43743754/e5c7e5d0-a724-43de-8fe7-fcbb97e40615)
> I own an identity-confused Toyota "Zupr4" so I had to cover both options. 

## Modifications 

Display a list of modifications with multiple ways of filtering them: 
![modifications](https://github.com/BenMoat/BenMoat/assets/43743754/166dcaa3-edc8-4066-af9e-2987bf7e5fbc)
> The user has 17 modifications all with either one or more attachments, as highlighted by the Files column. He sure knows how to waste money.
> You thought you could escape the total cost of your modifications, didn't you. 

### Modification
Up to three Invoices or any relevant files related to the modification can be attached:
![modification](https://github.com/BenMoat/vin-mind/assets/43743754/e5f6f657-1b78-4883-9fd0-7e847613a5ce)
> The user has created a non-obsolete modification and has attached a user guide to help brick their ECU. 

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
![settings](https://github.com/BenMoat/vin-mind/assets/43743754/d4187b5e-7108-4122-b986-e6b2f8d2d3fb)
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

## Accessibility
Although I am not directly affected by a website's command of accessible features, I think it should be an absolute priority to make every website easily accessible to everyone. 
93% is the lowest score from a page on this web app... for now. 

![accessibility](https://github.com/BenMoat/BenMoat/assets/43743754/a05edefc-4791-4ade-a6c9-48ff24486c62)

</details>

## Project Chronology
### Technical Documentation During Project Creation
If you're a true neckbeard, you can read through how I began developing this application here: https://1drv.ms/u/s!AmL6ph_olh5BlrJ-VBDoD6iCUCrrhQ?e=lCjA5c <br>
⚠️ It is best read in a Markdown editor. 
