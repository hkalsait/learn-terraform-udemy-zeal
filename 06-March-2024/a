terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {
   region = "us-east-1"
}

resource "aws_instance" "myec2" {
    ami = "ami-12345"
   # instance_type = var.list[0]
    instance_type = var.types["us-east-1"]
  
}

variable "list" {
    type = list
    default = ["m5.large","m5.xlarge","t2.medium"]
}

variable "types" {
    type = map
    default = {
        us-east-1 = "t2.micro"
        eu-west-2 = "t2.nano"
        ap-south-2 = "t2.small"
    }
}
