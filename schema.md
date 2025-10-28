# Data Model
Deck(id, name, region, tags[], created_at, updated_at)
Card(id, deck_id, type[flashcard_cloze|label|naming], prompt_text, answer_text, media_ref, tags[], extraJSON, created_at)
CardState(user_id, card_id, fam0..1, last_seen_at, state[new|learning|familiar|known], last_result)
SessionCard(session_id, card_id, times_shown)
DeckProgress(user_id, deck_id, learned_count, known_count, last_finished_at)
UserEconomy(user_id, xp, coins, streak_days, last_study_at)
Item(id, name, category[outfit|accessory|background|frame], rarity, price_coins, unlock_xp_min)
Inventory(user_id, item_id, owned, equipped)
