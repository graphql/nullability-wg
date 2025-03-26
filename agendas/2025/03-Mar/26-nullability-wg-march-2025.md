| This is an open meeting: To attend, edit and PR this file. (Edit: ✎ above, or press "e") |
| ---------------------------------------------------------------------------------------- |

# Nullability WG — March 2025

The Nullability WG (Working Group) is a subcommittee of the GraphQL Spec WG
tasked with improving the experience around nullability in GraphQL. It was
previously known as the Client Controlled Nullability WG, but now includes
server-side solutions within its scope also.

This is an open meeting in which anyone in the GraphQL community may attend.
We typically meet on the last Wednesday


- **Date & Time**: [March 26, 2025, 7:00 – 8:00 PM UTC](https://www.timeanddate.com/worldclock/converter.html?iso=20250326T190000&p1=224&p2=179&p3=136&p4=268&p5=367&p6=438&p7=248&p8=240)
  - View the [calendar][], or subscribe ([Google Calendar][], [ical file][]).
  - _Please Note:_ The date or time may change. Please check this agenda the
    week of the meeting to confirm. While we try to keep all calendars accurate,
    this agenda document is the source of truth.
- **Video Conference Link**: https://zoom.us/j/95723407712?pwd=ZHhQakxqd1JlTnZJNTJXdlN3UFdQUT09
- **Live Notes**: [Live Notes][]

[calendar]: https://calendar.google.com/calendar/embed?src=linuxfoundation.org_ik79t9uuj2p32i3r203dgv5mo8%40group.calendar.google.com
[google calendar]: https://calendar.google.com/calendar?cid=bGludXhmb3VuZGF0aW9uLm9yZ19pazc5dDl1dWoycDMyaTNyMjAzZGd2NW1vOEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t
[ical file]: https://calendar.google.com/calendar/ical/linuxfoundation.org_ik79t9uuj2p32i3r203dgv5mo8%40group.calendar.google.com/public/basic.ics
[live notes]: https://docs.google.com/document/d/1IwWB_JBgqFnKVNnXph1k0j3ZTrMzYR9n8fEaxR11Fj4/edit

## Attendees

<!-- prettier-ignore -->
| Name                 | GitHub        | Organization       | Location              |
| :------------------- | :------------ | :----------------- | :-------------------- |
| Martin Bonnin| @martinbonnin | Apollo | Paris, FR |
| Calvin Cestari | @calvincestari | Apollo | Vancouver, BC |
| Benjie Gillam        | @benjie       | Graphile           | Chandler's Ford, UK   |
| Alex Reilly | @twof | DoorDash | San Francisco, CA, US |


## Agenda

1. Agree to Membership Agreement, Participation & Contribution Guidelines and Code of Conduct (1m, Host)
   - [Specification Membership Agreement](https://github.com/graphql/foundation)
   - [Participation Guidelines](https://github.com/graphql/graphql-wg#participation-guidelines)
   - [Contribution Guide](https://github.com/graphql/graphql-spec/blob/main/CONTRIBUTING.md)
   - [Code of Conduct](https://github.com/graphql/foundation/blob/master/CODE-OF-CONDUCT.md)
   - Meetings are [published to YouTube](https://www.youtube.com/@GraphQLFoundation/videos) and we may use LLM/AI summary tools
1. Introduction of attendees (5m, Host)
1. Determine volunteers for note taking (1m, Host)
1. Review agenda (2m, Host)
1. Check for [ready for review agenda items](https://github.com/graphql/nullability-wg/issues?q=is%3Aissue+is%3Aopen+label%3A%22Ready+for+review+%F0%9F%99%8C%22+sort%3Aupdated-desc) (5m, Host)
1. State of experimental features (5m, Martin)
   - `@experimental_disableErrorPropagation`
     - graphql-java: merged, not released
     - graphql-js: merged, not released
   - `@semanticNonNull`
     - relay: available in version [18.0.0](https://relay.dev/docs/guides/semantic-nullability/)
     - grats: available in version [0.0.32](https://grats.capt.dev/docs/guides/strict-semantic-nullability/)
     - [graphql-sock](https://github.com/graphile/graphql-sock): available in version 1.0.0
     - graphql-code-generator: [PR opened](https://github.com/dotansimha/graphql-code-generator/pull/10323)
   - `@catch`
     - relay: available in version [18.0.0](https://relay.dev/docs/guides/catch-directive/) 
   - Throw on error
     - [graphql-toe](https://github.com/graphile/graphql-toe) released v1.0.0-rc.0
     - [@urql/exchange-throw-on-error](https://github.com/urql-graphql/urql/blob/main/exchanges/throw-on-error) released v0.1.2
     - Relay: [@throwOnFieldError](https://relay.dev/docs/guides/throw-on-field-error-directive/) since v18.0.0
1. [Transitional non-null proposal](https://benjie.dev/graphql/nullability) (10m, Benjie)
   - [60 second video summary](https://youtu.be/gYnVaZz-19A)
