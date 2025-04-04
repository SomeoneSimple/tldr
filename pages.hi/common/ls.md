# ls

> डायरेक्टरी की सामग्री की सूची दिखाएं।
> अधिक जानकारी: <https://www.gnu.org/software/coreutils/manual/html_node/ls-invocation.html>।

- एक प्रति पंक्ति फ़ाइलों की सूची दिखाएं:

`ls -1`

- सभी फ़ाइलें दिखाएं, छुपी हुई फ़ाइलें समेत:

`ls {{[-a|--all]}}`

- सभी फ़ाइलों की सूची दिखाएं, जहाँ नामों के आखिर में `/` जोड़ा गया है:

`ls {{[-F|--classify]}}`

- सभी फ़ाइलों की लॉन्ग सूची (अनुमतियाँ, स्वामित्व, आकार, और संशोधन तिथि) दिखाएं:

`ls {{[-la|--all -l]}}`

- लॉन्ग सूची जिसमें ह्यूमन-रीडेबल इकाइयों (KiB, MiB, GiB) का उपयोग करके आकार दिखाया गया है:

`ls {{[-lh|-l --human-readable]}}`

- आकार के आधार पर क्रमबद्ध की गई लॉन्ग सूची (अवरोही):

`ls {{-lSR|-lS --recursive}}`

- संशोधन तिथि के क्रम में क्रमबद्ध की गई सभी फ़ाइलों की लॉन्ग सूची (सबसे पुरानी पहले):

`ls {{[-ltr|-lt --reverse]}}`

- केवल डायरेक्टरी दिखाएं:

`ls {{[-d|--directory]}} */`
