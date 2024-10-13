What I am currently working on 🔨...

<h1 align="center">VinMind</h1>

### VinMind is a web application designed for the management of one or more vehicles. It focuses on keeping track of vehicle modifications, insurance, servicing, tax and MOT.

![landing](https://github.com/user-attachments/assets/06bb96ce-043a-45e3-b62f-ce3a395cee52)
___
#### Design Engineer ▲ @Vercel and Creator of [Shadcn/UI](https://ui.shadcn.com/)
![chadcn](https://github.com/user-attachments/assets/b712b495-6043-4da4-9cb5-cdec7bda24e0)
___

<details>
<summary><h1>Tech Stack</h1></summary>

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
<summary><h1>Features</h1></summary>

## Vehicle Overview

This tab provides an overview of your vehicle's data, depending on how you have populated the vehicle's information in the web app: 
![overview](https://github.com/user-attachments/assets/755243d2-7663-410f-9ba4-9af1bec4896f)

> This screenshot shows a vehicle where the user has opted to input their reg to retrieve their tax and MOT status via the DVLA RES API.
> The user has also supplied a comprehensive list of modifications added to their vehicle.
> This provides the user with a daily reminder of how much money they have ~~wasted~~ *spent on modifications. 💸

Here is how a newly-added vehicle will look:
![overview-new](https://github.com/user-attachments/assets/dceb66fa-0570-4459-8a31-ad99705f1e91)

## Light and Dark Mode:
Switch between light and dark mode at any time and your preference will be retained. 
![dashboard-light-dark](https://github.com/user-attachments/assets/715708c5-bb9a-4859-9d04-8d4b3cc33c82)

> It is automatically set depending on your system theme. 

## Card Visibility Menu
A card menu has now been added, allowing the user to show or hide cards on the Overview tab. This is independently configurable for each vehicle:
![card-menu](https://github.com/user-attachments/assets/f26fb208-dd1a-479b-87d4-e94e2713727c)

> I know you want to hide the total costs of the modifications. You're welcome.

## Notification Center
Get reminders of when your Tax, MOT, Servicing and Insurance is due. 

Each reminder is colour-coded and prioritised by the due date, with the main notification's dot colour set by this:

- 🟢 Due within 30 days.

- 🟠 Due within 7 days.

- 🔴 Due today/Overdue.

![notifications](https://github.com/user-attachments/assets/7eba8550-de6a-4b4e-96d0-7d9062b2ca54)
![notifications-read](https://github.com/user-attachments/assets/958a828d-f4ce-4bd4-a3ca-44c53d2d47d1)

> Notifications can be dismissed individually or all at once by either clicking on `Mark as Read` when hovering over the message, or `Mark all as Read` at the top of the notification center.
> For data housekeeping, each message, both Read and Unread has an expiry date of 30 days where the message will automatically be deleted. 


## Vehicle Switcher 
Seamlessly switch between any vehicle at any time, or add a new vehicle to your garage: 

![vehicle-switcher](https://github.com/BenMoat/vin-mind/assets/43743754/d9c2e7b5-7212-42eb-a877-4228b9653b88)
![new-vehicle](https://github.com/BenMoat/BenMoat/assets/43743754/e5c7e5d0-a724-43de-8fe7-fcbb97e40615)
> I own an identity-confused Toyota "Zupr4" so I had to cover both options. 

## Modifications 

Display a list of modifications with multiple ways of filtering them: 
![modifications](https://github.com/user-attachments/assets/d8d6b106-57ff-4423-9b47-eb39f5dd8b13)

> The user has 18 modifications all with either one or more attachments, as highlighted by the Files column. He sure knows how to waste money.
> You thought you could escape the total cost of your modifications, didn't you. 

### Modification
Up to three Invoices or any relevant files related to the modification can be attached:
![modification](https://github.com/user-attachments/assets/4d7ffd97-d594-4ceb-ae8c-c493bdbba0a0)

> The user has created a non-obsolete modification and has attached a user guide to help brick their ECU. 

## Modification Types
Catergorise your modifications by what type they are: exterior, interior, performance etc:
![modification-types](https://github.com/user-attachments/assets/44b35778-f02a-4147-b9a7-d7b287a9b75f)

> The user is able to see all related modifications to this type. They are able to click on one to view or edit it. I don't have a shit joke for this one, sorry. 

## Servicing
Keep track of your vehicle's service history. If the user has added more than one service, it will display the mileage and time in between each service in an 
intermediate card:

![servicing](https://github.com/user-attachments/assets/73318e0f-e7b4-4ee2-bf91-94836c159f34)


## Settings 
Change your vehicle's name, supply the registration number or delete data associated with this vehicle:
![settings](https://github.com/user-attachments/assets/e6cdf083-7c0c-4189-95d0-8fbe3e6c4f63)

> The user can change their vehicle's name or delete the vehicle entirely at any time.
> Protection features are built in so a user cannot delete all modification types unless there are no modifications associated with that type. 
> The developer wants to ensure you that he **definitely, 100%, no cap on a stack, did not** do this multiple times throughout development.  

## Responsiveness
Recently, I have been working on making the site more mobile-friendly, including adding a Burger Menu for smaller devices:

![menu-mobile](https://github.com/BenMoat/BenMoat/assets/43743754/3bd88434-98bc-4865-9e5b-b527c29c34c8)

![overview-mobile](https://github.com/user-attachments/assets/fb25fdd5-c5b5-4501-b5bb-c0cc60b0c22b)

![modifications-mobile](https://github.com/BenMoat/BenMoat/assets/43743754/8a974b9b-0ef9-40da-88f7-b5737700416d)

> The app has been made fully mobile-responsive with the expensive of the developer's remaining sanity. 

## Tax, MOT and Insurance
Mistakenly, the government trusted me with some API keys. <br>
Enter your vehicle's registration number to view its up-to-date tax and MOT status in the Overview tab. This is directly sourced from the [DVLA RES API](https://developer-portal.driver-vehicle-licensing.api.gov.uk/apis/vehicle-enquiry-service/vehicle-enquiry-service-description.html#response). 

To avoid getting 429'd, a request is only sent to the RES API if the user has **added/changed** their registration or it has been **24 hours** since the API was last called:

![last-updated-badge](https://github.com/user-attachments/assets/41669cf3-013d-4939-a728-2d8981b5309c)

> The user is able to see how recent the tax and MOT status is by clicking on the question mark icon. 

The insurance is dependant on the user manually inputting the data. This still follows the same principal of calling an api once every 24 hours to ensure its reflecting the correct data. In this instance, the API is called to determine whether to update the insurance status as "Insured" or "Not Insured":

![insurance-reminder](https://github.com/user-attachments/assets/cf05cec0-64cc-4c6a-a0ec-7c24d214af96)

![insurance-card](https://github.com/user-attachments/assets/83751787-70d0-438a-9832-033c6b5a9262)

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
