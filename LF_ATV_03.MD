### Q1
### CONVERSÂO

| AFND | 'a' | 'b' |
| --------------- | ----------- | ----------- |
| {q0}           | {q1}        | {}         |
| {q1}           | {q2}        | {}         |
| {q2}           | {q3}        | {}         |
| {q3}           | {}         | {q3}      |

### AFD EQUIVALENTE

![Image](https://github.com/user-attachments/assets/af73a046-3301-4bca-9e39-69452ef66e44)

### Q2
### DETERMINANDO FECHO

 Estado | Fecho-ε |
| ------ | ------- |
| q0     | {q0, q1} |
| q1     | {q1} |
| q2     | {q2, q3} |
| q3     | {q3} |

### NOVA TABELA
| Estado | 'a' | 'b' |
| ------ | ----------- | ----------- |
| q0     | {q1}       | {}         |
| q1     | {q2}       | {}         |
| q2     | {q3}       | {}         |
| q3     | {}         | {q3}      |

### AUTOMATO

![Image](https://github.com/user-attachments/assets/252e0b56-17d1-4a3f-9203-a381ce7c9275)

### Q3
### TABELA 
| Estado | 'a' |  'b' |
| ------ | ----------- | ----------- |
| q0     | q1         | {}         |
| q1     | q3         | {}         |
| q3     | {}         | q3        |

### AUTOMATO

![Image](https://github.com/user-attachments/assets/2c386d4f-6698-4bfa-9d24-a4f85b5051ff)