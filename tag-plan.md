## Tagging workflow 

# Editing tag assignments only

* Edit the YAML block in tag-plan.md (e.g. change [npr] → [drawing, npr] on a post's line).
* Run:
- cd "/Users/hertzman/Desktop/hertzmann.github.io copy" && python3 apply_tags.py
- Reload the page (jekyll serve picks up the post changes automatically; no restart needed).

# Editing tag definitions, colors, names, etc: \_config.yml, and restart Jekyll


## Tags (just notes; actual metadata is stored in _config.yml_)

| Slug | Display name | ~Posts | Scope |
|---|---|---|---|
| `npr` | Non-Photorealistic Rendering | 10 | Line-rendering algorithms; posts about perception *of* drawing that build on them carry `drawing` too |
| `perception` | Perception & Pictures | 16 | Visual perception, perspective, illusions, picture perception |
| `making-art` | My Art Practice | 14 | Personal painting/drawing practice, learning, creative process |
| `art-theory` | Art Theory & History | 14 | Definitions of art, art history, contemporary art, aesthetics |
| `photography` | Photography | 8 | Photography as art/technology, tone, objectivity, camera perspective |
| `art-tech` | Art & Technology | 16 | Tech-meets-art: generative AI, DeepDream, DALL-E, cryptoart, recorded music, tech & society |
| `minds` | Minds & Machines | 8 | Consciousness, computationalism, brains vs. computers, cognition |
| `academia` | Academia | 17 | Conferences, peer review, publishing, research practice, sci-comm |
| `books` | Book Reviews | 4 | Book review posts |

## Post → tag assignments

```yaml
# filename: [tags]
2020-04-19-lines-as-edges.md:                        [perception, npr]
2020-04-21-ar-vs-cs.md:                              [perception, npr]
2020-05-04-art-book-reviews.md:                      [books, art-theory]
2020-05-08-siggraph-as-conference.md:                [academia]
2020-05-19-wiwia.md:                                 [art-theory]
2020-06-08-wica.md:                                  [art-theory]
2020-07-13-rebuttals.md:                             [academia]
2020-07-14-bits.md:                                  [academia]
2020-08-31-cvpr-graphics.md:                         [academia]
2020-09-12-how-to-draw-pictures-contours.md:         [npr]
2020-09-13-how-to-draw-pictures-suggestive-contours.md: [npr]
2020-09-14-how-to-draw-pictures-style.md:            [npr]
2020-09-15-painting-in-karies.md:                    [making-art]
2020-09-23-dreaming-and-Sampling.md:                 [minds]
2020-10-05-art-is-a-process.md:                      [making-art]
2020-10-12-the-goal-of-painting.md:                  [making-art]
2020-10-21-quantitative-evaluation.md:               [academia]
2020-10-23-planning-and-strategy.md:                 [making-art]
2020-10-26-time-and-speed.md:                        [making-art]
2020-10-28-embracing-digital-painting.md:            [making-art]
2020-11-02-abstract-painting.md:                     [making-art]
2020-12-29-deepdream.md:                             [art-tech]
2021-01-11-robot-art.md:                             [art-tech]
2021-01-25-book-intro.md:                            [art-theory, perception]
2021-03-03-ac-suggestions.md:                        [academia]
2021-03-11-cryptoart.md:                             [art-tech]
2021-03-11-lifecycle.md:                             [art-tech]
2021-03-22-art-is-social.md:                         [art-theory]
2021-04-19-questons-for-computational-creativity.md: [art-tech]
2021-05-13-why-does-line-drawing-work.md:            [perception, npr]
2021-05-19-how-to-draw-line-thickness.md:            [npr]
2021-08-17-learning-skills.md:                       [making-art]
2022-2-28-how-does-perspective-work.md:              [perception, photography]
2022-3-10-photographic-tone.md:                      [photography, perception]
2022-3-17-photography-is-not-objective.md:           [photography, art-theory]
2022-5-25-dall-e.md:                                 [art-tech]
2022-6-1-art-books-2022.md:                          [books, art-theory]
2022-07-21-siggraph-expectation-creep.md:            [academia]
2022-08-29-photography-history.md:                   [photography, art-tech]
2022-09-04-computationalism.md:                      [minds]
2022-09-19-art-definitions-1.md:                     [art-theory]
2022-09-19-art-definitions-2.md:                     [art-theory]
2022-09-27-art-eras.md:                              [art-theory]
2022-10-11-amateurs.md:                              [art-tech, art-theory]
2022-10-26-experimentation.md:                       [art-theory]
2022-12-16-status-quo-bias.md:                       [art-tech]
2022-12-17-when-tech-changes-art.md:                 [art-tech]
2023-03-01-ai-art-analogies.md:                      [art-tech]
2023-03-06-open-ended-exploration.md:                [making-art, academia]
2023-03-23-hockney-falco.md:                         [art-theory, photography]
2023-03-30-can-you-tell-photography.md:              [photography, perception]
2023-04-27-user-studies.md:                          [academia]
2023-06-30-meta-papers.md:                           [academia]
2023-07-31-occluding-contours-part-1.md:             [npr]
2023-07-31-occluding-contours-part-2.md:             [npr]
2023-07-31-occluding-contours-part-3.md:             [npr]
2023-08-07-SIGGRAPH-reminiscences.md:                [academia]
2023-09-05-blogging.md:                              [academia]
2023-09-08-why-research-labs-should-publish.md:      [academia]
2023-09-27-what-is-creativity.md:                    [art-tech, minds]
2023-10-26-three-kinds-of-art-technologies.md:       [art-tech]
2023-12-11-art-worlds.md:                            [art-theory]
2024-03-15-computer-graphics-research.md:            [academia, perception]
2024-05-09-illusion-of-awareness.md:                 [perception]
2024-05-24-fixations-vision-illusions.md:            [perception]
2024-06-10-perspective-distortions.md:               [perception, photography]
2024-06-19-why-evolution-isnt-optimization.md:       [minds]
2024-06-21-judgments.md:                             [making-art]
2024-08-19-journey.md:                               [making-art, academia, perception, art-tech, npr]
2024-09-09-dvc-multiperspective.md:                  [perception, photography]
2024-09-18-books-on-consciousness.md:                [books, minds]
2024-10-07-picture-perception.md:                    [perception]
2024-10-14-six-years-later.md:                       [making-art]
2024-10-16-perspective-as-arrangement.md:            [making-art, perception]
2024-10-18-adrift.md:                                [making-art]
2025-06-23-nvc-1-scicomm.md:                         [academia]
2025-06-23-nvc-2-reviewing.md:                       [academia]
2025-09-15-books-that-changed-me.md:                 [books]
2025-09-30-menace-of-mechanical-music.md:            [art-tech]
2025-10-25-indistinguishability.md:                  [art-tech]
2025-10-26-isolation.md:                             [art-tech]
2026-03-23-drawing-skills.md:                        [perception]
2026-05-15-dog-knowledge.md:                         [minds]
2026-05-20-consciousness.md:                         [minds]
2026-06-01-scribbling.md:                            [perception, art-theory, making-art]
2026-07-13-brain-not-a-computer.md:                  [minds]
```