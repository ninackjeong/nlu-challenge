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
Extend the English JSGF development grammar ("jsgf_eng_basic_ruls.txt" under "eng") so that it can cover at least the following utterances.

```
[i want to listen to]<unk> [jazz]<genre> [music]<unk>
[play me]<unk> [ummagumma]<album> [by]<unk> [pink floyd]<artist>
[put]<unk> [lady gaga]<artist> [on]<unk>
```

## Task 2: Localize the JSGF grammar in your language (Korean, here)
Localize the extended English grammar from the above task in Korean.
Considerations
1. Korean is a SOV language
2. Korean utilizes case markers to mark case while English does syntactically
