# Entity Relationships

::: mermaid

erDiagram

Place {
  Guid Id
  String Name
  String Address
}

Booking {
  Guid Id
  Guid PlaceId
  Date CheckIn
  Date CheckOut
  Bool IsConfirmed
}

Booking2Guest {
  Guid BookingId
  Guid GuestId
}

Guest {
  Guid Id
  String Name
}

GuestContact {
  Guid Id
  Guid GuestId
  Int Type
  String Value
}

Booking }o--|| Place : has
Booking ||--o{ Booking2Guest : contains
Guest ||--o{ Booking2Guest: orders
Guest |o--o{ GuestContact: "may have"

:::

---

1. Uma reserva (Booking) pode conter mais do que um Hóspede (Guest).
1. Uma reserva (Booking) está obrigatoriamente relacionada a um lugar (Place).
1. Um hóspede (Guest) pode conter mais do que uma forma de contato.
1. `GuestContactType` pode ser:
    - `0` unknown
    - `1` email
    - `2` phone

---
[Índice](../Readme.md)
