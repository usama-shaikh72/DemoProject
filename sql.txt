-- phpMyAdmin SQL Dump
-- version 5.1.1
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Sep 03, 2025 at 09:50 PM
-- Server version: 10.4.20-MariaDB
-- PHP Version: 7.3.29

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `furniture_store`
--

-- --------------------------------------------------------

--
-- Table structure for table `admins`
--

CREATE TABLE `admins` (
  `id` int(11) NOT NULL,
  `email` varchar(255) NOT NULL,
  `password` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `admins`
--

INSERT INTO `admins` (`id`, `email`, `password`) VALUES
(1, 'admin@example.com', '$2y$10$/.vAaW6gzlMermff5eYHtOM7WcvrRfiUZhWP1DyteICTbET9ixTJC');

-- --------------------------------------------------------

--
-- Table structure for table `contacts`
--

CREATE TABLE `contacts` (
  `id` int(11) NOT NULL,
  `name` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `message` text NOT NULL,
  `submitted_at` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `contacts`
--

INSERT INTO `contacts` (`id`, `name`, `email`, `message`, `submitted_at`) VALUES
(1, 'usama shaikh', 'shaikhusama7548@gmail.com', 'hello', '2025-03-28 13:58:28'),
(5, 'usamaa', 'shaikhusama7548@gmail.com', 'hello', '2025-04-18 07:54:35'),
(6, 'usamaa', 'shaikhusama7548@gmail.com', 'hello', '2025-04-18 07:54:36'),
(7, 'usamaa shk', 'shaikhusama7548i@gmail.com', 'hellow', '2025-04-18 19:15:21'),
(9, 'abdul', 'shaikhusama7548@gmail.com', 'hellow', '2025-04-21 06:49:28'),
(10, 'abdul th', 'abdul68@gmail.com', 'hi', '2025-04-22 04:56:51'),
(11, 'abdul', 'shaikhusama7548@gmail.com', 'hellow', '2025-04-22 05:30:49'),
(12, 'rehan', 'shaikhusama7548@gmail.com', 'hellooooo', '2025-04-23 04:30:04'),
(13, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'hello', '2025-05-08 07:08:31');

-- --------------------------------------------------------

--
-- Table structure for table `orders`
--

CREATE TABLE `orders` (
  `id` int(11) NOT NULL,
  `name` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `address` text NOT NULL,
  `payment_method` varchar(50) NOT NULL,
  `upi_id` varchar(255) DEFAULT NULL,
  `phone` varchar(20) DEFAULT NULL,
  `order_date` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `orders`
--

INSERT INTO `orders` (`id`, `name`, `email`, `address`, `payment_method`, `upi_id`, `phone`, `order_date`) VALUES
(1, 'usama shaikh', 'shaikhusama7548@gmail.com', 'sdgdsgsfgkg', 'online', 'shaikhusama@h9t2', '9224334447', '2025-04-20 02:58:54'),
(2, 'usama shaikh', 'shaikhusama7548@gmail.com', 'area jytdycygcdu uyfdc', 'cod', '', '', '2025-04-20 02:59:25'),
(3, 'usama shaikh', 'shaikhusama7548@gmail.com', 'area jytdycygcdu uyfdc', 'cod', '', '', '2025-04-20 03:00:38'),
(4, 'usama shaikh', 'shaikhusama7548i@gmail.com', 'fg dfgfd dgrgf', 'online', 'shaikhusama@h9t2', '9224334447', '2025-04-20 03:01:33'),
(5, 'usama shaikh', 'shaikhusama7548i@gmail.com', 'sfhgfs fgskgftswkfbsk', 'cod', 'shaikhusama@h9t2', '9224334447', '2025-04-20 03:02:31'),
(6, 'usama shaikh', 'shaikhusama7548i@gmail.com', 'gdd dhgdhgdyhyd ', 'online', 'shaikhusama@h9t2', '9224334447', '2025-04-20 03:02:53'),
(7, 'abdul', 'shaikhusama7548@gmail.com', 'ulhasnagar', 'cod', '', '', '2025-04-21 03:20:50'),
(8, 'abdul', 'shaikhusama7548@gmail.com', 'ulhasnagar', 'online', 'shaikhusama@h9t2', '9224334447', '2025-04-21 03:21:17'),
(9, 'abdul', 'raj123@gmail.com', 'jhjbvviufi fkuoig', 'online', 'shaikhusama@h9t2', '9224334447', '2025-04-22 01:28:27'),
(10, 'usama shaikh', 'shaikhusama7548@gmail.com', 'ulhasnagar', 'online', 'shaikhusama@h9t2', '9224334447', '2025-04-22 01:57:41'),
(11, 'usama shaikh', 'shaikhusama7548@gmail.com', 'mumbra ', 'cod', '', '', '2025-04-23 00:56:40'),
(12, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'cod', '', '', '2025-05-08 03:36:59'),
(13, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'online', 'shaikhusama@h9t2', '9224334447', '2025-05-08 03:40:53'),
(14, 'usama jameel ahmed shaikh', 'shaikhusama7548@g.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'cod', '', '', '2025-05-08 05:07:12'),
(15, 'usama jameel ahmed shaikh', 'shaikhusama7548@g.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'cod', '', '', '2025-05-08 05:07:26'),
(16, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'online', 'shaikhusama@h9t2', '9224334447', '2025-05-08 05:08:23'),
(17, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'online', 'shaikhusama@h9t2', '9224334447', '2025-07-06 03:56:29'),
(18, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'cod', '', '', '2025-08-12 11:47:35'),
(19, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'online', 'shaikhusama@h9t2', '9224334447', '2025-08-17 02:00:26'),
(20, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'online', 'shaikhusama@h9t2', '9224334447', '2025-08-17 02:00:30'),
(21, 'usama jameel ahmed shaikh', 'shaikhusama7548i@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'cod', '', '', '2025-08-17 14:07:30'),
(22, 'usama jameel ahmed shaikh', 'shaikhusama7548@gmail.com', 'mumbra\r\n210, noorani blg, mumbra devi road mumbra thane', 'cod', '', '', '2025-08-30 09:18:33');

-- --------------------------------------------------------

--
-- Table structure for table `products`
--

CREATE TABLE `products` (
  `id` int(11) NOT NULL,
  `name` varchar(100) DEFAULT NULL,
  `description` text DEFAULT NULL,
  `price` decimal(10,2) DEFAULT NULL,
  `category` varchar(50) DEFAULT NULL,
  `image` varchar(255) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `products`
--

INSERT INTO `products` (`id`, `name`, `description`, `price`, `category`, `image`) VALUES
(10, 'foldable chair', 'A comfortable foldable chair \r\n', '2000.00', 'chair', 'uploads/modern.webp');

-- --------------------------------------------------------

--
-- Table structure for table `users`
--

CREATE TABLE `users` (
  `id` int(11) NOT NULL,
  `firstname` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `password` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `users`
--

INSERT INTO `users` (`id`, `firstname`, `email`, `password`) VALUES
(19, 'usama shaikhhh', 'usamashaikh6246@gmail.com', '$2y$10$RACfsKkZkl2c4YjMI67u6e4t5KgPzlWXDdszKeTe00FkS4ZaCSpTy'),
(21, 'usama shaikh', 'shaikhusama7548@gmail.com', '$2y$10$LRlkgeEdXTu6XzhZ15sQjuH5v9jcuSM7EDLxkZMTyHluMN1PFC5Da'),
(22, 'rehan', 'rehanshaikh7223@gmail.com', '$2y$10$jweWomZ1On/dI5Xo2SLFH.g8BSxjJxSapxjNMlPpSG3M40xHn3sNS'),
(23, 'austin', 'Austin7548@gmail.com', '$2y$10$zlrSz9FGaGxjHz7Fn0ZjCONIVhjYiQVzhPF6.xi/gTkB2BQkPPkBa'),
(24, 'usamaaa', 'shaikhusama7548ki@gmail.com', '$2y$10$1kRfPIGc2HGDR.71Eb7WkOW/AIKUn2h4Um1ifJTfL3kSslIN3tNIi'),
(25, 'abdul shaikh', 'abdul782@gmail.com', '$2y$10$1g0TpwvXZ94GboYUGxvBhu2LMDdlP5ax2O9CHQVny7OWX2Q7k5/xG'),
(26, 'usama shaikh', 'shaikhusama75484@gmail.com', '$2y$10$vmOdaZrMWiUlW4KbqMTUKOQUcbMzX2XwDb0msfh..qnHRj0dk/MFW'),
(27, 'usama shk', 'usama12@gmail.com', '$2y$10$IM6SbmVPo3R5mXqBK1Ejd.Cm8NmSVN/goaeq4IiejecgBaFP5ksJG');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `admins`
--
ALTER TABLE `admins`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `email` (`email`);

--
-- Indexes for table `contacts`
--
ALTER TABLE `contacts`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `orders`
--
ALTER TABLE `orders`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `products`
--
ALTER TABLE `products`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `users`
--
ALTER TABLE `users`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `email` (`email`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `admins`
--
ALTER TABLE `admins`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `contacts`
--
ALTER TABLE `contacts`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=14;

--
-- AUTO_INCREMENT for table `orders`
--
ALTER TABLE `orders`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=23;

--
-- AUTO_INCREMENT for table `products`
--
ALTER TABLE `products`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=11;

--
-- AUTO_INCREMENT for table `users`
--
ALTER TABLE `users`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=28;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
