To install **Terraform** and **AWS CLI** on GitHub Codespaces, follow these steps:

1. Open your **GitHub Codespace** and navigate to the **search bar**.
   
2. Type `>dev` and select **Add dev container configuration file**.

3. In the pop-up that appears, click on **Modify your active configuration**.

4. Search for **Terraform** and select the **verified** version from the list.

5. Click **OK** and keep the default settings.

6. Again, open the **search bar** and type `>dev`, then choose **Add dev container configuration file**.

7. In the pop-up, select **Modify your active configuration**.

8. Search for **AWS CLI** and select the **verified** version of AWS CLI from the list.

9. Click **OK** and keep the default settings.

10. Now, search for **Rebuild** in the search bar and select **Rebuild Container**.

11. Wait for the container to rebuild.

12. Once the rebuild is complete, verify that **Terraform** and **AWS CLI** are installed by running the following commands in the terminal:
   - For Terraform: `terraform --version`
   - For AWS CLI: `aws --version`

If both commands return the installed versions, you have successfully installed Terraform and AWS CLI on GitHub Codespaces!
