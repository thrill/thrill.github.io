---
title: Word Count Example
bg: "#F5C45E"
color: black
"fa-icon": sun-o
published: true
---

This C++ snippet shows our (unoptimized) working example of Word Count in Thrill.

{% highlight cpp linenos=table %}
using namespace thrill;

size_t WordCountExample(Context& ctx) {

    auto lines = ReadLines(ctx, "wordcount.in");

    auto word_pairs = lines.template FlatMap<WordCountPair>(
        [](const std::string& line, auto emit) -> void {
                /* map lambda: emit each word */
            for (const std::string& word : common::split(line, ' ')) {
                if (word.size() != 0)
                    emit(WordCountPair(word, 1));
            }
        });

    auto red_words =  word_pairs.ReduceBy(
        [](const WordCountPair& in) -> std::string {
            /* reduction key: the word string */
            return in.first;
        },
        [](const WordCountPair& a, const WordCountPair& b) -> WordCountPair {
            /* associative reduction operator: add counters */
            return WordCountPair(a.first, a.second + b.second);
        });

    red_words.Map(
        [](const WordCountPair& wc) {
            return wc.first + ": " + std::to_string(wc.second);
        })
    .WriteLinesMany(
        "wordcount_" + std::to_string(ctx.my_rank()) + ".out");

    return 0;
}

int main(int argc, char* argv[]) {
    return api::Run(WordCountExample);
}
{% endhighlight %}
