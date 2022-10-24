<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://www.researchgate.net/figure/The-Arbiter-PUF-structure_fig1_228851018">
    <img src="images/The-Arbiter-PUF-structure.png" alt="Logo" width="150" height="150">
  </a>

  <h3 align="center">Machine Learning Attack on Arbiter PUF</h3>
  <p align="center">
    by: Justin Schubeck, Alex Liu, Yash Bhat
  </p>
</p>

## University of Florida : [Electrical and Computer Engineering](https://www.ece.ufl.edu/)<br />EEE5716 - Introduction to Hardware Security and Trust Fall 2022
Faculty: <br />
[Dr. Fahahmandi](https://www.ece.ufl.edu/people/faculty/farimah-farahmandi/) <br />
[Dr. Tehranipoor](https://www.ece.ufl.edu/people/faculty/mark-m-tehranipoor/) <br />
Students: <br />
[Justin Schubeck](https://www.linkedin.com/in/justinschubeck/) <br />
[Alex Liu](https://www.linkedin.com/in/alex-liu-m1/) <br />
[Yash Bhat](https://www.linkedin.com/in/yash-bhat/)



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#dependencies">Dependencies</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#running">Running</a></li>
      </ul>
    </li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
**Main Objective **
In this project, you will learn that PUFs are not perfect! In particular, you will perform a machine learning (ML) based attack on arbiter PUFs.

**Background** 
Research shows that arbiter PUFs can be modeled with certain machine learning techniques [1], [2]. If adversaries can accurately model a PUF, they can predict its challenge response pairs and impersonate the PUF, thereby breaking the security of protocols that rely on the response being unpredictable.

In the simplest form, a machine learning-based modeling attack proceeds as follows:
1. The attacker learns some number of challenge-response pairs for the PUF. This could happen if, for example, a manufacturer remotely authenticates its chips on an unencrypted channel.
2. The attacker must have knowledge of the PUF architecture.
3. A mathematical model is constructed of the PUF, and parameters of the model are derived (or, equivalently, “the model
is trained”) using known challenge-response pairs.
4. New challenges can now be supplied to the trained model (which now acts as the software clone of the original PUF)
to predict the real PUF’s responses.
More efficient modeling attacks are those that accurately model a PUF’s responses given a small number of challenge-response
pairs.

**Project Goal**
1. For the given CRP dataset (CRPSets.zip), implement (G: two, UG: one) machine learning technique(s) for predicting
PUF responses given previously-unseen inputs (SVM: [1,3], regression: [2]). In other words, train your model using
the different training/testing splits as described in “Results to submit”.
2. Evaluate your model. Use CRPs that were not in your training set to determine how well your model predicts the PUF
output for inputs that it has not previously seen.


<!-- GETTING STARTED -->
## Getting Started

### Dependencies
* NumPy 1.22.4

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/justinschubeck/ML-Attack-on-Arbiter-PUF.git
   ```
2. Setup (and activate) your environment

### Running
**No additional actions should have to be taken by the user in order for the program to run successfully.**

**File Descriptions**
* ```Test.ipynb```: This file loads in the testing dataset and the model files and performs evaluation on the test set. 

<!-- Authors -->
## Authors

* Justin Schubeck - jschubeck@ufl.edu
* Alex Liu - aliu1@ufl.edu
* Yash Bhat - bhat.yashasvi@ufl.edu

Project Link: [https://github.com/justinschubeck/ML-Attack-on-Arbiter-PUF](https://github.com/justinschubeck/ML-Attack-on-Arbiter-PUF)


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [Catia Silva (readme template)](https://faculty.eng.ufl.edu/catia-silva/)
* [Nurun N. Mondol (teaching assistant)](https://fics.institute.ufl.edu/index.php/about/students/)

1. Rhrmair, Ulrich, et al. “PUF modeling attacks on simulated and silicon data.” IEEE Transactions on Information Forensics and Security 8.11 (2013): 1876-1891.
2. Rhrmair, Ulrich, et al. “Modeling attacks on physical unclonable functions.” Proceedings of the 17th ACM conference on Computer and communications security. ACM, 2010.
3. Lim, Daihyun. Extracting secret keys from integrated circuits. Diss. Massachusetts Institute of Technology, 2004

## Thank you