# Achiziția și generarea semnalelor analogice folosind LabVIEW
### Analog Signal Acquisition and Generation using LabVIEW

---

## 🇷🇴 Română

### Descriere

Acest proiect a fost dezvoltat în **LabVIEW** și urmărește implementarea operațiilor de achiziție, prelucrare și generare a semnalelor analogice, utilizând driverele **NI-DAQmx** și funcționalitățile echipamentelor National Instruments Data Acquisition (DAQ).

Proiectul include mai multe instrumente virtuale (VI-uri) care permit configurarea canalelor analogice, citirea și scrierea datelor, utilizarea temporizării pentru achiziție și generare, precum și vizualizarea semnalelor.

## Funcționalități

- Achiziția semnalelor analogice (Analog Input).
- Generarea semnalelor analogice (Analog Output).
- Configurarea canalelor și task-urilor NI-DAQmx.
- Citirea datelor analogice utilizând `DAQmx Read`.
- Scrierea datelor analogice utilizând `DAQmx Write`.
- Vizualizarea semnalelor prin intermediul unui Waveform Chart.
- Utilizarea temporizării Sample Clock pentru operații bazate pe waveform.
- Gestionarea și oprirea task-urilor de achiziție și generare.

## Structura proiectului

```text
Achizitie-Generare-Semnale-LabVIEW/
│
├── L12.vi
├── L12_1.vi
├── L12_2.vi
├── L12_3.vi
└── README.md
```

## Tehnologii utilizate

- **LabVIEW** – programare grafică și dezvoltarea instrumentelor virtuale.
- **NI-DAQmx** – configurarea și controlul operațiilor de achiziție și generare.
- **National Instruments DAQ** – interfață hardware pentru intrări și ieșiri analogice.

## Cerințe tehnice

- LabVIEW instalat.
- Drivere NI-DAQmx.
- Dispozitiv National Instruments DAQ compatibil pentru testarea operațiilor hardware.
- Canale și conexiuni hardware configurate corespunzător.

## Detalii tehnice

### L12.vi – Generarea formelor de undă

Utilizează funcții NI-DAQmx pentru temporizare și scrierea formelor de undă.

- Funcții NI-DAQmx de temporizare.
- Scriere de date de tip waveform.
- Referințe la două ieșiri de tensiune: `VoltageOut_0` și `VoltageOut_1`.

### L12_1.vi – Scrierea formelor de undă

Utilizează funcții NI-DAQmx pentru temporizarea prin Sample Clock și scrierea datelor de tip waveform.

- `DAQmx Timing (Sample Clock)`.
- `DAQmx Write`.
- Configurarea operațiilor de generare.

### L12_2.vi – Achiziția semnalelor analogice

Realizează achiziția tensiunii analogice și afișarea datelor într-un Waveform Chart.

- `DAQmx Create Channel (AI-Voltage-Basic)`.
- `DAQmx Start Task`.
- `DAQmx Read (Analog DBL 1Chan 1Samp)`.
- `Waveform Chart`.
- `DAQmx Clear Task`.

### L12_3.vi – Generarea semnalelor analogice

Realizează generarea tensiunii analogice prin intermediul unui canal de ieșire DAQ.

- `DAQmx Create Channel (AO-Voltage-Basic)`.
- `DAQmx Write (Analog DBL 1Chan 1Samp)`.
- `DAQmx Start Task`.
- `DAQmx Wait Until Done`.
- `DAQmx Clear Task`.

## Parametri de achiziție și generare

Parametrii depind de configurația hardware și de setările utilizate în LabVIEW.

| Parametru | Configurație |
|---|---|
| Platformă de dezvoltare | LabVIEW |
| Driver | NI-DAQmx |
| Dispozitiv DAQ | National Instruments DAQ |
| Intrare analogică | Configurată prin NI-DAQmx |
| Ieșire analogică | Configurată prin NI-DAQmx |
| Frecvență de eșantionare | Depinde de configurarea VI-ului |
| Număr de eșantioane | Depinde de configurarea VI-ului |
| Domeniu de tensiune | Depinde de dispozitivul DAQ |

