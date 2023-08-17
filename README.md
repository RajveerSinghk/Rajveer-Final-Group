# Rajveer-Final-Group
class Facility:
    def _init_(self):
        self.FacilityName = ""

    def addFacility(self):
        self.FacilityName = input("Enter Facility Name: ")
        self.writeFacilityToFile(self.FacilityName)

    def writeFacilityToFile(self, facility_name):
        with open("facilities.txt", "a") as file:
            file.write(facility_name + "\n")

    def displayFacilities(self):
        with open("facilities.txt", "r") as file:
            lines = file.readlines()
            for line in lines:
                print(line.strip())

    def writeListOffacilitiesToFile(self, facilities_list):
        with open("facilities.txt", "w") as file:
            for facility in facilities_list:
                file.write(facility + "\n")
                
