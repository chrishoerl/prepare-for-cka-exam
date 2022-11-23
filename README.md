# Certified Kubernetes Administrator Exam (CKA)

## My badge
<a href="https://www.credly.com/badges/5ae8fb96-13ee-41e0-96f3-fd445c37e794/public_url">
  <img src="https://images.credly.com/size/340x340/images/8b8ed108-e77d-4396-ac59-2504583b9d54/cka_from_cncfsite__281_29.png">
</a>

## How I prepared for it in August 2021

### My situation:
* 2 years of professional experience with K8s
* 17 years of professional experience in Linux

### Kubernetes Version
My exam was performed on K8s v1.21

### Material / Courses
* **Kubernetes Documentation**: it is a valuable pool of information and its search function also finds bash commands such as: "busybox while true"
As it is the most important resource during the exam, I forced myself to solve my problems with tips and examples from the official docs.

https://kubernetes.io/docs/

* **Udemy Course**: "Certified Kubernetes Administrator (CKA) with Practice Tests"

https://www.udemy.com/share/101WmE/

* **killer.sh** is now included free for all exam attendees on enrollment process

https://killer.sh/cka

### Timeline
* took a whole of 2 months for preparation
* started with Udemy course and completed all the videos (18.5 hours) and practice tests (~10-15 hours)


* then took a few days of


* then repeated some Udemy videos I was not so self-confident with
* then repeated all Udemy practice tests for the 2nd time
* repeated the 3 mock exams on Udemy 3 times each to become faster


* scheduled the date for my exam (2 weeks ahead on a Sunday afternoon)
* again repeated some Udemy videos which I had not fully understood

### In the last week before the exam:
* **Monday**: did my first of two killer.sh sessions and performed badly (27%)
* **Tuesday**: reworked all Questions and Answers of killer.sh (without timer) to understand each solution
* **Wednesday**: picked a few Questions from killer.sh and tested them on my own local K8s cluster
* **Thursday**: took a day off
* **Friday**: started my 2nd killer.sh session and performed properly (around 90%) - I already knew the solutions from first run but this time I did it for a better feeling of time management
* **Saturday**: reworked a few Questions from killer.sh again
* **Sunday**: summit day.... erm... exam day. - Had a good feeling afterwards.
* **Monday**: Got my result: Passed!

### Tools

I use:
* kubectl autocompletion

I do not use:
* terminal managers such as tmux, just a plain single terminal
* command aliases for kubectl such as k=kubectl because I want to have clear commands other can also understand

### Favorite K8s shortcuts

This is a list of my favorite and most-used links and examples for creating K8s objects.

* Create a container to test other pods and services:
```
kubectl run curl --image=radial/busyboxplus:curl -i --tty
```

* Run a command in a shell:
```
command: ["/bin/sh"]
args: ["-c", "while true; do echo hello; sleep 10;done"]
```

* Create a pod in a 1-liner
```
kubectl run mypod --image=nginx --dry-run=client -o yaml > mypod.yml
kubectl -n default apply -f mypod.yml
kubectl -n default get po
```

* API resources 
```
kubectl api-resources
kubectl api-resources --namespaced=true
kubectl api-resources --namespaced=false
```

* Explain K8s objects

If you want to know the object structure of pods:
```
kubectl explain pods --recursive  | wc -l
996 #note this number!

kubectl explain pods --recursive  | grep image -b996

# this will color-mark the object in the given structure you were looking for.
# This helps to build structured commands for jsonpath! 
```

### Favorite links

* kubectl Cheat Sheet

  https://kubernetes.io/docs/reference/kubectl/cheatsheet/

* Configure a Pod to Use a Volume for Storage

  https://kubernetes.io/docs/tasks/configure-pod-container/configure-volume-storage/

* Configure a Pod to Use a PersistentVolume for Storage

  https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/

* Network Policy

  https://kubernetes.io/docs/concepts/services-networking/network-policies/#networkpolicy-resource

* Security Context

  https://kubernetes.io/docs/tasks/configure-pod-container/security-context/


### Environment
I set up my own local K8s cluster on a notebook

Tutorial: https://github.com/chrishoerl/k8s-play

### My desk for the exam day
* notebook with lid closed (it plays audio in case the proctor wants to say something)
* big 21:9 wide screen in the center to have 2 browser tabs besides each other (1 for exam terminal and 1 for K8s Docs)
* Webcam Logitech C920 HD Pro on top of my screen
* USB keyboard
* mouse
* 1 bottle of water
* door locked for no one to come in and disturb me
* leave your mobile phone outside the room

### Room tip:

If you want to do the exam in a room you are not so familiar with, make sure to prepare the room fitting your needs.
* light
* window
* distance of your chair towards the desk
* distance of the keyboard to the screen
* does the mouse work well on the desk?!
