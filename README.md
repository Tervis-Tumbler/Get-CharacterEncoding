# Get-CharacterEncoding
PowerShell module for finding out the System.Text.Encoding of things

# Example
`````PowerShell
$DemandwareLogFileCharacterEncoding = Get-FileCharacterEncoding -Path $DemandwareLogFileOnDisk
if($DemandwareLogFileCharacterEncoding.EncodingName -ne "Unicode (UTF-8)") { 
            Throw @"
Appending to the end of a file instead of downloading the whole file is only supported for ASCII or UTF-8 character encoded files.
$DemandwareLogFileOnDisk's character encoding is $($DemandwareLogFileCharacterEncoding.EncodingName).
"@
}
`````
