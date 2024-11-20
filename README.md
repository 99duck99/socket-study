# 1. 소켓 프로그래밍 소켓 관련 함수
## 리눅스함수
### <sys/socket.h>에 포함된 함수
int socket(int domain, int type, int protocol); // 소켓 생성함수
성공시 파일 디스크럽터, 실패시 -1반환

int bind(int sockfd, struct sockaddr *myaddr, socklen_t addrlen); // 소켓에 IP와 포트번호 할당
성공시 0, 실패시 -1 반환

int listen(int sockfd, int backlog); // 소켓을 연결요청 가능한 상태 전환
성공시 0 실패시 -1반환

int accept(int sockfd, struct sockaddr *addr, socklen_t *addrlen); // 연결요청에 대한 수락
성공시 파일 디스크럽터, 실패시 -1 반환
