# GR Scheduler

http://www.trondeau.com/blog/2013/9/15/explaining-the-gnu-radio-scheduler.html

https://static1.squarespace.com/static/543ae9afe4b0c3b808d72acd/t/55ddd7f0e4b0b66ae5941808/1440602096261/10.+rondeau-how_not_to_write_a_block+2015-08-24.pdf

- noutput_items: minimum number of output available on all output buffers
- ninput_items: vector of items available on all input buffers
- gr::sync_block: ninput_items[i] = noutput_items
- gr::sync_decimator: ninput_items[i] = noutput_items*decimation()
- gr::sync_interpolator: ninput_items[i] = noutput_items/interpolation()

Default: ninput_items[i]=noutput_items+history()-1;


## forecast

we can utilize the forecast function to specify the number of input items.

## history

If you set the history to length N, the first N items in the input buffer include the N-1 previous ones (even though you've already consumed them).

That is for the FIR filter.

# Message Communication
## Message passing

## Tag
PDU: protocol data unit. 

## set and get parameter with gnuradio block

fft_vcc:

      virtual void set_nthreads(int n) = 0;
      virtual int nthreads() const = 0;

fft_vcc_impl

      void set_nthreads(int n);
      int nthreads() const;

fft_complex class

      /*!
       *  Set the number of threads to use for caclulation.
       */
      void set_nthreads(int n);

      /*!
       *  Get the number of threads being used by FFTW
       */
      int nthreads() const { return d_nthreads; }

fft_complex class implementation
      
    void
    fft_vcc_fftw::set_nthreads(int n)
    {
      d_fft->set_nthreads(n);
    }

    int
    fft_vcc_fftw::nthreads() const
    {
      return d_fft->nthreads();
    }
      
fft_complex implementation
    
    void
    fft_complex::set_nthreads(int n)
    {
      if (n <= 0) {
        throw std::out_of_range ("gr::fft: invalid number of threads");
      }
      d_nthreads = n;
    }

SWIG Problem:
Add callback parameter in the xml.

For some reason virtual header files don't get swig'ed again unless explicitly triggered. Just do a 'make clean' and 'make' again. That should rebuild your module from scratch and also swig your headers.

      make clean

# Digital Communication Moudle

## correllation and clock estimation
Modulator factor

# Debug

Utilize the virtual sink and virtual source to test the code first.
