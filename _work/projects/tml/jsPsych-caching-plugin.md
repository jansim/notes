```js
import { initJsPsych } from 'jspsych'
import jsPsychHtmlKeyboardResponse from '@jspsych/plugin-html-keyboard-response'

import { conditionalCacheFunction, hasTrialInCache, retrieveTrialFromCache, storeTrialToCache, resetCache } from 'jsPsych-caching'

// TODO: How to insert / submit fake data? Has to be in jsPsych and pushkin data
// Maybe by generating a custom timeline with our own plugin? Ideally we would store the data as-is
// with a custom key to indicate it's coming from cache (the type should be the same to not mess with parsing scripts)

const jsPsych = initJsPsych();

const timeline = [
  {
    type: jsPsychHtmlKeyboardResponse,
    conditional_function: () => hasTrialInCache("language") && hasTrialInCache("country"),
    stimulus: () => {
      const languageData = retrieveTrialFromCache("language");
      const countryData = retrieveTrialFromCache("country");
      `It looks like you previously participated with the following data: ${languageData.language}, ${countryData.country}. Was this you?`
    },
    on_finish: (data) => {
      if (data.response == "Yes") {
        // Do nothing
      } else {
        // Someone else, remove data
        resetCache()
      }
    }
  },
	{
		type: jsPsychHtmlKeyboardResponse,
    // conditionalCacheFunction will evaluate to 'false' if there is data cached for this id
    // and will insert the latest stored trial's data instead
    conditional_function: conditionalCacheFunction({ id: 'language' }),
    on_finish: (data) => {
      storeTrialToCache(data)
    }
	},
  // OR
  cacheTrial({
    id: "language",
    trial: {
      type: jsPsychHtmlKeyboardResponse,
      on_finish: (data) => {
        storeTrialToCache(data)
      }
    }
  })
]
jsPsych.run(timeline);
```