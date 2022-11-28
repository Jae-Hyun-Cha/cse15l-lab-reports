# __Lab Report5 (Week 9)__

grade.sh (Code Block)

```
rm -rf student-submission
git clone $1 student-submission
echo "Finished cloning"

cd student-submission
Score=0

if [[ ! -f ListExamples.java ]]
then 
    echo "File has not been found!"
    echo "------------------------------"
    echo "Score : [$Score / 3 points]"
    exit 1

else 
   echo "ListExamples.java found! [+ 1point]"
   ((Score+=1))
fi

cd ..
cp TestListExamples.java student-submission/
cp -r lib student-submission/
cd student-submission/
javac -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar *.java

if [[ $? -ne 0 ]]
then
  echo "Compile Error!"
  echo "------------------------------"
  echo "Score : [$Score / 3 points]"
  exit 1

else
   echo "File has been compiled! [+ 1point]"
   ((Score+=1))
fi

java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples

if [[ $? -ne 0 ]]
then
  echo "Failed tests"
  echo "------------------------------"
  echo "Score : [$Score / 3 points]"
  exit 1
else
  echo "Passed all tests [+ 1point]"
  ((Score+=1))
  echo "------------------------------"
  echo "Score : [$Score/3 points]"
  exit 0
fi
```

Three Screenshot

![Image](filename.png)

![Image](fileerror.png)

![Image](filecorrect.png)


Pick One Example and Explain

