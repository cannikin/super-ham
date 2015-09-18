Simple SDR receive and play over speaker with Raspberry Pi:

    sudo rtl_fm -f 144M -M wbfm -s 200000 -r 48000 -l 80 - | aplay -r 48k -f S16_LE

For some reason appears to have the best reception when the transmission offset by about +240,000 Hz. For example, telling it to listen at 441,000,000 Hz, causes it to say it's listening at 144316000 Hz but the best reception comes in at 144,520,000 Hz.
