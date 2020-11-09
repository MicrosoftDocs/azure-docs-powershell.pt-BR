---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3c96ab0cdcc25e0e1c9b4a343cd68420654d934c
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94284383"
---
# <span data-ttu-id="81baa-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="81baa-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="81baa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81baa-102">SYNOPSIS</span></span>
<span data-ttu-id="81baa-103">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="81baa-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="81baa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81baa-104">SYNTAX</span></span>

### <span data-ttu-id="81baa-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="81baa-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81baa-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81baa-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81baa-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="81baa-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81baa-120">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81baa-120">DESCRIPTION</span></span>

<span data-ttu-id="81baa-121">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="81baa-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="81baa-122">O conjunto de parâmetros padrão usa valores padrão para parâmetros se não forem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="81baa-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="81baa-123">Para obter mais informações sobre valores padrão, consulte a descrição para cada parâmetro.</span><span class="sxs-lookup"><span data-stu-id="81baa-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="81baa-124">Esse cmdlet tem a capacidade de atribuir uma função à entidade de serviço com os parâmetros **role** e **Scope** .</span><span class="sxs-lookup"><span data-stu-id="81baa-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="81baa-125">Se ambos forem omitidos, a função de colaborador será atribuída à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="81baa-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="81baa-126">Os valores padrão para os parâmetros **role** e **Scope** são **colaboradores** para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="81baa-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="81baa-127">O cmdlet cria um aplicativo e define suas propriedades se um ApplicationId não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="81baa-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="81baa-128">Para atualizar os parâmetros específicos do aplicativo, use o cmdlet [Update-AzADApplication](./update-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="81baa-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="81baa-129">Quando você cria uma entidade de serviço usando o comando **New-AzADServicePrincipal** , a saída inclui credenciais que você deve proteger.</span><span class="sxs-lookup"><span data-stu-id="81baa-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="81baa-130">Certifique-se de que você não inclui essas credenciais em seu código ou verifique as credenciais em seu controle de origem.</span><span class="sxs-lookup"><span data-stu-id="81baa-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="81baa-131">Como alternativa, considere o uso de [identidades gerenciadas](/azure/active-directory/managed-identities-azure-resources/overview) para evitar a necessidade de usar credenciais.</span><span class="sxs-lookup"><span data-stu-id="81baa-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="81baa-132">Por padrão, **New-AzADServicePrincipal** atribui a função de [colaborador](/azure/role-based-access-control/built-in-roles#contributor) à entidade de serviço no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="81baa-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="81baa-133">Para reduzir o risco de uma entidade de serviço comprometida, atribua uma função mais específica e restrinja o escopo a um recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81baa-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="81baa-134">Consulte [as etapas para adicionar uma atribuição de função](/azure/role-based-access-control/role-assignments-steps) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="81baa-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="81baa-135">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81baa-135">EXAMPLES</span></span>

