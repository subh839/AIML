obs(tree).

	obs(human).	obs(car).

	obs(roadblock).

	obs(redlight).

	obs(blackbuck).

	pc(noentry).

	trafficlight(red).

	light1(red).

	trafficlight2(green).

	light2(green).

	trafficlight3(yellow).

	light3(yellow).

	

	brakes(X) :- obs(X).

	turnleft(X) :- pc(X).

	acc(X) :- !,obs(X).

	stop(X) :- trafficlight(X), light1(X).

	move(X) :- trafficlight2(X), light2(X).

	moveslow :- trafficlight3(X), light3(X).
