#ifndef STUDENTWORLD_H_
#define STUDENTWORLD_H_

#include "GameWorld.h"
#include "GraphObject.h"
#include "GameConstants.h"
#include "Actor.h"
#include <string>
#include <iostream>

// Students:  Add code to this file, StudentWorld.cpp, Actor.h, and Actor.cpp

class StudentWorld : public GameWorld
{
public:
	StudentWorld(std::string assetDir);
	~StudentWorld();

	virtual int init();
	

	virtual int move();
	//{
		  // This code is here merely to allow the game to build, run, and terminate after you hit enter a few times.
		  // Notice that the return value GWSTATUS_PLAYER_DIED will cause our framework to end the current level.
		//decLives();
		//return GWSTATUS_PLAYER_DIED;
	//}

	virtual void cleanUp();
	//{
	//}

private:
	Dirt* m_dirt[60][60];
	Frackman* m_player;
};

#endif // STUDENTWORLD_H_
