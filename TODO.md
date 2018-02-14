# TODO

- [x] create github repo
- [x] create basic framework (description readme, todo)
- [] create basic call (POST)
- [] create tests 
- 

- [] possibly move git2r to suggest and use alternative, f.i. from the DESCRIPTION / BugReports: https://github.com/RMHogervorst/ghissues/issues

query {
    repository(owner:"rmhogervorst", name:"ghissues") {
        issues(last:20, states:OPEN) {
            edges {
                node {
                    title
                    url
                    labels(first:5) {
                        edges {
                            node {
                                name
                            }
                        }
                    }
                }
            }
        }
    }
}


curl -H "Authorization: bearer token" -X POST -d " \
 { \
   \"query\": \"query { viewer { login }}\" \
 } \
" https://api.github.com/graphql

# what nees to be collected from the github api?
- can be hardcoded

total number of issues opened, total closed.
- first 20 issues? (paging option for others? ) (button that collects the others?)
- options to import all of the issues?
- filtering on issues, so collect the possible labels and give option to label on that?
- 

# what needs to be supplied?
owner, ghrepo

