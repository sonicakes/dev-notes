# TDD with RSPEC
RSPEC us actually BDD, not TDD! It is Behaviour Driven Development , which combines TDD, Domain-Driven design and acceptance TDD planning.

Command in terminal for running test for models (add name of respective model you want to test)

`rspec spec/models/tour_spec.rb --format d`

To group the tests, we put them in ‘describe' blocks:
`describe "Validations" do`

*Linguistic remark:*

Ruby converts multiple of non-typical nouns, such as People from Person! With my associations,  I can specify that my Tour model `has_many people` and it knows that I’m talking about Person model!
