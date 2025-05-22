# S32025
Attempted work on S3 (personal)
#okay, trying to make a guide for how to actually use the updated search terms and gemma.r in 2025, see how this goes.
#default search term should look like this below:
get_datasets(
  query = NA_character_,
  filter = NA_character_,
  taxa = NA_character_,
  uris = NA_character_,
  offset = 0L,
  limit = 20L,
  sort = "+id",
  raw = getOption("gemma.raw", FALSE),
  memoised = getOption("gemma.memoised", FALSE),
  file = getOption("gemma.file", NA_character_),
  overwrite = getOption("gemma.overwrite", FALSE)
)
#We can go ahead and remove "filter" for now, you can filter after results are pulled
#Set query to your search terms
#make sure to name each object
#dplyr package allows %>% use (pipeline command to add addtitional code to line)
SearchTerms <- "Chronic stress anterior cingulate cortex OR Chronic stress prefrontal cortex"
SearchResults_df <- get_datasets(query = SearchTerms, taxa = c('mouse', 'rat')) %>%
select(experiment.shortName, experiment.longName
taxa = "mouse"
offset = 0L
limit = 100L
sort = "+id"
raw = getOption("gemma.raw", FALSE)
memoised = getOption("gemma.memoised", FALSE)
overwrite = getOption("gemma.overwrite", FALSE)

#if you run 
gemma.R::get_datasets()
#and then hit help on the right side it explains each feature of the code.
#maybe URI would help? ex:
get_datasets(taxa = c("mouse", "human"), uris = "http://purl.obolibrary.org/obo/UBERON_0002048")