## Mod de utilizare

1. Descărcați sau clonați repository-ul.
2. Deschide fișierul VI dorit în LabVIEW.
3. Verifică dispozitivul DAQ și canalele fizice configurate.
4. Verifică parametrii de achiziție sau generare.
5. Rulează instrumentul virtual dorit.
6. Urmărește valorile și formele de undă afișate.
7. Oprește execuția folosind controlul STOP, dacă este disponibil.

---

# 🇬🇧 English

## Description

This project was developed using **LabVIEW** and focuses on implementing analog signal acquisition, processing, and generation operations through **NI-DAQmx** drivers and National Instruments Data Acquisition (DAQ) hardware.

The project includes several Virtual Instruments (VIs) that allow analog channel configuration, data reading and writing, sample-clock timing, and signal visualization.

## Features

- Analog signal acquisition (Analog Input).
- Analog signal generation (Analog Output).
- NI-DAQmx channel and task configuration.
- Analog data reading using `DAQmx Read`.
- Analog data writing using `DAQmx Write`.
- Signal visualization through a Waveform Chart.
- Sample Clock timing for waveform-based operations.
- Acquisition and generation task management.

## Project Structure

```text
Achizitie-Generare-Semnale-LabVIEW/
│
├── L12.vi
├── L12_1.vi
├── L12_2.vi
├── L12_3.vi
└── README.md
```

## Technologies Used

- **LabVIEW** – graphical programming and Virtual Instrument development.
- **NI-DAQmx** – configuration and control of data acquisition and generation.
- **National Instruments DAQ** – hardware interface for analog input and output operations.

## Technical Requirements

- LabVIEW.
- NI-DAQmx drivers.
- Compatible National Instruments DAQ hardware for physical testing.
- Properly configured channels and hardware connections.

## Technical Details

### L12.vi – Waveform Generation

Uses NI-DAQmx functions for timing and waveform writing.

- NI-DAQmx timing functions.
- Waveform data writing.
- References to two voltage outputs: `VoltageOut_0` and `VoltageOut_1`.

### L12_1.vi – Waveform Writing

Uses NI-DAQmx Sample Clock timing and waveform-writing functions.

- `DAQmx Timing (Sample Clock)`.
- `DAQmx Write`.
- Signal generation configuration.

### L12_2.vi – Analog Signal Acquisition

Acquires analog voltage data and displays it through a Waveform Chart.

- `DAQmx Create Channel (AI-Voltage-Basic)`.
- `DAQmx Start Task`.
- `DAQmx Read (Analog DBL 1Chan 1Samp)`.
- `Waveform Chart`.
- `DAQmx Clear Task`.

### L12_3.vi – Analog Signal Generation

Generates analog voltage through a DAQ analog output channel.

- `DAQmx Create Channel (AO-Voltage-Basic)`.
- `DAQmx Write (Analog DBL 1Chan 1Samp)`.
- `DAQmx Start Task`.
- `DAQmx Wait Until Done`.
- `DAQmx Clear Task`.

## Acquisition and Generation Parameters

Parameters depend on the hardware configuration and LabVIEW settings.

| Parameter | Configuration |
|---|---|
| Development platform | LabVIEW |
| Driver | NI-DAQmx |
| DAQ device | National Instruments DAQ |
| Analog Input | Configured through NI-DAQmx |
| Analog Output | Configured through NI-DAQmx |
| Sampling rate | Depends on VI configuration |
| Number of samples | Depends on VI configuration |
| Voltage range | Depends on DAQ hardware |

## How to Run

1. Clone or download this repository.
2. Open the desired VI file in LabVIEW.
3. Check the DAQ device and configured physical channels.
4. Verify the acquisition or generation parameters.
5. Run the desired Virtual Instrument.
6. Monitor the displayed values and waveforms.
7. Stop execution using the STOP control, if available.

---

## 👤 Autor / Author

**IonutD**
