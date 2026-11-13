# Swirl

Analysis of a slow, periodic component ("swirl") in fixational eye-motion traces from AOSLO recordings, using scalograms and the Fourier transform.

## Data

Each video has 900 frames and is 30 s long. Every frame is stabilised in 33 strips, so one strip corresponds to about 1.01 ms. The horizontal and vertical shifts per strip are in `2018_02_21_15_40_08_AOSLO/` (`.csv` and MATLAB `.fig` files).

## What was found

- The scalograms of the horizontal and vertical shifts show a high-power component around 2 to 2.75 Hz. Two successive negative peaks 400 ms apart give about 2.5 Hz, in line with the scalograms. The dominant frequency changes over time.
- In the Fourier transform, the strong low-frequency component is at 2.308 Hz, for both horizontal and vertical shifts.
- A component at 33 Hz (one cycle per 33 strips) was expected but is not present. There is only a small component at 30.31 Hz, which is tiny compared with the low-frequency components.
- Two ways of separating the carrier signal (removing low or high frequencies globally, and MATLAB built-in smoothing) followed by stacking 33-strip windows did not reveal a pattern common to the whole recording.

## Notes

The scalogram is good at showing when frequencies occur, but removing components globally from it works poorly; the Fourier transform is better for global removal.

Full write-up with figures: `2021-07-18_swirl.docx` and `FEM.docx`. The large result files are linked in `ReadMe.txt`.
