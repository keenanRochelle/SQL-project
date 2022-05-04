CREATE TABLE disc_golfers (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    fullname TEXT,
    age INTEGER,
    nationality TEXT);
    
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Ricky Wysocki", 28, "US");
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Paul McBeth", 31, "US");
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Eagle McMahon", 24, "US");
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Calvin Heimburg", 27, "US");
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Chris Dickerson", 29, "US");
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Matt Orum", 35, "US");
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Kyle Klein", 20, "US");
INSERT INTO disc_golfers (fullname, age, nationality) VALUES ("Adam Hammes", 23, "US");

CREATE table pdga_raiting (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    disc_golfer_id INTEGER,
    raiting TEXT,
    sponsor TEXT);
    
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (1, "1053", "Dynamic Discs");
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (2, "1053", "Discraft");
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (3, "1053", "Discmania");
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (4, "1050", "Innova");
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (5, "1046", "Discraft");
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (6, "1042", "Westside");
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (7, "1040", "Discmania");
INSERT INTO pdga_raiting (disc_golfer_id, raiting, sponsor) VALUES (8, "1039", "Discraft");


SELECT * FROM disc_golfers;
SELECT * FROM pdga_raiting;

SELECT disc_golfers.fullname, pdga_raiting.raiting
    FROM disc_golfers
    JOIN pdga_raiting
    ON disc_golfers.id = pdga_raiting.disc_golfer_id;
    
