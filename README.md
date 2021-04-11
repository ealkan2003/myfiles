This is JSON file to get scores of Turkish Super League 2020-21 season.

You have to use below construction to fetch data:

class Datum
        public int id
        public string leagueName
        public string country
        public List<Season> seasons

class Season
        public string id { get; set; }
        public string seasonName { get; set; }
        public List<Ranking> currentGeneralRanking { get; set; }
        public List<Ranking> currentHomeRanking { get; set; }
        public List<Ranking> currentAwayRanking { get; set; }
        public List<Team> teams { get; set; }
        public List<Round> rounds { get; set; }

class Ranking
        public int rank { get; set; }
        public string teamName { get; set; }
        public int played { get; set; }
        public int win { get; set; }
        public int draw { get; set; }
        public int loose { get; set; }
        public int goalFor { get; set; }
        public int goalAgainst { get; set; }
        public int average { get; set; }
        public int point { get; set; }

class Team
        public int teamId { get; set; }
        public string teamName { get; set; }
        public string city { get; set; }

class Round
        public int roundId { get; set; }
        public List<Match> matches { get; set; }

class Match
        public int matchId { get; set; }
        public int roundId { get; set; }
        public string matchDate { get; set; }
        public string homeTeam { get; set; }
        public string homeScore { get; set; }
        public string awayTeam { get; set; }
        public string awayScore { get; set; }
        public List<Goal> goals { get; set; }

class Goal
        public int goalId { get; set; }
        public int matchId { get; set; }
        public string player { get; set; }
        public string goalTime { get; set; }
        public string madeUsing { get; set; }
        public bool penalty { get; set; }
        public bool ownGoal { get; set; }
        public string homeOrAway { get; set; }
