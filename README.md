# Manual de Instruções para Utilização do Notebook Jupyter

Este manual descreve como utilizar as funções interativas desenvolvidas no notebook Jupyter disponível no GitHub. O notebook oferece diversas técnicas de modulação e efeitos de áudio, permitindo ajustes em tempo real com sliders e widgets. O notebook pode ser executado tanto no ambiente Jupyter quanto no Google Colab.

## 1. Introdução

O notebook contém funções para explorar diferentes técnicas de modulação e efeitos de áudio. Cada técnica pode ser ajustada interativamente para observar o impacto das alterações nos sinais.

## 2. Bibliotecas Necessárias

Para garantir que todas as funcionalidades do notebook funcionem corretamente, você deve instalar as seguintes bibliotecas Python:

- **NumPy**: Para operações matemáticas e manipulação de arrays.
- **SciPy**: Para processamento de sinais e funções adicionais de matemática.
- **Matplotlib**: Para visualização gráfica dos sinais e efeitos.
- **IPython**: Para widgets interativos e integração com Jupyter.
- **librosa**: Para processamento e análise de áudio.
- **soundfile**: Para leitura e escrita de arquivos de áudio.
- **wavio**: Para leitura e escrita de arquivos WAV.




## 3. Modulação em Fase (PM)

**Descrição**  
Permite ajustar as frequências da portadora e do sinal de mensagem, e observar as mudanças no sinal resultante.

**Parâmetros**  
- `carrier_frequency`: Frequência da portadora (50 Hz a 500 Hz).  
- `message_frequency`: Frequência do sinal de mensagem (1 Hz a 50 Hz).

**Resultados**  
- Gráficos dos sinais de mensagem e portadora.  
- Sinal modulado em fase e seu espectro de frequência.

## 4. Modulação e Demodulação AM

**Descrição**  
Explora a modulação em amplitude (AM) e sua demodulação com um filtro passa-baixa.

**Parâmetros**  
- `freq_modulante`: Frequência do sinal modulante (1 MHz a 200 MHz).  
- `freq_portadora`: Frequência da portadora (100 MHz a 2000 MHz).  
- `amplitude_modulante`: Amplitude do sinal modulante (0.1 a 10).  
- `profundidade_modulacao`: Profundidade da modulação (0 a 1.0).

**Resultados**  
- Sinal modulante, sinal da portadora e sinal modulado.  
- Sinal demodulado e seu espectro de frequência.

## 5. Modulação em Banda Lateral Única (SSB)

**Descrição**  
Permite explorar a modulação de sinais com técnica SSB, gerando sinais de banda lateral superior (USB) e inferior (LSB).

**Parâmetros**  
- `fs`: Frequência de amostragem (100 Hz a 5000 Hz).  
- `fc`: Frequência da portadora (100 Hz a 2000 Hz).  
- `xlim`: Limite do eixo x para visualização (0.001 s a 0.1 s).

**Resultados**  
- Sinal de áudio, sinais USB e LSB.  
- Sinal modulado e seu espectro de frequência.

## 6. Modulação em Anel

**Descrição**  
A modulação em anel é uma técnica onde um sinal de mensagem modula um sinal portador através da multiplicação, resultando em dois sinais laterais que podem ser filtrados.

**Parâmetros**  
- `carrier_freq`: Frequência da portadora (1 Hz a 100 Hz).  
- `modulating_freq`: Frequência do sinal modulante (1 Hz a 100 Hz).  
- `modulation_index`: Índice de modulação, ajustável de 0 a 2.

**Resultados**  
- Gráficos do sinal original, sinal modulado e seu espectro de frequência.  
- Comparação entre o sinal modulado e o sinal filtrado.

## 7. Modulação em Frequência (FM)

**Descrição**  
A modulação em frequência altera a frequência da portadora com base no sinal modulante. Este módulo permite explorar como a frequência de modulação afeta o sinal.

**Parâmetros**  
- `carrier_freq`: Frequência da portadora (50 Hz a 500 Hz).  
- `modulating_freq`: Frequência do sinal modulante (1 Hz a 50 Hz). 

**Resultados**  
- Gráficos dos sinais de portadora, modulante e sinal modulado em frequência.  
- Espectro de frequência do sinal modulado.

