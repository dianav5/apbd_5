# TrainingCenterApi

Prosta aplikacja ASP.NET Core Web API oparta na kontrolerach.

## Opis
Aplikacja służy do zarządzania salami oraz rezerwacjami w centrum szkoleniowym.
Dane są przechowywane wyłącznie w pamięci aplikacji przy użyciu statycznych list.

## Zastosowane elementy
- ASP.NET Core Web API
- Controllers
- routing atrybutowy
- GET, POST, PUT, DELETE
- model binding z route, query i body
- walidacja Data Annotations
- poprawne statusy HTTP

## Endpointy

### Rooms
- GET /api/rooms
- GET /api/rooms/{id}
- GET /api/rooms/building/{buildingCode}
- POST /api/rooms
- PUT /api/rooms/{id}
- DELETE /api/rooms/{id}

### Reservations
- GET /api/reservations
- GET /api/reservations/{id}
- GET /api/reservations?date=2026-05-10&status=confirmed&roomId=2
- POST /api/reservations
- PUT /api/reservations/{id}
- DELETE /api/reservations/{id}

## Reguły biznesowe
- nie można dodać rezerwacji dla nieistniejącej sali
- nie można dodać rezerwacji dla nieaktywnej sali
- nie można dodać dwóch nakładających się rezerwacji tej samej sali tego samego dnia
- nie można usunąć sali, która ma powiązane rezerwacje

## Statusy HTTP
- 200 OK
- 201 Created
- 204 No Content
- 400 Bad Request
- 404 Not Found
- 409 Conflict

## Testowanie
API zostało przetestowane w Swaggerze i może być testowane również w Postmanie.