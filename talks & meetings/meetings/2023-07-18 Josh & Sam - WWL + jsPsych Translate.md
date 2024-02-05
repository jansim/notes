---
creation date: 2023-07-18 10:02
---

## Notes going into
- Agenda
	- jsPsych Translate
		- lab.js translate?
		- Write a short reply paper on this?
	- WWL

```js
import jsPsychHtmlKeyboardResponse from '@jspsych/plugin-html-keyboard-response'
import { jsPsychSelectLanguageTrial, translate } from '@jspsych/translate'

const jsPsych = initJsPsych();

const timeline = [
	{
		type: jsPsychSelectLanguageTrial,
		availableLanguages: ['en', 'de'],
		defaultLanguage: 'en',
		fallbackLanguage: 'en',
		translations: {
			// Overall translations can be passed here or on the trials themselves
		}
	},
	{
		type: jsPsychHtmlKeyboardResponse,
		// should translate behave similar to timelineVariable() instead i.e. return a function?
	    stimulus: () => translate('Hello world!'),
	    translations: {
		    // These translations are only available on the trial
		    de: {
		        'Hello world!': 'Hallo Welt!'
		    }
	  }
	}
]
jsPsych.run(timeline);
```

- Further questions:
	- how to deal with `stimulus: translate('Test')`
		- should there be `translateNow()`
- 

## Notes during
- WWL
	- what does it cost to run this?
	- people want a single fee in the end
	- re-visiting cost of running it


## Summary

- Re translation / internationalization: https://www.w3.org/International/questions/qa-i18n

New Example Code

```js
import { initJsPsych, translate } from 'jspsych'
import jsPsychHtmlKeyboardResponse from '@jspsych/plugin-html-keyboard-response'
import jsPsychSelectLocale from '@jspsych/plugin-select-locale'
// 'jsPsych' should also export sth. like setLocale() which will be called within the plugin

// Properly supported locale / language formats: 'en' and 'en-US' / 'en-GB'
// [https://datatracker.ietf.org/doc/html/rfc5646](https://datatracker.ietf.org/doc/html/rfc5646)

const jsPsych = initJsPsych({
  // Default starting locale, if not set, use navigator.language
  defaultLocale: 'en',
  translations: {
    // Overall translations can be passed here or on the trials themselves
  }
});

const timeline = [
	{
		type: jsPsychSelectLocale,
		availableLocales: ['en', 'de'],
    // If I don't provide a translation in the selected locale, fallback locale will be returned
    // if there's no translation in that, the key will be returned as is
		fallbackLocale: 'en',
	},
	{
		type: jsPsychHtmlKeyboardResponse,
		// should translate behave similar to timelineVariable() instead i.e. return a function?
	    stimulus: () => translate('str_hello') + ' ' + translate('World!'),
	    translations: {
        // These translations are only available on the trial
        en: {
          'str_hello': 'Hello',
          // as there's no key for 'World!' it should be returned as is,
          // which is fine in this case
        },
		de: {
          'str_hello': 'Hallo',
          'World!': 'Welt!',
		}
	  }
	}
]
jsPsych.run(timeline);
