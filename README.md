# _StringBetween
#include &lt;String.au3>  Func _RegExpStringBetween(Const $test, Const $start_pattern, Const $end_pattern, $fCase = False)     $fCase = ($fCase = Default) ? False : $fCase     $sCase = ($fCase = True) ? "(?s)" : "(?is)"      Local Const $start = StringRegExp($test, $sCase &amp; $start_pattern, 1)[0]     If @error Then Return SetError(1, 0, False)      Local Const $end = StringRegExp($test, $sCase &amp; $end_pattern, 1)[0]     If @error Then Return SetError(2, 0, False)      Return @error ? SetError(3, 0, False) : _StringBetween($test, $start, $end, $fCase) EndFunc
