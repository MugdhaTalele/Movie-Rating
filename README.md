# Movie-Rating
import imdb
moviesDB=imdb.IMDb()
movies=moviesDB.search_movie("Titanic")
id=movies[0].getID()
movie=moviesDB.get_movie(id)
title=movie["title"]
year=movie["year"]
rating=movie["rating"]
directors=movie["director"]
casting=movie["cast"]
print("movie info")
print(f'{title} -{year}')
print(f'rating:{rating}')
#direcStr=' '.join(map(str,directors))
print(f'directors:{directors}')
actors=' '.join(map(str,casting))
print(f'actors:{actors}')
