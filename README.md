INSTALLATION TRAINING.
1)Go to https://colab.research.google.com.
2)Create a new project.
3)go to the files folder, it is located on the left side of the folder icon. Next, click on the leaf with an arrow and upload the required file.
4)install one by one: 1)pip install pydub
2)!apt install ffmpeg
3)pip install spleeter
4)from IPython.display import Audio
5)pip install -U openai-whisper.
5)pip install and run, execute what is shown to us:
1)from pydub import AudioSegment
from pydub import effects
vv = input("Enter the name of the file along with its extension:")
sound_before = AudioSegment.from_file(vv, "wav")
print('current dBFS: ', round(sound_before.dBFS, 1))
sound_after = effects.normalise(sound_before)
print('dBFS after normalisation: ', round(sound_after.dBFS, 1), '\n')
sound_after.export(vv, format="wav")
print("process complete")
2)!spleeter separate -o output/ 1.wav #change 1.wav to you audio file
3)#transfer the file with vocals
4)!whisper vocals.wav --model large-v2 #it is possible to change the resolution depending on the complexity of the audio file, 
#change large-v2 to: medium or large-v2 or large-v3. the older the model, the less errors, 
#but longer audio processing time. We recommend that if the file is small, not long and not complicated, 
#not noisy, use the initial model, and as the complexity increases, increase the model. 
#Also processing speed may depend on your PC.
