| This is an open meeting: To attend, edit and PR this file. (Edit: ✎ above, or press "e") |
| ---------------------------------------------------------------------------------------- |

# Nullability WG — September 2024

The Nullability WG (Working Group) is a subcommittee of the GraphQL Spec WG
tasked with improving the experience around nullability in GraphQL. It was
previously known as the Client Controlled Nullability WG, but now includes
server-side solutions within its scope also.

This is an open meeting in which anyone in the GraphQL community may attend.
We typically meet on the last Wednesday


- **Date & Time**: [September 25, 2024, 7:00 – 8:00 PM UTC](https://www.timeanddate.com/worldclock/converter.html?iso=20240925T190000&p1=224&p2=179&p3=136&p4=268&p5=367&p6=438&p7=248&p8=240)
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
| Alex Reilly          | @twof         | Independent        | San Francisco, US     |
| Benjie Gillam        | @benjie       | Graphile           | Chandler's Ford, UK   |
| Benoit Lubek         | @bod          | Apollo             | Lyon, FR              |
| Calvin Cestari       | @calvincestari| Apollo (Swift)     | Vancouver, CA         |
| Martin Bonnin        | @martinbonnin | Apollo             | Paris, FR             |
| Jordan Eldredge      | @Captbaritone | Meta (Relay)       | San Francisco, US     |
| Itamar Kestenbaum    | @itamark      | Meta               | Plainsboro, NJ        |
| Stephen Spalding     | @fotoetienne  | Netflix            | Los Gatos, CA, US     |
| Alf Lervåg           | @alf          | Sikt               | Oslo, NO              |
| Ernie Turner         | @ernieturner  | Coinbase           | Bozeman, MT           |

## Agenda

1. Agree to Membership Agreement, Participation & Contribution Guidelines and Code of Conduct (1m, Host)
   - [Specification Membership Agreement](https://github.com/graphql/foundation)
   - [Participation Guidelines](https://github.com/graphql/graphql-wg#participation-guidelines)
   - [Contribution Guide](https://github.com/graphql/graphql-spec/blob/main/CONTRIBUTING.md)
   - [Code of Conduct](https://github.com/graphql/foundation/blob/master/CODE-OF-CONDUCT.md)
1. Introduction of attendees (5m, Host)
1. Determine volunteers for note taking (1m, Host)
1. Review agenda (2m, Host)
1. Review previous meeting's action items (5m, Host)
   - [Ready for review](https://github.com/graphql/nullability-wg/issues?q=is%3Aissue+is%3Aopen+label%3A%22Ready+for+review+%F0%9F%99%8C%22+sort%3Aupdated-desc)
   - [All open action items (by last update)](https://github.com/graphql/nullability-wg/issues?q=is%3Aissue+is%3Aopen+label%3A%22Action+item+%3Aclapper%3A%22+sort%3Aupdated-desc)
1. Introducing the nullability trifecta (10m, Benjie)
   - client-side localized error handling (e.g. throw on error) - brings the errors back into the data tree
   - no null bubbling - for smart clients, fixes issues writing to normalized caches when errors occur, but requires clients to reproduce null-bubbling
   - semantic non-null - indicates what the true nullability of something is, excluding the possibility of errors
1. Introducing [GraphQL-TOE](https://github.com/graphile/graphql-toe) (5m, Benjie)
   - Already has [a PR open against URQL](https://github.com/urql-graphql/urql/pull/3677)
   - Should also work with `window.fetch()`-style implementations, and `useQuery()` from Apollo Client
1. An [early implementation in graphql-js](https://github.com/graphql/graphql-js/pull/4192) (25m, Benjie)
   - How should introspection work for backwards compatibility?
   - Doesn't use the latest proposed syntax; let's revisit this now the implementation and application is more concrete
1. Incorporate `graphql-toe` and the graphql-js pre-release into blog post? (15m, Benjie)
   - If we can agree on some things above and fix the implementation, we can let people get hands on with the full nullability trifecta.
