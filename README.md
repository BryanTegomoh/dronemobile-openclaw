# dronemobile-openclaw

Control your DroneMobile vehicle from any OpenClaw agent.

Say "start my car", "lock it", "check battery" — the agent handles the rest.

## What it does

- Start / stop engine
- Lock / unlock doors
- Open trunk
- Check status (battery, temp, mileage, door state)

Works with any vehicle on the DroneMobile platform.

## Setup

Install the dependency:

```bash
pip install drone-mobile
```

Add your credentials to the OpenClaw env file:

```
DRONEMOBILE_EMAIL=your@email.com
DRONEMOBILE_PASSWORD=yourpassword
DRONEMOBILE_DEVICE_KEY=your_device_key
```

Find your device key in the DroneMobile app under vehicle settings.

## Usage

```bash
python dronemobile.py status
python dronemobile.py start
python dronemobile.py stop
python dronemobile.py lock
python dronemobile.py unlock
python dronemobile.py trunk
```

## Notes

Tested on a 2017 Audi Q7. The `drone-mobile` PyPI package uses `command_success` in the API response — see [PR #18](https://github.com/bjhiltbrand/drone_mobile_python/pull/18) for a fix to the upstream library.

## License

MIT
