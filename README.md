# Software Engineering Design Patterns

A Java console demonstration that combines **Observer**, **Abstract Factory**,
and **Singleton** in a simulated weather-reporting scenario.

## How the patterns fit together

| Pattern | Role in the demonstration |
| --- | --- |
| Observer | Temperature subjects notify an attached display when readings change |
| Abstract Factory | An icon factory selects the representation for the current temperature |
| Singleton | Sun, cloud, and snow icons are obtained through shared instances |

The readings are randomly generated; this is not a weather API client.
The console uses colored output and weather symbols.

## Build and run

Use a JDK with Java 7-or-later language support. From the repository root:

```sh
javac -encoding UTF-8 -sourcepath src -d out src/main/Main.java
java -cp out main.Main
```

The simulation updates its city readings ten times with five-second intervals.
Use a UTF-8-capable terminal with ANSI color support to display the icons as
intended.

## Repository guide

| Path | Purpose |
| --- | --- |
| [src/main/Main.java](src/main/Main.java) | Simulation, temperature subjects, display, and concrete factory |
| [src/observer](src/observer) | Observer contract and subject registration |
| [src/abstractFactory](src/abstractFactory) | Factory and icon interfaces |
| [src/singleton](src/singleton) | Shared weather-icon implementations |
| [elaboratoOrale.docx](elaboratoOrale.docx) | Original coursework document |
| [correzioneEsame.docx](correzioneEsame.docx) | Related examination document |

## Scope

This is a compact coursework example intended to make the interaction between
patterns visible. It has no external service dependency, GUI, or build-tool
wrapper. The singleton implementations demonstrate the pattern in this
single-threaded scenario rather than providing thread-safe application services.

## Project provenance

This repository is a fork of
[edoardore/ElaboratoSWE](https://github.com/edoardore/ElaboratoSWE).
The original implementation and history are preserved.
