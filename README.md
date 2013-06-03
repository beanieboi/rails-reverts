# Rails Reverts

show the number of git reverts over time on rails/rails

getting the data:

	git log --no-merges --format="%ci" --grep="^Revert" | awk '{print substr($0, 0, 7)}' | sort -n | uniq -c | sort
