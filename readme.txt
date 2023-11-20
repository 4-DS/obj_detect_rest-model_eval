------------------------------ MASSCAN ------------------------------

sudo apt install masscan

1)  sudo masscan -p 1-65535 -iL ip.txt -oL done.txt --max-rate 150000 -nmap
2)  sudo java -jar masscan.jar done.txt 1500 | tee "done2.txt"
3)  sudo java -jar qChecker.jar done2.txt 1500 | tee "done3.txt"


---------------------------- QUBOSCANNER ----------------------------

wget https://github.com/replydev/Quboscanner/releases/download/0.3.7/quboscanner-0.3.7-jar-with-dependencies.jar

1)  mv quboscanner-0.3.7-jar-with-dependencies.jar qubo.jar
2)  sudo java -Dfile.encoding=UTF-8 --enable-preview -jar qubo.jar -range [IP] -ports [PORTS] -th 1000 -ti 1000

-------------------------------- END --------------------------------