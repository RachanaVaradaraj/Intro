package com.example.oracleconnect.repository;

import com.example.oracleconnect.entity.Employee;
import org.springframework.data.jpa.repository.JpaRepository;

public interface EmployeeRepository extends JpaRepository<Employee, Long> {
}