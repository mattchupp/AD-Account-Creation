# Get User Information
$FirstName = Read-Host -Prompt "First Name"
$LastName = Read-Host -Prompt "Last Name"
$JobTitle = Read-Host -Prompt "Job Title"
$Department = Read-Host -Prompt "Department"
$Location = Read-Host -Prompt "Location"

# create username from Firstname and Lastname and put to lowercase
$UserName = $FirstName[0]+$LastName
$Username = $UserName.ToLower()
$Email = "$UserName@femoransecurity.com"

$HomePage = "www.FEMoranSecurity.com"

# Generate Default Password
#$Initials = $FirstName[0]+$LastName[0]
#$Password = ConvertTo-SecureString "$Initials"+"femoran19!"


# Conditions for Locations to set Address and assign OU
if ($Location -eq 'Kansas') {
    $StreetAddress = "2611 East 17th Ave"
    $City = "Hutchinson"
    $State ="KS"
    $PostalCode = "67501"
    $OfficeNumber = "620-665-6651"
    $FaxNumber = "620-665-6790"
} elseif ($Location -eq 'Carmel') {
    Write-Host "Carmel Office"
    $StreetAddress = "887 W Carmel Dr"
    $City = "Carmel"
    $State = "IN"
    $PostalCode = "46032"
    $OfficeNumber = "317-865-1014"
    $FaxNumber = "317-532-5772"
} elseif ($Location -eq 'Michigan') {
    Write-Host "Michigan Office"
    $StreetAddress = "30801 Barrington Street, Suite 120"
    $City = "Madison Heights"
    $State = "MI"
    $PostalCode = "48071"
    $OfficeNumber = "586-296-4300"
    $FaxNumber = "586-403-6442"
} else {
    Write-Host "Champaign Office"
    $StreetAddress = "201 W University Ave"
    $City = "Champaign"
    $State = "IL"
    $PostalCode = "61820"
    $OfficeNumber = "217-403-6444"
    $FaxNumber = "217-403-6442"
}


New-ADUser -Name "$FirstName $LastName" -DisplayName "$FirstName $LastName" -GivenName "$Firstname" -Surname "$LastName" -UserPrincipalName "$Username@femam.local" -SamAccountName "$UserName" -Office "$City" -EmailAddress "$Email" -StreetAddress "$StreetAddress" -PostalCode "$PostalCode" -City "$City" -State "$State" -Fax "$FaxNumber" -OfficePhone "$OfficeNumber" -HomePage "$HomePage" -Title "$JobTitle" -Department "$Department"


Write-Host "Account for $FirstName $LastName has been created."
#Write-Host "Password is $Password"
