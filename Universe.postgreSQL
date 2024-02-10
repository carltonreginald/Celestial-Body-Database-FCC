--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: description; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.description (
    description_id integer NOT NULL,
    name character varying(100) NOT NULL,
    short_description text,
    is_spherical boolean NOT NULL,
    has_life boolean NOT NULL,
    constriant name
);


ALTER TABLE public.description OWNER TO freecodecamp;

--
-- Name: description_description_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.description_description_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.description_description_id_seq OWNER TO freecodecamp;

--
-- Name: description_description_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.description_description_id_seq OWNED BY public.description.description_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(100) NOT NULL,
    age_in_billion_years numeric,
    distance_from_earth_in_lightyears integer,
    constriant name
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(100) NOT NULL,
    occurrences_in_year integer,
    constriant name,
    month character varying(100),
    planet_id integer
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(100) NOT NULL,
    age_in_million_years numeric,
    orbit_period_in_days integer,
    star_id integer,
    constriant name
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(100) NOT NULL,
    age_in_million_years numeric,
    distance_from_earth_in_lightyears integer,
    galaxy character varying(100),
    galaxy_id integer,
    contraint public.galaxy
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: description description_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description ALTER COLUMN description_id SET DEFAULT nextval('public.description_description_id_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: description; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.description VALUES (1, 'Galaxy', 'huge collection of gas, dust, and billions of stars and their solar systems, all held together by gravity', true, true, '1');
INSERT INTO public.description VALUES (2, 'Moon', 'The Moon is Earths only natural satellite', true, false, '2');
INSERT INTO public.description VALUES (3, 'Planet', 'A planet is a celestial body that is in orbit around the Sun', true, true, '3');
INSERT INTO public.description VALUES (4, 'Star', 'Stars are giant balls of hot gas mostly hydrogen, with some helium and small amounts of other elements', true, false, '4');


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Andromeda', 10, 3, '1');
INSERT INTO public.galaxy VALUES (2, 'Black Eye Galaxy', 1, 17, '2');
INSERT INTO public.galaxy VALUES (3, 'Whirlpool', 400, 30, '3');
INSERT INTO public.galaxy VALUES (4, 'Cartwheel', 400, 500, '4');
INSERT INTO public.galaxy VALUES (5, 'Comet', 1, 3, '5');
INSERT INTO public.galaxy VALUES (6, 'Milky Way', 13.6, 27, '6');


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'Moon', 5, '1', 'May', 54);
INSERT INTO public.moon VALUES (2, ' Micromoon', 5, '2', 'Jan', 49);
INSERT INTO public.moon VALUES (3, ' Blood Moon', 1, '3', 'Feb', 50);
INSERT INTO public.moon VALUES (4, ' Blue Moon', 2, '4', 'Mar', 51);
INSERT INTO public.moon VALUES (5, ' Wolf Moon', 1, '5', 'Apr', 52);
INSERT INTO public.moon VALUES (6, ' Snow Moon', 2, '6', 'May', 53);
INSERT INTO public.moon VALUES (7, ' Worm Moon', 1, '7', 'Jun', 54);
INSERT INTO public.moon VALUES (8, ' Pink Moon', 1, '8', 'Jul', 55);
INSERT INTO public.moon VALUES (9, ' Flower Moon', 2, '9', 'Aug', 56);
INSERT INTO public.moon VALUES (10, ' Strawberry Moon', 2, '10', 'Sept', 57);
INSERT INTO public.moon VALUES (11, ' Buck Moon', 1, '11', 'Oct', 58);
INSERT INTO public.moon VALUES (12, ' Sturgeon Moon', 1, '12', 'Nov', 58);
INSERT INTO public.moon VALUES (13, ' Corn Moon', 1, '13', 'Dec', 59);
INSERT INTO public.moon VALUES (14, ' Harvest Moon', 2, '14', 'Dec', 60);
INSERT INTO public.moon VALUES (15, ' Frost Moon', 2, '15', 'Nov', 60);
INSERT INTO public.moon VALUES (16, ' Cold Moon', 2, '16', 'Oct', 59);
INSERT INTO public.moon VALUES (17, ' Waning crescent', 4, '17', 'Sept', 58);
INSERT INTO public.moon VALUES (18, ' Waxing crescent', 4, '18', 'Aug', 57);
INSERT INTO public.moon VALUES (19, ' Crescent', 4, '19', 'Jul', 56);
INSERT INTO public.moon VALUES (20, ' Full Moon', 6, '20', 'Jun', 55);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (49, 'Mercury ', 4.5, 224, 16, '1');
INSERT INTO public.planet VALUES (50, 'Venus ', 4.5, 224, 15, '2');
INSERT INTO public.planet VALUES (51, 'Earth ', 4.5, 365, 14, '3');
INSERT INTO public.planet VALUES (52, 'Mars ', 4.5, 687, 13, '4');
INSERT INTO public.planet VALUES (53, 'Jupiter ', 4.6, 4331, 12, '5');
INSERT INTO public.planet VALUES (54, 'Saturn ', 4.5, 10, 17, '6');
INSERT INTO public.planet VALUES (55, 'Uranus ', 4.5, 30, 17, '7');
INSERT INTO public.planet VALUES (56, 'Neptune ', 4.5, 59, 12, '8');
INSERT INTO public.planet VALUES (57, 'Haumea', 4.5, 103, 13, '39');
INSERT INTO public.planet VALUES (58, ' Pluto', 4.5, 90, 14, '10');
INSERT INTO public.planet VALUES (59, 'Ceres', 4.5, 2, 15, '11');
INSERT INTO public.planet VALUES (60, ' Makemake', 4.5, 111, 16, '12');


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (12, 'Sirius ', 230, 9, 'Milky way', 6, NULL);
INSERT INTO public.star VALUES (13, 'Canopus', 10, 310, 'Milky Way', 6, NULL);
INSERT INTO public.star VALUES (14, 'Arcturus', 7.1, 37, 'Dwarf Satellite', 3, NULL);
INSERT INTO public.star VALUES (15, 'Regulus', 50, 14, 'Black eye', 2, NULL);
INSERT INTO public.star VALUES (16, 'Mimosa', 11, 277, 'Milky Way', 6, NULL);
INSERT INTO public.star VALUES (17, 'Pollux', 727, 34, 'Gemini', 4, NULL);


--
-- Name: description_description_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.description_description_id_seq', 1, false);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 6, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 20, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 60, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 17, true);


--
-- Name: description description_constriant_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description
    ADD CONSTRAINT description_constriant_key UNIQUE (constriant);


--
-- Name: description description_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description
    ADD CONSTRAINT description_pkey PRIMARY KEY (description_id);


--
-- Name: galaxy galaxy_constriant_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_constriant_key UNIQUE (constriant);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_constriant_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_constriant_key UNIQUE (constriant);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_constriant_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_constriant_key UNIQUE (constriant);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: star star_contraint_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_contraint_key UNIQUE (contraint);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: star fk_galaxy; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT fk_galaxy FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- Name: moon fk_planet; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT fk_planet FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet fk_star; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT fk_star FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- PostgreSQL database dump complete
--

