Symmetric Pairs
SELECT F.X, F.Y FROM FUNCTIONS AS F


GROUP BY F.X, F.Y 
HAVING COUNT(*) >= 1
