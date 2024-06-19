# Intro to Clustering

## Clustering for segmentation

![Screenshot 2024-06-19 at 10 00 27 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/c23065ad-6b83-4508-b9c6-c99169cc9d6a)

## What is clustering?

![Screenshot 2024-06-19 at 10 00 46 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/72ad3935-db37-4a5a-a2ae-7c8908a6d98b)

## Clustering vs Classification

![Screenshot 2024-06-19 at 10 01 22 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/9b1733bd-0d44-4ae5-ab12-906663da0242)

## Clustering applications

- **Retail / Marketing**
  - Identifying buying patterns of customers
  - Recommending new books or movies to new customers
- **Banking**
  - Fraud detection in credit card use
  - Identifying clusters of customers (e.g., loyal)
- **Insurance**
  - Fraud detection in claims analysis
  - Insurance risk of customers
- **Publication**
  - Auto-categorizing news based on their content
  - Recommending similar news articles
- **Medicine**
  - Characterizing patient behavior
- **Biology**
  - Clustering genetic markets to identify family ties
 
## Why Clustering?
- Exploratory data analysis
- Summary generation
- Outlier detection
- Finding duplicates
- Pre-precessing step

## Clustering algorithms

![Screenshot 2024-06-19 at 11 51 08 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/c0e475de-6b23-481d-b724-25effdba4ac2)

# Intro to k-Means

## What is k-Means clustering?

![Screenshot 2024-06-19 at 11 52 29 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/a0f15340-de90-4338-9662-3472b3ba5031)

## k-Means algorithms

![Screenshot 2024-06-19 at 11 53 06 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/f7ace984-18e4-42a0-bf14-8ff8b58f1e6b)

## Determine the similarity or dissimilarity

![Screenshot 2024-06-19 at 11 53 39 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/1715bfd6-ebd6-42e5-acc7-8fcd2905ad42)

## 1-dimensional similarity / distance

![Screenshot 2024-06-19 at 11 54 20 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/1b11362f-85f5-4f6a-b178-de73ec03ac3f)

## 2-dimensional similarity / distance

![Screenshot 2024-06-19 at 11 55 12 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/1ef622cc-5be0-43a7-a419-8bc96fc6826e)

## Multi-dimentional similarity / distance

![Screenshot 2024-06-19 at 11 55 48 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/0fdc7557-8340-46bd-bef3-b99ad58ef790)

## How does k-Means clustering work?

### 1. Initialize k

![Screenshot 2024-06-19 at 11 57 03 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/8f3552d7-2ef9-443a-8117-0d154a284c3c)

### 2. Calculate the distance

![Screenshot 2024-06-19 at 11 57 53 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/8d8de144-6776-41f5-90ee-6ca680e57873)

### 3. Assign to centroid

![Screenshot 2024-06-19 at 11 58 36 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/a9b13651-b58d-489f-9b31-51a704575efb)

### 4. Compute new centroids

![Screenshot 2024-06-19 at 11 59 16 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/20407cec-3884-4654-98fb-f8cb8b249df9)

### 5. Repeat

![Screenshot 2024-06-19 at 11 59 37 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/898dc189-f190-4faf-bb03-0cea075c5942)

# More on k-Means

## k-Means clustering algorithm
1. Randomly placing k centroids , one for each cluster
2. Calculate the distance of each point from each centroid
3. Assign each data point (object) to its closest centroid, creating a cluster
4. Recalculate the position of the k centroids
5. Repeat the steps 2-4, until the centroids no longer move.

## k-Means accuracy

![Screenshot 2024-06-19 at 12 02 23 PM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/b5f2df34-d5cb-4479-b6cf-38dcd0bb21df)

## Choosing k

![Screenshot 2024-06-19 at 12 02 50 PM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/30d03603-245d-4779-9a56-fdea4d173b98)

## k-Means recap
- Med and Large sized databases (Relatively efficient)
- Produces sphere-like clusters
- Needs number of clusters (k)
