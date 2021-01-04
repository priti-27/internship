CREATE TABLE `cards1` (
  `card_id` bigint(20) NOT NULL,
  `card_template_id` bigint(20) NOT NULL,
  `card_user_id` bigint(20) NOT NULL,
  `card_name` varchar(100) NOT NULL,
  `card_job_title` varchar(100) NOT NULL,
  `card_mobile` bigint(15) NOT NULL,
  `card_website` varchar(200) NOT NULL,
  `card_fax` varchar(50) NOT NULL,
  `card_about_us` text NOT NULL,
  `Card_address_1` varchar(250) NOT NULL,
  `Card_address_2` varchar(250) NOT NULL,
  `Card_cover_photo_url` tinytext NOT NULL,
  `Card_profile_image_ur` tinytext NOT NULL,
  `card_has_whatsapp` int(1) NOT NULL DEFAULT 0,
  `card_has_contact_form` int(1) NOT NULL DEFAULT 0,
  `card_facebook_link` tinytext NOT NULL,
  `card_youtube_link` tinytext NOT NULL,
  `card_instagram_link` tinytext NOT NULL,
  `card_linkdin_link` tinytext NOT NULL,
  `card_created_at` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `card_deleted_at` timestamp NOT NULL DEFAULT current_timestamp(),
  `card_Updated_at` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;


CREATE TABLE `galleries` (
  `gallery_id` int(11) NOT NULL,
  `user_Id` bigint(20) NOT NULL,
  `gallery_Image_name` varchar(255) NOT NULL,
  `gallery_image_url` varchar(255) NOT NULL,
  `gallery_type` varchar(1) NOT NULL,
  `gallery_created_at` int(11) NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE `packages` (
  `package_id` int(11) NOT NULL,
  `package_name` varchar(50) NOT NULL,
  `package_has_free` int(11) NOT NULL DEFAULT 0,
  `package_amount` float(8,2) NOT NULL,
  `package_has_social_link` int(1) NOT NULL DEFAULT 0,
  `package_has_whatsapp` int(2) NOT NULL DEFAULT 0,
  `package_has_profile_image` int(1) NOT NULL DEFAULT 0,
  `package_created_at` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `package_deleted_at` timestamp NOT NULL DEFAULT current_timestamp(),
  `package_update_at` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=latin1;


CREATE TABLE `users` (
  `user_Id` bigint(20) NOT NULL,
  `user_f_name` varchar(100) NOT NULL,
  `user_l_name` varchar(100) NOT NULL,
  `user_mobile` bigint(15) NOT NULL,
  `user_mobile_verified_at` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `user_email` varchar(100) DEFAULT NULL,
  `user_email_verified_at` timestamp NOT NULL DEFAULT current_timestamp(),
  `user_password` varchar(255) NOT NULL,
  `user_term_condition_status` char(1) NOT NULL DEFAULT '1',
  `user_device_token` varchar(255) DEFAULT NULL,
  `user_roll_type` int(2) NOT NULL,
  `user_status` char(1) NOT NULL DEFAULT 'P',
  `User_created_at` timestamp NOT NULL DEFAULT current_timestamp(),
  `User_updated_at` timestamp NOT NULL DEFAULT current_timestamp(),
  `User_deleted_at` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
COMMIT;

CREATE TABLE `template` (
  `template_Id` bigint(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
