---
Due: 2022-09-28
Label:
  - Classes
Status: Done
Priority: Medium
---
# To Do

- [x] HW1
- [x] Hw 2: make nice + turn in
- [x] Study
- [x] HW3
- [ ] HW5
- [x] STUDY

  

  

  

  

  

  

  

  

  

  

  

  

  

  

HW1

%% Problem 3  
b = 15;  
k = 0.5;

dt = 1;  
initial =10  
kvals = [-0.5,0.5,1.5,2.5]

endYear = 15;

figure('Name','Problem 4');  
hold on  
for index = 1:length(kvals)

```
k = kvals(index);xAxis = 0:dt:endYear;pointer = 2;time = 0;discrete = [initial];while (time < endYear)    pastVal = discrete(pointer - 1);    discrete(pointer) = pastVal - k *pastVal +b;    pointer = pointer + 1;    time = time + dt;endsubplot(2,2,index)scatter(xAxis, discrete, 'MarkerFaceColor','flat');title(strcat("k = ", num2str(k)))ylabel('Whale Population')xlabel('Time (Years)')
```

end

sgtitle('Bloodstream')  
hold off