__Lab 5 Report__

```
DIR="./student-submission/"

rm -rf $DIR
git clone $1 $DIR

echo -e "\n"

score=0
MUSTFILE="ListExamples.java"
MAXIMUMCREDIT=5
SOURCETEST="TestListExamples.java"
SOURCETESTEXEC="TestListExamples"
## note here we use .. to go up one level to reach the lib folder
CPATH=".:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar"

# Checking the existance of the file
if [ -f $DIRNAME$MUSTFILE ]
then
    echo -e "The file" $MUSTFILE "in the directory " $DIR "is present [+1 point]"
    ((score++))
else 
    echo -e "The file" $MUSTFILE "in the directory " $DIR "is not present [+0 points]"
    echo "Final Grade: [$score/4]"
    exit
fi

cp $SOURCETEST $DIRNAME
cd $DIR
javac -cp $CPATH *.java 2> compile-err.txt

# Checking the compilation of the file
if [ $? -eq 0 ]
then
    echo "The compilation of the directory" $DIR "was successfull [+1 point]"
    ((score++))
else 
    echo "The compilation of the directory" $DIR "failed [+0 points]"
    echo "Final Grade: [$score/4]"
    exit
fi

java -cp $CPATH org.junit.runner.JUnitCore $SOURCETESTEXEC > test-err.txt

# Checking the correctness of the file
if [ $? -eq 0 ]
then
    echo "All the tests within" $SOURCETEST "were successfull [+1 point]"
    # as we have 2 tests
    ((score=score+2))
else 
    echo "Some the tests within" $SOURCETEST "were not successfull [+0 points]"
    echo "Check test-err.txt for understanding"
    grep -h "Failures" test-err.txt
fi

echo "Final Grade: [$score/4]"
```