### <span data-ttu-id="81baa-136">Exemplo 1: criação de entidade de serviço de anúncio simples</span><span class="sxs-lookup"><span data-stu-id="81baa-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="81baa-137">O exemplo a seguir cria uma entidade de serviço de anúncio usando valores padrão para parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="81baa-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="81baa-138">Como uma ID de aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="81baa-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="81baa-139">Como nenhum valor é fornecido para a **função** ou o **escopo** , a entidade de serviço criada é atribuída à função **colaborador** da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="81baa-139">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="81baa-140">Exemplo 2: criação de entidade de serviço de anúncio simples com função especificada e escopo padrão</span><span class="sxs-lookup"><span data-stu-id="81baa-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="81baa-141">O exemplo a seguir cria uma entidade de serviço de anúncio usando os valores padrão para os parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="81baa-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="81baa-142">Como a ID do aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="81baa-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="81baa-143">A entidade de serviço é criada com permissões de **leitor** para a assinatura atual, pois nenhum valor é fornecido para o parâmetro de **escopo** .</span><span class="sxs-lookup"><span data-stu-id="81baa-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="81baa-144">Exemplo 3: criação de entidade de serviço de anúncio simples com um escopo e função padrão especificados</span><span class="sxs-lookup"><span data-stu-id="81baa-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="81baa-145">O exemplo a seguir cria uma entidade de serviço de anúncio usando os valores padrão para os parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="81baa-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="81baa-146">Como a ID do aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="81baa-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="81baa-147">A entidade de serviço é criada com permissões de **colaborador** para o escopo do grupo de recursos fornecido, pois nenhum valor é fornecido para o parâmetro **role** .</span><span class="sxs-lookup"><span data-stu-id="81baa-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="81baa-148">Exemplo 4: criação de entidade de serviço de anúncio simples com um escopo e função especificado</span><span class="sxs-lookup"><span data-stu-id="81baa-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="81baa-149">O exemplo a seguir cria uma entidade de serviço de anúncio usando os valores padrão para os parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="81baa-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="81baa-150">Como a ID do aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="81baa-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="81baa-151">A entidade de serviço é criada com permissões de **leitor** para o escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="81baa-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="81baa-152">Exemplo 5: criar uma nova entidade de serviço de anúncio usando a ID do aplicativo com atribuição de função</span><span class="sxs-lookup"><span data-stu-id="81baa-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="81baa-153">O exemplo a seguir cria uma nova entidade de serviço de anúncio para o aplicativo com a ID de aplicativo ' 00000000-0000-0000-0000-000000000000 '.</span><span class="sxs-lookup"><span data-stu-id="81baa-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="81baa-154">Como nenhum valor é fornecido para a **função** ou o **escopo** , a entidade de serviço criada é atribuída à função **colaborador** da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="81baa-154">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="81baa-155">Exemplo 6: criar uma nova entidade de serviço de anúncio usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="81baa-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="81baa-156">O exemplo a seguir recupera o aplicativo com a ID de objeto ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' usando o cmdlet [Get-AzADApplication](./get-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="81baa-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="81baa-157">Os resultados são canalizados para o `New-AzADServicePrincipal` cmdlet para criar uma nova entidade de serviço de anúncio para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81baa-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="81baa-158">Exemplo 7: criar uma nova entidade de serviço de anúncio usando DisplayName e credenciais de senha</span><span class="sxs-lookup"><span data-stu-id="81baa-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="81baa-159">O exemplo a seguir cria um novo aplicativo com o nome **servicePrincipalName** e uma senha de **StrongPassworld! 23**.</span><span class="sxs-lookup"><span data-stu-id="81baa-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="81baa-160">Ele cria a entidade de serviço com base no aplicativo criado.</span><span class="sxs-lookup"><span data-stu-id="81baa-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="81baa-161">A data de início e a data de término são adicionadas à credencial de senha.</span><span class="sxs-lookup"><span data-stu-id="81baa-161">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="81baa-162">Exemplo 8: criar uma nova entidade de serviço de anúncio usando uma credencial de chave simples e DisplayName</span><span class="sxs-lookup"><span data-stu-id="81baa-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="81baa-163">O exemplo a seguir cria um novo aplicativo com o nome **servicePrincipalName** e um certificado **$CERT**. Ele cria a entidade de serviço com base no aplicativo criado.</span><span class="sxs-lookup"><span data-stu-id="81baa-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="81baa-164">A data de término é adicionada à credencial de chave.</span><span class="sxs-lookup"><span data-stu-id="81baa-164">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="81baa-165">OS</span><span class="sxs-lookup"><span data-stu-id="81baa-165">PARAMETERS</span></span>

### <span data-ttu-id="81baa-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="81baa-166">-ApplicationId</span></span>

<span data-ttu-id="81baa-167">A ID do aplicativo exclusivo para uma entidade de serviço em um locatário.</span><span class="sxs-lookup"><span data-stu-id="81baa-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="81baa-168">Uma vez criado, essa propriedade não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="81baa-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="81baa-169">Se uma ID de aplicativo de um aplicativo existente não for especificada, um aplicativo será criado.</span><span class="sxs-lookup"><span data-stu-id="81baa-169">If an application ID for an existing application is not specified, an application is created.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="81baa-170">-ApplicationObject</span></span>

<span data-ttu-id="81baa-171">O objeto que representa o aplicativo para o qual a entidade de serviço é criada.</span><span class="sxs-lookup"><span data-stu-id="81baa-171">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-172">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="81baa-172">-CertValue</span></span>

