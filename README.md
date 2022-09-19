#                             Online Bash Shell.
#                 Code, Compile, Run and Debug Bash script online.
# Write your code in this editor and press "Run" button to execute it.


# echo "file version: $fileversion" 
# not working command prompt argument not working online



# taking fileversion as argument
#storing it into an array zoo
#converting it into an array of characters
#taking list of versions in myArray
#converting them into an array of characters
#storing them into an array foo 
#using if condition to check whether a greater fileversion is available
#checking by iterating over each element and checking if its greater
#if greater then print it
#if not greater then dont print continue checking
#if available printing them



read fileversion
 zoo=$fileversion
#for (( i=0; i<${#zoo}; i++ )); do
 # echo "${zoo:$i:1}"                       #foo is array of characters
#done  

myArray=("2.1.1" "2.1.5" "2.1.10" "2.1.11" "2.1.18" "2.2.0" "2.2.20" "2.2.10" "2.4.5" "3.1.0" "3.1.6" "3.1.1" "3.1.13")
    
#my array is array of strings

#processing array
for i in ${!myArray[@]}; do

  foo=${myArray[$i]}
for (( i=0; i<${#foo}; i++ )); do

  if [ "${zoo:$i:1}" < "${foo:$i:1}" ]; then    #if smaller then print
  
if [ "${zoo:$i:1}" = "3" ]; then    #if smaller then print
  
  echo "file latest major version is 3"
fi
  echo "${myArray[$i]}"
fi
done  
done
  echo "------"
  
  #untouched working
  <<c
  
  for i in ${!myArray[@]}; do

  foo=${myArray[$i]}
for (( i=0; i<${#foo}; i++ )); do
  echo "${foo:$i:1}"    #foo is array of characters
done  
done
  echo "------"



  
  
  
  
  
  
