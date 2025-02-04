[![Build Status](https://travis-ci.org/parlr/chinese-data.svg?branch=master)](https://travis-ci.org/parlr/chinese-data)

# chinese-data

> Extract data from Unihan database as JSON

## Usage

Filter codepoint from raw database

	toggleValues="U+4E00,U+9FFF,U+3400,U+4DBF,U+20000,U+2A6DF,U+2A700,U+2B73F,U+2B740,U+2B81F,U+2B820,U+2CEAF,U+F900,U+FAFF"
	awk \
		-f src/chinese.awk \
		-v toggleValues="$toggleValues" \
	   src/Unihan_Readings.txt \
	> src/codepoint-ruby.tsv

Generate JSON file

	yarn start
	# copy to ruby-font-creator directory
	cp src/codepoint-ruby.json ../src/data.json

## License

> [Apache License 2.0](http://choosealicense.com/licenses/apache-2.0/)
// [CC-BY-SA-4.0 ](https://choosealicense.com/licenses/cc-by-sa-4.0/)
