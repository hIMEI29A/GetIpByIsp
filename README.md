# GetIpByIsp  
 
**Deprecated. See [Goranger](https://github.com/hIMEI29A/goranger).**

Simple cURL based console application for getting IP ranges from [https://suip.biz](https://suip.biz) web-services by city, country (very big size!! i'm really afraid) or ISP. In case of ISP you may specify single ip or web-site url of that provider as argument of script.

## Dependencies

* pear/console_commandline

## Installation

**Install via Composer:**

```shell
composer require himei/getIpbyIsp
```

**For manual installation clone repo**

```shell
git clone https://github.com/hIMEI29A/getIpbyIsp.git
```

**Follow to the root programm folder:**

```shell
cd getIpbyIsp
```

**Then install dependencies**

```shell
composer update

composer install
```

## Usage

**Follow to bin directory of root program folder:**

```shell
cd bin
```

**Make main program file executable:**

```shell
chmod +x getipbyisp
```

Now use it.

**Type next in your console for getting help:**

```shell
./getipbyisp -h
```

or

```shell
./getipbyisp --help
```

**The output:**

```shell
Console application for getting IP range 
from suip.biz web-services by city, country or ISP

Usage:
  getipbyisp [options] type request

Options:
  -o output, --output=output  File to store the result
                              
  -h, --help                  Show this help message and exit

Arguments:
  type     Set the type of which IP ranges will be requested: city, counrty or isp
           
  request  Request string: for country - 2-letter country code, for city - its name, for ISP - single IP or ISPs url
```
## Examples

To get all IP ranges of **Serbia**

```shell
./getipbyisp country RS
```

To get all IP ranges of **London** and save it to **file.txt**

```shell
./getipbyisp city london -o file.txt
```

To get all IP ranges of **Beeline** ISP

```shell
./getipbyisp isp beeline.ru
```

or

```shell
./getipbyisp isp 217.118.85.19
```

**Warning!!!** In case of request by city, write the name of the city **carefully and accurately**, as much as possible. If an error occurs in the name, the search on the uncleaned database is activated, and the result includes **ALL** IP ranges from **all** possible variants. To get the most accurate result, the city name **must not contain errors**.

## TODO

* Tests

## Contact

For bug reports or any other purpose you may contact me via email [himei at tuta dot io].

