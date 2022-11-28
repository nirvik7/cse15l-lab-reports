__Lab 5 Report__

```
DIR="./student-submission/"

rm -rf $DIR
git clone $1 $DIR -q

echo -e "Code Grader \n"

score=0
MUSTFILE="ListExamples.java"
TEST="TestListExamples.java"
TESTEX="TestListExamples"
CP=".:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar"

# Checking if file exists
if [ -f $DIR$MUSTFILE ]
then
    echo -e "File is present! [+2 points]"
    ((score=score+2))
else 
    echo -e "File was not found. [+0 points]"
    echo "Final Grade: 0/10"
    exit
fi

cp $TEST $DIR
cd $DIR
javac -cp $CP *.java 2> compile-err.txt

# Checking compilation
if [ $? -eq 0 ]
then
    echo "Compiled successfully! [+3 points]"
    ((score=score+3))
else 
    echo "Failed to compile. [+0 points]"
    echo "Final Grade: 2/10"
    exit
fi

java -cp $CP org.junit.runner.JUnitCore $TESTEX > test-err.txt

# Checking correctness
if [ $? -eq 0 ]
then
    echo "All tests passed successfully! [+5 points]"
    ((score=score+5))
else 
    echo "All tests were not successful... [+0 points]"
    echo "Check test-err.txt for more"
    grep -h "Failed Tests" test-err.txt
fi

echo "Final Grade: [$score/10]"
```
