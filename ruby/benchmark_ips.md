### Benchmark IPS

Benchmark IPS is a gem to benchmark your code snippets.
You can benchmark and compare two or more snippets of Ruby code.
It provides Iterations per second.

```ruby

    require 'benchmark/ips'

    Benchmark.ips do |x|
      x.config(:time => 5, :warmup => 2)

      x.time = 5
      x.warmup = 2

      x.report("report_1") do
        (('a'..'z').to_a + ('0'..'9').to_a).repeated_permutation(2).to_a.sample(1).join
      end

      x.report("report_2") do
        (('a'..'z').to_a + ('0'..'9').to_a).sample(2).join
      end

      x.compare!
    end
```

## Output

```
            report_1     1.000  i/100ms
            report_2     1.000  i/100ms
            -------------------------------------------------
            report_1      1.029  (± 0.0%) i/s -      6.000  in   5.835516s
            report_2     16.458  (± 6.1%) i/s -     82.000

            Comparison:

            report_2:       16.5 i/s
            report_1:        1.0 i/s - 16.00x slower
```
