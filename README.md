# Configurações e softwares instalados no Ubuntu

## Atribuir microfone default via linha de comando
- Listar os devices sources (entradas/microfone)
    - `pactl list short sources`
- Definir o microfone em execução
    - `pactl set-default-source alsa_input.usb-C-Media_Electronics_Inc._USB_Audio_Device-00.mono-fallback`
- Agendar no crontab no startup do sistema
    - `crontab -e`

        ```
        # Considere colocar o comando dentro do setAudioMicDefault.sh
        # Não esqueça de dar permissão de execução chmod +x
        @reboot sudo /home/setAudioMicDefault.sh &

        ```