def normalize_company_name(company_name):
    """
    Converts different CAF SoftSol name formats
    into a standard company name.

    Args:
        company_name (str): Input company name

    Returns:
        str: Standardized company name
    """

    STANDARD_NAME = "CAF SoftSol India Pvt Ltd."

    # Handle empty or None input gracefully
    if not company_name or not isinstance(company_name, str):
        return None

    # Convert to lowercase for comparison
    name = company_name.lower()

    # Check if it belongs to CAF SoftSol
    if "caf" in name and ("softsol" in name or "solution" in name):
        return STANDARD_NAME

    # If not matching, return original value
    return company_name
