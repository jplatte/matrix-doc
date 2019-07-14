# MSC2175: Remove the `creator` field from `m.room.create` events

[`m.room.create`](https://matrix.org/docs/spec/client_server/r0.5.0#m-room-create)
events have a mandatory `creator` property giving the ID of the user who
created the room. This field is redundant as it is always identical to the
`sender` of the create event.

This MSC proposes that, in a future room version, this field should be removed.