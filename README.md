# A Natural Language Understanding Task: JSGF Development using Python

The following is a Context Free Grammar, written using the Java Speech Grammar Format (JSGF)

```
 #JSGF V1.0 utf-8 en;
 grammar music_play;

 public <music_play> =
	[can you] (play | put on) (<artist> | <song>);

 <artist> =
	 the beatles |
	 radio head |
	 lady gaga |
	 pink floyd;

 <song> =
	 comfortably numb |
	 paranoid android |
	 let it be |
	 hey jude;
```
This grammar creates utterances that express the desire or intent to play music. Then, they are used as training data for statistical models for intent recognition. This grammar can generate utterances using a custom parser as follows:

```
[can you play]<unk> [the beatles]<artist>
[can you put on]<unk> [paranoid android]<song>
```

## Task 1: Extend the English Grammar
