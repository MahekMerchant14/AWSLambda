# AWSLambda
def is_anagram(str1, str2):
    # Convert both strings to lowercase
    str1 = str1.lower()
    str2 = str2.lower()

    # Sort the characters in both strings
    sorted_str1 = sorted(str1)
    sorted_str2 = sorted(str2)

    # Check if the sorted strings are equal
    return sorted_str1 == sorted_str2

def lambda_handler(event, context):
    str1 = event['str1']
    str2 = event['str2']

    # Check if the strings are anagrams
    result = is_anagram(str1, str2)

    return {
        'is_anagram': result
    }
