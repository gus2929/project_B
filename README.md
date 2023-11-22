# project_B
<br/>
img_compressed2raw<br/>
aruco_node<br/>
map.pgm / map.pgm : 주차장 환경 맵<br/>
parking_lot : waypoint로 가는 코드<br/>
parking_lidar : 라이다 토픽(/scan)을 구독하여 특정각도(270)를 기준으로 물체(주차된 차량) 유무를 판단<br/>
parking_marker : 주차된 차가 있을 때 번호를 읽기 위해, ar_marker를 찾아 화면 중앙으로 정렬<br/>
parking_plate : 읽어들인 이미지를 영상처리 하여 번호판을 출력함<br/>


----------------------최종 ---------------------------------------------<br/>

1.지정한 좌표로 이동한다<br/>
2.정해진 좌표에 도착하면 라이다값을 읽는다.<br/>
 2-1 차가 없을 경우<br/>
    현재상태 파라미터를 html에 넘긴다(empty)<br/>
    다음포인트로 이동한다.<br/>
 2-2차가 있을경우<br/>
    현재상태 파라미터를 html에 넘긴다(busy)<br/>
    ar_marker를 찾는다.<br/>
    번호판을 인식하여 출력한다.<br/>
    현재상태(plate) 파라미터를 html에 넘긴다.<br/>
3. 주어진 파라미터를 기반으로 html을 출력한다.<br/> 

    
