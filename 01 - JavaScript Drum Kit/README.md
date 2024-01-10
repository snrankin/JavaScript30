# 01 - JavaScript Drum Kit

## PRE-VIDEO

I knew there had to be a class added an removed to the key when pressed. So I added two event listeners to the window.

The first one checked if the key that was pressed was in the group of keys found by the query selector `document.querySelector(.key[data-key="${event.keyCode}"]);`. If it was there then it would add the class `.playing` to the key and play the sound. Then when the key was released, it would remove the `.playing` class.

## POST-VDEO

After watching the tutorial, I learned that one of the biggest things I missed was not reseting the audio to the beginning every time the key was pressed. Without it, it meant that the sound associated with the key would only play for every key pressed AFTER it was finished, which isn't what we wanted.

I also learned that it was better to add the removal of the `.playing` class to the transition end event. Otherwise the class would remain there so long as the key was pressed.
