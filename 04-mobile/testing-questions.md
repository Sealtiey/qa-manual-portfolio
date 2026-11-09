# Perguntas de teste — respostas

Respostas a perguntas situacionais de QA (estratégia de teste a partir de especificação, diferenças entre web/desktop/mobile, priorização de bugs críticos no fim do ciclo e como lidar com um bug crítico não detectado). Conteúdo original em inglês.

## Estratégia de teste

**Q: Analyze the excerpt from the specification. What tests will you apply to the described functionality?**

> Application X is the remote data backup solution trusted by Home;
>
> Business users are located worldwide. The application allows the user to back up his files and folders anytime.
>
> 50GB of storage space is available for the basic accounts and 500 GB for the premium account.
>
> The application contains 2 wizards: one for backup and another for data recovery.
>
> The application supports both manual and scheduled backup modes.
>
> Users can specify the backup file/folder location and set up the schedule using a backup wizard.
>
> The recovery wizard allows selecting the created backup and specifying the recovery Location.

**A:** I would test the backup and recovery functions.

For the backup, I would test:

- Manual backup of files and folders.

- Scheduled backup.

- Different backup locations.

- Different schedule dates and times.

- The storage limits: 50 GB for basic accounts and 500 GB for premium accounts.

- What happens when the storage limit is reached.

- Backup of different types and sizes of files.

For the recovery, I would test:

- Selecting an existing backup.

- Choosing the recovery location.

- Checking if the recovered files are correct.

- Trying to recover a backup that does not exist.

- What happens if there is not enough space in the recovery location.

I would also test what happens if the internet connection is lost during backup or recovery.

**Q: Testing Zoom.**

> Imagine, you have to test the Zoom app.
>
> You have:

- Web version

- Desktop version

- Mobile version

> Will the testing approaches for each of these versions differ in any way?
>
> If so, what?

**A:** Yes, the testing approach can be different for each version.

Some functional tests will be the same for all versions, such as joining a meeting, turning the microphone and camera on and off, using the chat, sharing the screen, and leaving the meeting.

However, each version also needs specific tests.

For the web version, I would test different browsers, permissions for camera and microphone, and different screen sizes.

For the desktop version, I would test installation, updates, permissions, notifications, and different operating systems.

For the mobile version, I would test Android and iOS, different screen sizes, screen rotation, notifications, phone calls during a meeting, switching between Wi-Fi and mobile data, and what happens when the app goes to the background.

So, the main functionality can be tested on all versions, but some tests will be different because each platform has its own characteristics.

## Situações de trabalho

**Q: Imagine that you are the Team lead of a small group of testers who found a few Critical bugs on the last day of testing and the developers do not have enough time to fix them all. Your actions?**

**A:** I would prioritize the bugs by severity and impact. I would discuss with the developers and product owner which bugs must be fixed before release. The most critical ones should be fixed first, and the others can be documented for the next release if there is no time.

**Q: You missed a critical bug. Explain why and give several options.**

**A:** I would be honest and report it as soon as I noticed it. I would analyze why I missed it, for example, lack of time, test coverage or unclear requirements. Then I would suggest options like fixing it before release, delaying the release, or accepting the risk and fixing it in the next version.
