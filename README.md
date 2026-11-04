## Hi, I'm Nicolás 👋

Software engineer from Maldonado, Uruguay. I build systems end to end, from the backend and the cloud infrastructure down to the NFC reader on the table. Most of my work lives where software meets physical things: wristbands, smart cards, kiosks and installations that real people touch at events.

These days I spend most of my open-source time on smart cards, especially getting the Uruguayan eID to work with open tooling.

## Smart cards and the Uruguayan eID

I contribute to [**OpenSC**](https://github.com/OpenSC/OpenSC), the open-source smart card middleware, where I work on support for the Uruguayan cédula de identidad:

- [Contactless (PACE) support](https://github.com/OpenSC/OpenSC/pull/3805) for the `cedulauy` driver, so the cédula works over NFC with a standard reader.
- [A fix in `sm-iso`](https://github.com/OpenSC/OpenSC/pull/3771) for response buffer sizing and `Le` in Secure Messaging, which truncated chained responses like RSA signatures read over NFC.
- Multi-batch testing and card identification (ATR mask) for the [original driver](https://github.com/OpenSC/OpenSC/pull/3729) by [Carlos Planchon](https://github.com/carlosplanchon), validated end to end with a PAdES signature.
- Smaller fixes to the tools and [documentation in the wiki](https://github.com/OpenSC/Wiki/pull/39) on the MRZ requirement for PACE.

Around that work:

- [**cedulauy-mrz-scan**](https://github.com/nicolasgutierrezdev/cedulauy-mrz-scan) reads the MRZ of a cédula from a photo or a live webcam feed. That's the input PACE needs to open a contactless session. [On PyPI](https://pypi.org/project/cedulauy-mrz-scan/).
- On [**FirmaUY**](https://github.com/carlosplanchon/firmauy), a CLI to sign and verify PDF, XML and other files with the cédula, I added the `fetch-identity` and `list-readers` commands, a native PKCS#11-free signing backend and Windows support, which I also brought to [firmauy-desktop](https://github.com/carlosplanchon/firmauy-desktop) and [firmauy-mcp-inspect](https://github.com/carlosplanchon/firmauy-mcp-inspect).

## NFC and events

As a tech lead I designed a dynamic NFC wristband system (backend and Android app) that handled real-time, queue-free check-in for events with 500+ people at once. Any wristband could be linked to any guest live, which removed a third-party dependency.

[**simple-nfc-tag**](https://github.com/nicolasgutierrezdev/simple-nfc-tag) is the library that came out of it: tag-agnostic data storage over PC/SC that hides reader, tag and protocol details. Tested on real hardware (ACR122U, NTAG213, MIFARE Classic 1K). [On PyPI](https://pypi.org/project/simple-nfc-tag/).

I've also built Raspberry Pi installations, like personalized welcome holograms and photo booths that send pictures straight to the event app, plus interactive experiences for [BMW](https://www.behance.net/gallery/213858163/The-Dream-Drive-Collection), [Campus Party](https://www.behance.net/gallery/213864257/QueRify) and [Burger King](https://www.behance.net/gallery/217666095/Burger-King-Almas-Gemelas).

## Python and FastAPI

I work mostly in the Python and FastAPI ecosystem. I contribute to [FastAPI Boilerplate](https://github.com/benavlabs/FastAPI-boilerplate), an extendable starting point for async APIs built on FastAPI, Pydantic v2, SQLAlchemy 2.0, PostgreSQL and Redis.

I also contributed to [UruAPI](https://github.com/LibreCourseUY/UruAPI), an API for Uruguay's daily economic indicators, through [LibreCourseUY](https://librecourse.uy).

## And then there's this

[**moanpoint**](https://github.com/nicolasgutierrezdev/moanpoint) makes every interaction with your ThinkPad TrackPoint awkward. It plays moaning sounds whose volume scales with how hard you push. It's also my most-starred repo, and I've made peace with that.

---

**Stack:** Python · FastAPI · PostgreSQL · Redis · AWS · Docker · Linux · C · Android · PC/SC, APDU, PKCS#11

🌐 [nicolasgutierrez.uy](https://nicolasgutierrez.uy) · 📫 [contacto@nicolasgutierrez.uy](mailto:contacto@nicolasgutierrez.uy)
