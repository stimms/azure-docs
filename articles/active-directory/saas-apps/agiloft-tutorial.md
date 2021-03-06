---
title: 'Tutorial: Azure Active Directory integration with Agiloft | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and Agiloft.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 05/25/2021
ms.author: jeedes
---
# Tutorial: Azure Active Directory integration with Agiloft

In this tutorial, you'll learn how to integrate Agiloft with Azure Active Directory (Azure AD). When you integrate Agiloft with Azure AD, you can:

* Control in Azure AD who has access to Agiloft.
* Enable your users to be automatically signed-in to Agiloft with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Agiloft single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.

* Agiloft supports **SP and IDP** initiated SSO.
* Agiloft supports **Just In Time** user provisioning.

## Add Agiloft from the gallery

To configure the integration of Agiloft into Azure AD, you need to add Agiloft from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Agiloft** in the search box.
1. Select **Agiloft** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD SSO for Agiloft

Configure and test Azure AD SSO with Agiloft using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Agiloft.

To configure and test Azure AD SSO with Agiloft, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Agiloft SSO](#configure-agiloft-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Agiloft test user](#create-agiloft-test-user)** - to have a counterpart of B.Simon in Agiloft that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Agiloft** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

4. On the **Basic SAML Configuration** section, If you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.agiloft.com/<KB_NAME>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.agiloft.com:443/gui2/spsamlsso?project=<KB_NAME>`

5. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.agiloft.com/gui2/samlssologin.jsp?project=<KB_NAME>`

    > [!NOTE]
    > These values are not real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [Agiloft Client support team](https://www.agiloft.com/support-login.htm) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

6. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, click **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

    ![The Certificate download link](common/certificatebase64.png)

7. On the **Set up Agiloft** section, copy the appropriate URL(s) as per your requirement.

    ![Copy configuration URLs](common/copy-configuration-urls.png)

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Agiloft.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Agiloft**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Agiloft SSO

1. In a different web browser window, log in to your Agiloft company site as an administrator.

2. Click on **Setup** (on the Left Pane) and then select **Access**.

    ![Screenshot that highlights the Access section.](./media/agiloft-tutorial/access.png)

3. Click on the button **Configure SAML 2.0 Single Sign-On**.

    ![Screenshot that highlights the Configure SAML 2.0 Single Sign-On button.](./media/agiloft-tutorial/setup.png)

4. A wizard dialog appears. On the dialog, click on the **Identity Provider Details** and fill in the following fields:  

    ![Agiloft Configuration](./media/agiloft-tutorial/details.png)

    a. In **IdP Entity Id / Issuer** textbox, paste the value of **Azure Ad Identifier**, which you have copied from Azure portal.

    b. In **IdP Login URL** textbox, paste the value of **Login URL**, which you have copied from Azure portal.

    c. In **IdP Logout URL** textbox, paste the value of **Logout URL**, which you have copied from Azure portal.

    d. Open your **base-64 encoded certificate** in notepad downloaded from Azure portal, copy the content of it into your clipboard, and then paste it to the **IdP Provided X.509 certificate contents** textbox.

    e. Click **Finish**.

### Create Agiloft test user

In this section, a user called Britta Simon is created in Agiloft. Agiloft supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in Agiloft, a new one is created after authentication.

## Test SSO

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to Agiloft Sign on URL where you can initiate the login flow.  

* Go to Agiloft Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the Agiloft for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the Agiloft tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Agiloft for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Next steps

Once you configure Agiloft you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).
