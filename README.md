# l4d2coop

## �T�v

Left 4 dead 2��8�lcoop�p�̃v���O�C���A�ݒ�t�@�C�����܂Ƃ߂ē����i���łɓ�Փx�Ԃ��グ�j

���O��mod

�E[Metamod](http://www.metamodsource.net/)

�E[Sourcemod](http://www.sourcemod.net/)

�E[L4DToolZ](https://forums.alliedmods.net/showthread.php?t=93600)

�E[LEFT12DEAD](https://forums.alliedmods.net/showthread.php?t=126857) 

�E[L4D Idle Fix](https://chasethecore.run/?page_id=1121)

�E~~[L4D2 Defib Glitch Canceller](https://chasethecore.run/?page_id=821)~~

�E[DHooks](https://forums.alliedmods.net/showthread.php?p=2588686#post2588686)

�E[Defib_Fix](https://forums.alliedmods.net/showthread.php?t=315483)

�E[l4d player ver 0.07a](http://nico-op.forjp.net/doku.php?id=nicofile)

�E[Incapped Crawling with Animation](https://forums.alliedmods.net/showthread.php?p=1291588)

�E[[L4D2] LAST BOSS](https://forums.alliedmods.net/showthread.php?t=129013)

## �C���X�g�[�����@

### �T�[�o�̐ݒ�

#### �@[steamcmd](https://developer.valvesoftware.com/wiki/SteamCMD)���_�E�����[�h

#### �A�K���ȏꏊ��SteamCMD.exe���N����L4D2�T�[�o���C���X�g�[��

```
login anonymous
force_install_dir l4d2server
app_update 222860
```

#### �B�T�[�o���C���X�g�[�������t�H���_��left4dead2�t�H���_��start.bat������

git��Ȃ火����

```
git init
git remote add origin https://github.com/neohral/l4d2coop.git
git pull origin master
```

#### �C�T�[�o�n�̐ݒ������B

�Eleft4dead2\cfg\server.cfg

| �ݒ荀��                     | �ݒ�l                                   | �ݒ�l     |
| ---------------------------- | ---------------------------------------- | ---------- |
| hostname                     | �T�[�o�̖��O                             | l4d2server |
| sv_allow_lobby_connect_only  | 0�ɂ���ƃR���\�[������ڑ��ł���        | 0          |
| rcon_password                | �T�[�o�Ǘ��҂̃p�X���[�h                 | "password" |
| sv_lan                       | �l�b�g���[�N�ݒ�(0:�C���^�[�l�b�g 1:LAN) | 0          |
| sv_region                    | �n��ݒ�(4:�A�W�A)                       | 4          |
| sv_alltalk                   | �{�C�`���̐ݒ�(0:�����̂�1:�S�̂�)       | 0          |
| sm_cvar sv_force_unreserved  | ���ڃQ�[���ɎQ������                     | 1          |
| sm_cvar sv_visiblemaxplayers | �T�[�o��ʂŌ�����Q���l���i�����ڂ����j | **10**     |
| sm_cvar sv_removehumanlimit  | �Q������̃L�b�N�𖳌��ɂ���             | 1          |
| sm_cvar sv_maxplayers        | �ڑ��\�ȍő�l��                       | **10**     |
| sm_cvar l4d_maxplayers       | �ڑ��\�ȍő�l��(����Ȃ�����)         | **10**     |
| sm_cvar l4d_survivor_limit   | BOT���܂߂������҂̐l��                  | **10**     |
| sm_cvar l4d_infected_limit   | ���ꊴ���҂̍ő哯��������               | 20         |
| sm_cvar l4d_players_delay    | �Ȃɂ���(�Ƃ肠�����K�v����)             | 12         |
| sm_cvar l4d_players_kick     | �Ȃɂ���(�Ƃ肠�����K�v����)             | 0.7        |
| sm_cvar l4d_players_timer    | �Ȃɂ���(�Ƃ肠�����K�v����)             | 1.5        |

�l�����₷�Ȃ�A����������ς���

���̑����ꊴ���҂̐ݒ肠����͂����̂ŕ��ʂɂ��Ȃ�A�v����

#### �Dstart.bat���N������B

�N���I�v�V������ݒ肵�Asrcds.exe���N�������B

�Estart.bat

| �N���I�v�V����               | �T�v                               | �ݒ�l            |
| ---------------------------- | ---------------------------------- | ----------------- |
| -autoupdate                  | �N�����ɃA�b�v�f�[�g�`�F�b�N������ |                   |
| -console                     | CUI�R���\�[���ŋN������            |                   |
| +hostport                    | IP�|�[�g�ԍ����w�肷��             | 27016             |
| +map "�}�b�v�� �Q�[�����[�h" | �}�b�v�ƃQ�[�����[�h���w��         | "c1m1_hotel coop" |
| +maxplayers                  |                                    | **10**            |

�l�����₷�Ȃ�A����������ς���B

#### �E�R���\�[������ڑ�

connect `���[�J����IP�A�h���X`:`�|�[�g`

�����[�J����IP�A�h���X�̓��[�v�o�b�N�A�h���X(127.0.0.1)����Ȃ�����

�m�F���@�̓T�[�o��GUI�ŋN������IP�A�h���X�̂Ƃ��ɏo����

### �N���C�A���g�̐ݒ�

#### �@�R���\�[������ڑ�

connect `�O���[�o����IP�A�h���X`:`�|�[�g`

------------------



## ����

�E���O��`left4dead2\addons\sourcemod\logs`������ɏo�Ă���

�E[The Ultimate Mod Testing and Reviewing Area](https://steamcommunity.com/sharedfiles/filedetails/?id=469986973&searchtext=TUMTaRA)

## �Q�l

http://gengen5656.blog46.fc2.com/blog-entry-34.html

2011�N�̋L���Ȃ̂ŁA�C���X�g�[��������̂Ƃ��͍ŐV�̂������Ă����ق�������(1�s)