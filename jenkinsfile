pipeline
{
	agent 
	{
		label "built-in"
	}
	stages 
	{
		stage ("stage-1")
		{
			steps
			{
				echo " maar dunga"
			}
		}
		
		stage ("stage-2")
		{
			steps
			{
				dir ("/mnt/data1")
				{
					echo " dekh dunga"
				}
			}
		}
		
		stage ("parallel-stage")
		{
			parallel
			{
				stage ("1")
				{
					steps
					{
						echo "hi"
					}
				}
				
				stage ("2")
				{
					steps
					{
						echo "hi"
					}
				}
				
				stage ("3")
				{
					agent 
					{
						label "slave-a"
					}
					steps
					{
						build "unkil"
					}
				}
			}
		
		}
		
		stage ("stage-3")
		{
			steps
			{
				echo " uda dunga"
			}
		}
	}

}
