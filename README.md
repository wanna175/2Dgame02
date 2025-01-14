🕹️ RPG 게임
FSM(유한 상태 기계)을 기반으로 플레이어의 행동을 제어하며, 다양한 기능과 시스템을 갖춘 RPG 게임입니다. 싱글톤 패턴과 JSON 파일을 활용하여 데이터 관리 및 게임의 연속성을 유지합니다.

🎮 01. RPG 게임 - Player 시스템
플레이어 행동 제어
**FSM(유한 상태 기계)**을 기반으로 플레이어의 행동을 제어합니다.
각각의 캐릭터는 BasePlayer 클래스를 상속받아 동작하며, 이는 **프리팹(Prefab)**으로 저장되어 있습니다.
<img src="https://raw.githubusercontent.com/your-repo/path/to/player-action.png" alt="플레이어 행동 제어" width="600"/>
PlayerManager와 데이터 관리
PlayerManager는 싱글톤(Singleton) 객체로, 플레이어 데이터를 관리합니다.
데이터 유지: 씬 전환 시에도 데이터가 유지되도록 설계되었습니다.
데이터 불러오기: 게임 시작 시 DataManager 싱글톤 객체가 JSON 파일을 읽어와 캐릭터 슬롯을 보여줍니다.
선택된 캐릭터 관리: 캐릭터 선택 후 PlayerManager에 정보가 저장됩니다.
<img src="https://raw.githubusercontent.com/your-repo/path/to/character-selection.png" alt="캐릭터 데이터 관리" width="600"/>
씬 전환과 플레이어 배치
플레이어가 다른 맵으로 이동할 때마다 SceneManager가 PlayerManager를 참조하여 로딩 중에 새로운 플레이어를 생성하고 배치합니다.
<img src="https://raw.githubusercontent.com/your-repo/path/to/scene-transition.png" alt="씬 전환 시 플레이어 배치" width="600"/>
🛠️ 02. RPG 게임 - 다른 기능들
데미지 스킨
데미지 숫자는 텍스트가 아니라 스프라이트로 출력됩니다.
데미지 값을 int로 분리한 후, 해당 값에 맞는 스프라이트를 매칭하여 출력합니다.
크리티컬 데미지: 일정 확률로 크리티컬 데미지를 표현합니다.
<img src="https://raw.githubusercontent.com/your-repo/path/to/damage-skin.png" alt="데미지 스킨" width="600"/>
정보창
사용자가 획득한 아이템이나 경험치 정보를 출력합니다.
직관적인 UI를 통해 게임 정보를 확인할 수 있습니다.
<img src="https://raw.githubusercontent.com/your-repo/path/to/info-window.png" alt="정보창" width="600"/>
인벤토리 시스템
아이템 버리기: 불필요한 아이템을 선택적으로 버릴 수 있습니다.
아이템 사용: 선택한 아이템을 바로 사용할 수 있도록 구현되었습니다.
<img src="https://raw.githubusercontent.com/your-repo/path/to/inventory.png" alt="인벤토리" width="600"/>



 