## 8. Efeito Vibrato

**Descrição**  
Adiciona um efeito vibrato ao áudio, variando a altura do tom.

**Parâmetros**  
- `modfreq`: Frequência do vibrato (1 Hz a 10 Hz).  
- `width`: Largura do efeito vibrato (0.001 s a 0.05 s).

**Resultados**  
- Sinal de áudio original e com efeito vibrato.  
- Áudio modificado para reprodução.

## 9. Efeito Estéreo Phaser

**Descrição**  
Aplica um efeito de phaser estéreo ao áudio, variando a fase entre os canais esquerdo e direito.

**Parâmetros**  
- `carrier_freq`: Frequência da portadora (0.1 Hz a 10 Hz).  
- `depth`: Profundidade do efeito (0.0 a 1.0).  
- `frequency`: Frequência do LFO (0.1 Hz a 5.0 Hz).  
- `feedback`: Feedback do efeito (0.0 a 1.0).

**Resultados**  
- Sinal original e processado pelos canais esquerdo e direito.  
- Áudio modificado para reprodução.

## 10. Efeito Leslie

**Descrição**  
Simula o efeito de um alto-falante rotativo Leslie ao áudio.

**Parâmetros**  
- `model`: Modelo do Leslie (122, 122A, 147).  
- `hpf_cutoff`: Corte do filtro passa-alta (0 Hz a 200 Hz).  
- `volume`: Volume do efeito (0 a 10).  
- `gain`: Ganho do efeito (0 a 10).

**Resultados**  
- Sinal original e com efeito Leslie.  
- Comparação entre o sinal original e modulado.

## 11. Efeito Tremolo

**Descrição**  
Modula a intensidade do áudio de forma cíclica, criando variações no volume.

**Parâmetros**  
- `rate`: Frequência da modulação do tremolo.  
- `depth`: Intensidade da modulação.

**Resultados**  
- Sinal original e com efeito tremolo.  
- Áudio modificado para reprodução.

## 12. Efeito Vocoder

**Descrição**  
Combina dois sinais de áudio para criar um som sintetizado usando modulação de banda.

**Parâmetros**  
- `modulator_file`: Arquivo de áudio para o sinal modulador (em WAV).  
- `carrier_file`: Arquivo de áudio para o sinal portador (em WAV).

**Resultados**  
- Sinal original e sintetizado.  
- Áudio resultante para reprodução.

## 13. Arquivos de Áudio

Para testar os efeitos e modulações descritos, utilize os seguintes arquivos de áudio disponíveis no repositório GitHub:

- `guitar.wav`: Arquivo de áudio de guitarra para efeitos como vibrato e phaser estéreo.  
- `child-voice-sound.wav`: Arquivo de áudio de voz infantil para modulação SSB.
- `modulator.wav`: Arquivo de áudio para o sinal modulador no efeito Vocoder.
- `carrier.wav`: Arquivo de áudio para o sinal portador no efeito Vocoder.

**Sugestões de Utilização**  
- **Efeito Vibrato**: Use `guitar.wav` para observar o impacto do vibrato na guitarra.  
- **Efeito Estéreo Phaser**: Aplique em `guitar.wav` para experimentar o efeito de phaser estéreo.
- **Efeito Tremolo**: Utilize `guitar.wav` para testar o efeito de tremolo.
- 
- **Modulação SSB**: Utilize `child-voice-sound.wav` para visualizar como a modulação SSB afeta a voz.
- **Efeito Vocoder**: Use `modulator.wav` e `carrier.wav` para combinar os sinais e criar um som sintetizado com modulação de banda.

## 14. Referências

- Sammy Guo - GraphicsHikingAboutPhotography. Channel Vocoder Adventure, Feb 6, 2020. Disponível em: [GitHub - vocoder.py](https://github.com/sammyguo/vocoder.py)  
- Lucas Nedel Kirsten. Digital Implementation of Leslie Speaker. 2018.

### Instalando as Bibliotecas

Você pode instalar todas as bibliotecas necessárias usando o pip. Execute o seguinte comando no terminal:

```
pip install numpy scipy matplotlib ipython librosa soundfile wavio ```
