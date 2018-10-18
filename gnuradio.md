1. GR Scheduler

http://www.trondeau.com/blog/2013/9/15/explaining-the-gnu-radio-scheduler.html

https://static1.squarespace.com/static/543ae9afe4b0c3b808d72acd/t/55ddd7f0e4b0b66ae5941808/1440602096261/10.+rondeau-how_not_to_write_a_block+2015-08-24.pdf

- noutput_items: minimum number of output available on all output buffers
- ninput_items: vector of items available on all input buffers
- gr::sync_block: ninput_items[i] = noutput_items
- gr::sync_decimator: ninput_items[i] = noutput_items*decimation()
- gr::sync_interpolator: ninput_items[i] = noutput_items/interpolation()

wptr

Default: ninput_items[i]=noutput_items+history()-1;
