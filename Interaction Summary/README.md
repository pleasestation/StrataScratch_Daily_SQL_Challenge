{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "7cc81717-da82-4ed5-8275-36264565b590",
   "metadata": {},
   "source": [
    "Interaction Summary"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1bb42ca3-4786-401b-84fe-3388250ca773",
   "metadata": {},
   "source": [
    "IBM | \n",
    "Medium\r\n",
    "ID 10542\r\n",
    "\r\n",
    "29\r\n",
    "\r\n",
    "Data En | ineer\r\n",
    "Data Sc | entist\r\n",
    "BI | Analyst\r\n",
    "Dat |  Analyst\r\n",
    "ML\n",
    " Engineer\r\n",
    "Calculate the total number of interactions and the total number of contents created for each customer. Include all interaction types and content types in your cal\n",
    "lations.\r\n",
    "\r\n",
    "\r\n",
    "Your output should include the customer's ID, the total number of interactions, and the total number of ns, user_content"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "84ae46bc-e9ec-4398-826d-d7f53591c60a",
   "metadata": {},
   "source": [
    "Tables: customer_interactions, user_content"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "d45341bf-1cb2-4914-94ee-3cdc3e00fe93",
   "metadata": {},
   "source": [
    "customer_interactions"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b637cb44-2f22-4ecc-8dd5-0c8aace578c4",
   "metadata": {},
   "source": [
    "| interaction_id | customer_id | interaction_type | interaction_date |\n",
    "|---------------|------------|------------------|------------------|\n",
    "| 1             | 7          | click           | 2024-02-13       |\n",
    "| 2             | 4          | view            | 2024-01-25       |\n",
    "| 3             | 8          | like            | 2024-02-18       |\n",
    "| 4             | 5          | like            | 2024-01-27       |\n",
    "| 5             | 7          | view            | 2024-02-28       |\n",
    "| 6             | 10         | view            | 2024-02-11       |\n",
    "| 7             | 3          | view            | 2024-01-28       |\n",
    "| 8             | 7          | like            | 2024-02-29       |\n",
    "| 9             | 8          | like            | 2024-01-16       |\n",
    "| 10            | 5          | click           | 2024-01-15       |\n",
    "| 11            | 4          | click           | 2024-02-16       |\n",
    "| 12            | 8          | like            | 2024-02-20       |\n",
    "| 13            | 8          | view            | 2024-02-13       |\n",
    "| 14            | 3          | view            | 2024-02-24       |\n",
    "| 15            | 6          | click           | 2024-02-21       |\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a05b5fcb-be10-46a4-94e8-c9966e18b32f",
   "metadata": {},
   "source": [
    "- **customer_id**: bigint  \r\n",
    "- **interaction_date**: date  \r\n",
    "- **interaction_id**: bigint  \r\n",
    "- **interaction_type**: text  \r\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f5f0df7c-e84a-4723-94b5-b8c8a1f780a4",
   "metadata": {},
   "source": [
    "user_content"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "0aa24fbe-4b84-42e3-a49b-825b1dec4e3a",
   "metadata": {},
   "source": [
    "| content_id | customer_id | content_type | content_text                           |\n",
    "|------------|-------------|--------------|----------------------------------------|\n",
    "| 1          | 2           | comment      | hello world! this is a TEST.           |\n",
    "| 2          | 8           | comment      | what a great day                       |\n",
    "| 3          | 4           | comment      | WELCOME to the event.                  |\n",
    "| 4          | 2           | comment      | e-commerce is booming.                 |\n",
    "| 5          | 6           | comment      | Python is fun!!                        |\n",
    "| 6          | 6           | review       | 123 numbers in text.                  |\n",
    "| 7          | 10          | review       | special chars: @#$$%^&*()              |\n",
    "| 8          | 4           | comment      | multiple CAPITALS here.               |\n",
    "| 9          | 6           | review       | sentence. and ANOTHER sentence!       |\n",
    "| 10         | 2           | post         | goodBYE!                               |\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "316c5521-ab5c-4f4f-acb5-bbfe466faa53",
   "metadata": {},
   "source": [
    "- **content_id**: bigint  \n",
    "- **content_text**: text  \n",
    "- **content_type**: text  \n",
    "- **customer_id**: bigint  \r\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "82b0db4d-6d00-486b-8c3b-7a877fde02a9",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
