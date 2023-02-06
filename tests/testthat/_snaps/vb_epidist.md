# vb_epidist print & format method works as expected

    Code
      dengue_dist <- suppressMessages(vb_epidist(intrinsic_epidist = epidist(disease = "dengue",
        epi_dist = "incubation", prob_distribution = "gamma",
        prob_distribution_params = c(shape = 1, scale = 1), metadata = create_epidist_metadata(
          vector_borne = TRUE)), extrinsic_epidist = epidist(disease = "dengue",
        epi_dist = "incubation", prob_distribution = "gamma",
        prob_distribution_params = c(shape = 2, scale = 2), metadata = create_epidist_metadata(
          vector_borne = TRUE, extrinsic = TRUE))))

---

    Code
      print(dengue_dist)
    Output
      Disease: dengue
      Epi Distribution: incubation
      
       <Intrinsic Distribution> 
      
      Distribution: Gamma(1, 1)
      Parameters:
        shape: 1
        rate: 1
      
       <Extrinsic Distribution> 
      
      Distribution: Gamma(2, 0.5)
      Parameters:
        shape: 2
        rate: 0.5

---

    Code
      format(dengue_dist)
    Output
      Disease: dengue
      Epi Distribution: incubation
      
       <Intrinsic Distribution> 
      
      Distribution: Gamma(1, 1)
      Parameters:
        shape: 1
        rate: 1
      
       <Extrinsic Distribution> 
      
      Distribution: Gamma(2, 0.5)
      Parameters:
        shape: 2
        rate: 0.5
