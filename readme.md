Code for Ramanujan Number in SimpleRisc Format -- 

.count_Increase
    add count, count , 1
.exit

mov count , 0
mov r1 , 1

.loop:
    mov r2 ,1 
    mov r3 , 1

.loop1:
    .loop2:
        mul r4 , r2 , r2
        mul r5 , r4 , r2
        mul r6 , r3 , r3
        mul r6 , r6 , r3
        add r6 , r6, r5
        cmp r6 , r1
        beq .count_increase
        
        add r3 , r3 , 1
        cmp r3 ,r1
        blt.loop2

        add r2 , r2 , 1
        cmp r2 , r1
        blt .loop1

        cmp count , 2
        bgt. exit

add r1 , r1 , 1
exit
mov count , 0