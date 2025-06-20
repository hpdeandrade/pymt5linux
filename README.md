# pymt5linux
Welcome to pymt5linux repository!

**Forked from [lucas-campagna/mt5linux](https://github.com/lucas-campagna/mt5linux)**. This is a up-to-date version which incorporates recent MT5 software updates. It works with Python 3.13.

**Check out [mt5docker](https://github.com/hpdeandrade/mt5docker)**. It is also possible to run pymt5linux embedded in a Docker image that runs MT5 with x11/noVNC remote access.

Before stepping into the below, I strongly recommend you to check MetaQuotes' [official Python MQL5 documentation](https://www.mql5.com/en/docs/python_metatrader5).

## How To Use
1\. As per [MT5 Linux user guide](https://www.metatrader5.com/en/terminal/help/start_advanced/install_linux), install:
- [Wine](https://www.winehq.org) in your Linux machine.
- [Python for Windows](https://www.python.org) inside Wine.
- [MT5 client terminal for Windows](https://www.metatrader5.com) inside Wine.
    
2\. In your Windows environment (Wine), install the following packages:

```
pip install MetaTrader5 pymt5linux
```

3\. In your Linux environment, install the following packages:

```
pip install pymt5linux
```

4\. In your Windows environment (Wine), open the MT5 client terminal and run the server:

```
python -m pymt5linux --host localhost --port 8001 <path/to/python.exe>
```

5\. In your Linux environment, run your Linux script.

```python
# establish connection to MT5
from pymt5linux import MetaTrader5
mt5 = MetaTrader5(host="localhost", port=8001)
```

6\. Make sure you test with a DEMO account first, then have fun!