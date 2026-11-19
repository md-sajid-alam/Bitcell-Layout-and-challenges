# Bitcell-Layout-and-challenges

Design of 6T SRAM Bitcell in 7nm FinFet

## Schematic of 6T SRAM Bitcell
<img width="322" height="262" alt="image" src="https://github.com/user-attachments/assets/1d5cf216-1d02-4217-9238-cb7695256fc4" />

## Layout Screenshot of Bitcell, Height of bitcell: 486nm, Width of Bitcell: 108nm

<img width="897" height="662" alt="image" src="https://github.com/user-attachments/assets/338e7858-8a69-42e4-b433-030974e6a5ab" />


Bitcell Layout Challenges kept in mind while making Layout

    ► SRAM bit cell has half-cell schematic symmetry
          o Access
          o Pull down
          o Pull up
    ► Hence half-the bit cell layout to be drawn
    ► Bit lines and word lines passes across cells sharing their connections on boundaries.
    ► This half-cell has to be instantiated twice
          o On half-cell in R0
          o Other half-cell in My + Mx orientation
          o Keeping PMOS in center
          o Access NMOS BT and BC are shared on boundaries reducing bit line capacitance
          o Pulldowns NMOS VSS are shared on Boundaries
          o Pullup PMOS VDD are shared on Boundaries
          o WL connections are shared on Boundaries reducing WL capacitance.
    ► Bit lines are shielded on boundary as to avoid capacitance from neighbouring bit lines when placed in array
