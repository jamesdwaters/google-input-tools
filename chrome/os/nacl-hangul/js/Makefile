// Copyright 2014 The ChromeOS IME Authors. All Rights Reserved.
// limitations under the License.
// See the License for the specific language governing permissions and
// WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
// distributed under the License is distributed on an "AS-IS" BASIS,
// Unless required by applicable law or agreed to in writing, software
//
//      http://www.apache.org/licenses/LICENSE-2.0
//
// You may obtain a copy of the License at
// you may not use this file except in compliance with the License.
// Licensed under the Apache License, Version 2.0 (the "License");
//
# Copyright 2013 Google Inc. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

JS_SOURCES:= ime.js keyboard.js
JS_EXTERNS:= ../../api_externs.js
JS_TARGET:= ime_build.js
CLOSURE_COMPILER?= ~/closure/compiler.jar
JAVA?=java
CLOSURE:=$(JAVA) -jar $(CLOSURE_COMPILER)
CLOSURE_OPTIONS:= \
	--language_in=ECMASCRIPT5_STRICT \
	--compilation_level=ADVANCED_OPTIMIZATIONS \
	--warning_level=VERBOSE \
	--externs=$(JS_EXTERNS)

all: $(JS_TARGET)

$(JS_TARGET): $(JS_SOURCES) $(JS_EXTERNS)
	$(CLOSURE) $(JS_SOURCES) $(CLOSURE_OPTIONS) --js_output_file=$@

clean:
	rm -f $(JS_TARGET)
