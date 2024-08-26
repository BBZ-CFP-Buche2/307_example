# Github

Token: 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


# Database Verwaltung:
https://db-sql.ch/  
enrico.buchs@bbz-cfp.ch  
Abcd1234  

nexdu.ch  
ebuchs_bbz  
K5p68o6b@  


## Tables
CREATE TABLE users (
id SERIAL PRIMARY KEY,
email TEXT NOT NULL,
passwort TEXT NOT NULL
);


CREATE TABLE posts (
id SERIAL PRIMARY KEY,
user_id BIGINT(20) UNSIGNED,
titel VARCHAR(64) NOT NULL,
inhalt VARCHAR(512) NOT NULL,
datum DATE,
likes INT DEFAULT 0,
CONSTRAINT fk_user FOREIGN KEY (user_id) REFERENCES users(id)
);