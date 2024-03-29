## Dklodd for operating CTF system challenge with docker

[TJCSec/klodd](https://github.com/TJCSec/klodd)을 k8s 없이 운용할 수 있도록 만든 프로젝트입니다.
TJCsec과 아무런 연관이 없으며 단독적인 프로젝트임을 밝힙니다.

This is a project created to enable TJCSec/klodd to be operated without k8s.
We would like to clarify that this is an independent project and has no connection with TJCsec.

우아하게 설정된 단독 traefik와 하나의 머신 또는 VM에서 동작하도록 설계되었습니다.

기존의 nc 명령어 대신 ncat, socat, openssl를 사용하여 ssl 접속을 허용합니다.

## [dome service](https://dklodd.minpeter.tech)

- mathematian-in-wonderland: [dklodd.minpeter.tech/0](https://dklodd.minpeter.tech/0)
- admin panel: [dklodd.minpeter.tech/admin](https://dklodd.minpeter.tech/admin) (admin:admin)

### How to use

아직 실험적인 단계이므로, 사용에 주의가 필요합니다.

```bash
make dev
```

실제로 서비스를 이용하기 위해선 <dklodd.traefik.me:8080>에 접속하여 사용할 수 있습니다.

---

실제 서비스를 위해선 sidecar-compose.yml과 [minpeter/homelab_infra](https://github.com/minpeter/homelab_infra)의 traefik을 이용하여 외부에서 접속할 수 있도록 설정해야 합니다. 이때 `infra-config/sidecar-compose.yml`를 사용하여 서비스를 실행하면 됩니다.

### shutdown all containers

```bash
make down
```

## photo
![image](https://github.com/minpeter/dklodd/assets/62207008/6fd5c64a-9e11-4452-bad6-10b772654c09)
![image](https://github.com/minpeter/dklodd/assets/62207008/4c7ead83-4927-4e80-a1e9-7b2d42bbb423)