<span data-ttu-id="81baa-173">O valor do tipo de credencial assimétrica.</span><span class="sxs-lookup"><span data-stu-id="81baa-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="81baa-174">Ele representa o certificado codificado em base64.</span><span class="sxs-lookup"><span data-stu-id="81baa-174">It represents the Base64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81baa-175">-DefaultProfile</span></span>

<span data-ttu-id="81baa-176">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81baa-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81baa-177">-DisplayName</span></span>

<span data-ttu-id="81baa-178">O nome amigável da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="81baa-178">The friendly name of the service principal.</span></span> <span data-ttu-id="81baa-179">Se um nome de exibição não for fornecido, esse valor será definido como padrão **Azure-PowerShell-mm-dd-yyyy-hh-mm-SS** em que o sufixo é a hora da criação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81baa-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="81baa-180">-EndDate</span></span>

<span data-ttu-id="81baa-181">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="81baa-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="81baa-182">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="81baa-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="81baa-183">Para uma credencial de tipo assimétrico, isso deve ser definido como em ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="81baa-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-184">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="81baa-184">-KeyCredential</span></span>

<span data-ttu-id="81baa-185">A coleção de credenciais de chave associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81baa-185">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="81baa-186">-PasswordCredential</span></span>

<span data-ttu-id="81baa-187">A coleção de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81baa-187">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-188">-Função</span><span class="sxs-lookup"><span data-stu-id="81baa-188">-Role</span></span>

<span data-ttu-id="81baa-189">A função que a entidade de serviço tem sobre o escopo.</span><span class="sxs-lookup"><span data-stu-id="81baa-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="81baa-190">Se nenhum valor for fornecido, o padrão da **função** será a função **colaborador** .</span><span class="sxs-lookup"><span data-stu-id="81baa-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-191">-Escopo</span><span class="sxs-lookup"><span data-stu-id="81baa-191">-Scope</span></span>

<span data-ttu-id="81baa-192">O escopo ao qual a entidade de serviço tem permissões.</span><span class="sxs-lookup"><span data-stu-id="81baa-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="81baa-193">Se nenhum valor for fornecido, o **escopo** será definido como padrão para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="81baa-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="81baa-194">-SkipAssignment</span></span>

<span data-ttu-id="81baa-195">Se definido, ignore a criação da atribuição de função padrão para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="81baa-195">If set, skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="81baa-196">-StartDate</span></span>

<span data-ttu-id="81baa-197">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="81baa-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="81baa-198">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="81baa-198">The default start date value is today.</span></span> <span data-ttu-id="81baa-199">Para uma credencial de tipo assimétrico, isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="81baa-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-200">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81baa-200">-Confirm</span></span>

<span data-ttu-id="81baa-201">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81baa-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81baa-202">-WhatIf</span></span>

<span data-ttu-id="81baa-203">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81baa-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81baa-204">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81baa-204">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81baa-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81baa-205">CommonParameters</span></span>
<span data-ttu-id="81baa-206">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81baa-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81baa-207">Para obter mais informações, consulte [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="81baa-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="81baa-208">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81baa-208">INPUTS</span></span>

### <span data-ttu-id="81baa-209">System. GUID</span><span class="sxs-lookup"><span data-stu-id="81baa-209">System.Guid</span></span>

### <span data-ttu-id="81baa-210">System. String</span><span class="sxs-lookup"><span data-stu-id="81baa-210">System.String</span></span>

### <span data-ttu-id="81baa-211">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="81baa-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="81baa-212">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="81baa-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="81baa-213">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="81baa-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="81baa-214">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="81baa-214">System.DateTime</span></span>

## <span data-ttu-id="81baa-215">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81baa-215">OUTPUTS</span></span>

### <span data-ttu-id="81baa-216">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="81baa-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="81baa-217">Microsoft. Azure. Commands. Resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="81baa-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="81baa-218">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81baa-218">NOTES</span></span>

<span data-ttu-id="81baa-219">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="81baa-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="81baa-220">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81baa-220">RELATED LINKS</span></span>

[<span data-ttu-id="81baa-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="81baa-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="81baa-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="81baa-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="81baa-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="81baa-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="81baa-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="81baa-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="81baa-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="81baa-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="81baa-226">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="81baa-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="81baa-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="81baa-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)
