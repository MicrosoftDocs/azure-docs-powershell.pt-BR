---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f826ecbde81bc301cc51e031b2047bc7a9f284e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890083"
---
# <span data-ttu-id="671cd-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="671cd-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="671cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="671cd-102">SYNOPSIS</span></span>
<span data-ttu-id="671cd-103">Cria uma nova entidade de serviço do Active Directory do Azure.</span><span class="sxs-lookup"><span data-stu-id="671cd-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="671cd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="671cd-104">SYNTAX</span></span>

### <span data-ttu-id="671cd-105">SimpleParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="671cd-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="671cd-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="671cd-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="671cd-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="671cd-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="671cd-120">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="671cd-120">DESCRIPTION</span></span>

<span data-ttu-id="671cd-121">Cria uma nova entidade de serviço do Active Directory do Azure.</span><span class="sxs-lookup"><span data-stu-id="671cd-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="671cd-122">O conjunto de parâmetros padrão usa valores padrão para parâmetros se eles não são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="671cd-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="671cd-123">Para obter mais informações sobre valores padrão, consulte a descrição de cada parâmetro.</span><span class="sxs-lookup"><span data-stu-id="671cd-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="671cd-124">Este cmdlet tem a capacidade de atribuir uma função à entidade de serviço com os parâmetros **Role** e **Scope.**</span><span class="sxs-lookup"><span data-stu-id="671cd-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="671cd-125">Se ambos são omitidos, a função de colaborador é atribuída à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="671cd-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="671cd-126">Os valores padrão para os parâmetros **Role** e **Scope** são **Colaborador** para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="671cd-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="671cd-127">O cmdlet cria um aplicativo e define suas propriedades se um ApplicationId não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="671cd-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="671cd-128">Para atualizar os parâmetros específicos do aplicativo, use o cmdlet [Update-AzADApplication.](./update-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="671cd-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="671cd-129">Quando você cria uma entidade de serviço usando **o comando New-AzADServicePrincipal,** a saída inclui credenciais que você deve proteger.</span><span class="sxs-lookup"><span data-stu-id="671cd-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="671cd-130">Como alternativa, considere o uso [de identidades gerenciadas](/azure/active-directory/managed-identities-azure-resources/overview) para evitar a necessidade de usar credenciais.</span><span class="sxs-lookup"><span data-stu-id="671cd-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="671cd-131">Por padrão, **New-AzADServicePrincipal** atribui a função [Colaborador](/azure/role-based-access-control/built-in-roles#contributor) à entidade de serviço no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="671cd-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="671cd-132">Para reduzir o risco de uma entidade de serviço comprometida, atribua uma função mais específica e reduza o escopo a um grupo de recursos ou recursos.</span><span class="sxs-lookup"><span data-stu-id="671cd-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="671cd-133">Consulte [Etapas para adicionar uma atribuição de função](/azure/role-based-access-control/role-assignments-steps) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="671cd-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="671cd-134">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="671cd-134">EXAMPLES</span></span>

### <span data-ttu-id="671cd-135">Exemplo 1: criação da entidade de serviço AD simples</span><span class="sxs-lookup"><span data-stu-id="671cd-135">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="671cd-136">O exemplo a seguir cria uma entidade de serviço do AD usando valores padrão para parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="671cd-136">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="671cd-137">Como uma ID de aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="671cd-137">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="671cd-138">Como nenhum valor é fornecido para **Função** ou **Escopo,** a entidade de serviço criada recebe a função de colaborador da assinatura atual. </span><span class="sxs-lookup"><span data-stu-id="671cd-138">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="671cd-139">Exemplo 2: criação da entidade de serviço AD simples com uma função especificada e escopo padrão</span><span class="sxs-lookup"><span data-stu-id="671cd-139">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="671cd-140">O exemplo a seguir cria uma entidade de serviço do AD usando os valores padrão para parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="671cd-140">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="671cd-141">Como a ID do aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="671cd-141">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="671cd-142">A entidade de serviço é criada com **permissões de** leitor para a assinatura atual, já que nenhum valor é fornecido para o **parâmetro Scope.**</span><span class="sxs-lookup"><span data-stu-id="671cd-142">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="671cd-143">Exemplo 3: criação da entidade de serviço AD simples com um escopo especificado e uma função padrão</span><span class="sxs-lookup"><span data-stu-id="671cd-143">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="671cd-144">O exemplo a seguir cria uma entidade de serviço do AD usando os valores padrão para parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="671cd-144">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="671cd-145">Como a ID do aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="671cd-145">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="671cd-146">A entidade de serviço é criada com **permissões colaboradoras** para o escopo do grupo de recursos fornecido, pois nenhum valor é fornecido para o **parâmetro Role.**</span><span class="sxs-lookup"><span data-stu-id="671cd-146">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="671cd-147">Exemplo 4: criação da entidade de serviço AD simples com um escopo e função especificados</span><span class="sxs-lookup"><span data-stu-id="671cd-147">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="671cd-148">O exemplo a seguir cria uma entidade de serviço do AD usando os valores padrão para parâmetros não especificados.</span><span class="sxs-lookup"><span data-stu-id="671cd-148">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="671cd-149">Como a ID do aplicativo não é fornecida, um aplicativo é criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="671cd-149">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="671cd-150">A entidade de serviço é criada com **permissões de** leitor para o escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="671cd-150">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="671cd-151">Exemplo 5: Criar uma nova entidade de serviço do AD usando a ID do aplicativo com atribuição de função</span><span class="sxs-lookup"><span data-stu-id="671cd-151">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="671cd-152">O exemplo a seguir cria uma nova entidade de serviço do AD para o aplicativo com a ID do aplicativo '000000000-0000-0000-00000000000000000'.</span><span class="sxs-lookup"><span data-stu-id="671cd-152">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="671cd-153">Como nenhum valor é fornecido para **Função** ou **Escopo,** a entidade de serviço criada recebe a função de colaborador da assinatura atual. </span><span class="sxs-lookup"><span data-stu-id="671cd-153">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="671cd-154">Exemplo 6: Criar uma nova entidade de serviço do AD usando a canalização</span><span class="sxs-lookup"><span data-stu-id="671cd-154">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="671cd-155">O exemplo a seguir recupera o aplicativo com a ID do objeto '3ede3c26-b443-4e0b-9efc-b05e68338dc3' usando o cmdlet [Get-AzADApplication.](./get-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="671cd-155">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="671cd-156">Os resultados são canalados para o cmdlet para criar uma nova entidade de serviço `New-AzADServicePrincipal` do AD para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="671cd-156">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="671cd-157">Exemplo 7: Criar uma nova entidade de serviço do AD usando DisplayName e credencial de senha</span><span class="sxs-lookup"><span data-stu-id="671cd-157">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="671cd-158">O exemplo a seguir cria um novo aplicativo com o nome **ServicePrincipalName** e uma senha **de StrongPassworld!23**.</span><span class="sxs-lookup"><span data-stu-id="671cd-158">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="671cd-159">Ele cria a entidade de serviço com base no aplicativo criado.</span><span class="sxs-lookup"><span data-stu-id="671cd-159">It creates the service principal based on the created application.</span></span> <span data-ttu-id="671cd-160">A data de início e a data de término são adicionadas à credencial de senha.</span><span class="sxs-lookup"><span data-stu-id="671cd-160">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="671cd-161">Exemplo 8: Criar uma nova entidade de serviço do AD usando DisplayName e a credencial de chave simples</span><span class="sxs-lookup"><span data-stu-id="671cd-161">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="671cd-162">O exemplo a seguir cria um novo aplicativo com o nome **ServicePrincipalName** e um certificado **$cert**. Ele cria a entidade de serviço com base no aplicativo criado.</span><span class="sxs-lookup"><span data-stu-id="671cd-162">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="671cd-163">A data de término é adicionada à credencial da chave.</span><span class="sxs-lookup"><span data-stu-id="671cd-163">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="671cd-164">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="671cd-164">PARAMETERS</span></span>

### <span data-ttu-id="671cd-165">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="671cd-165">-ApplicationId</span></span>

<span data-ttu-id="671cd-166">A ID do aplicativo exclusiva para uma entidade de serviço em um locatário.</span><span class="sxs-lookup"><span data-stu-id="671cd-166">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="671cd-167">Uma vez criada, essa propriedade não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="671cd-167">Once created this property cannot be changed.</span></span> <span data-ttu-id="671cd-168">Se uma ID de aplicativo para um aplicativo existente não for especificada, um aplicativo será criado.</span><span class="sxs-lookup"><span data-stu-id="671cd-168">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="671cd-169">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="671cd-169">-ApplicationObject</span></span>

<span data-ttu-id="671cd-170">O objeto que representa o aplicativo para o qual a entidade de serviço é criada.</span><span class="sxs-lookup"><span data-stu-id="671cd-170">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="671cd-171">-CertValue</span><span class="sxs-lookup"><span data-stu-id="671cd-171">-CertValue</span></span>

<span data-ttu-id="671cd-172">O valor do tipo de credencial assimétrico.</span><span class="sxs-lookup"><span data-stu-id="671cd-172">The value of the asymmetric credential type.</span></span> <span data-ttu-id="671cd-173">Ele representa o certificado codificado base64.</span><span class="sxs-lookup"><span data-stu-id="671cd-173">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="671cd-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="671cd-174">-DefaultProfile</span></span>

<span data-ttu-id="671cd-175">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="671cd-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="671cd-176">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="671cd-176">-DisplayName</span></span>

<span data-ttu-id="671cd-177">O nome amigável da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="671cd-177">The friendly name of the service principal.</span></span> <span data-ttu-id="671cd-178">Se um nome de exibição não for fornecido, esse valor será padrão para **azure-powershell-MM-dd-yyyy-HH-mm-ss** onde o sufixo é o momento da criação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="671cd-178">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="671cd-179">-EndDate</span><span class="sxs-lookup"><span data-stu-id="671cd-179">-EndDate</span></span>

<span data-ttu-id="671cd-180">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="671cd-180">The effective end date of the credential usage.</span></span> <span data-ttu-id="671cd-181">O valor de data de término padrão é de um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="671cd-181">The default end date value is one year from today.</span></span>
<span data-ttu-id="671cd-182">Para uma credencial de tipo assimétrica, ela deve ser definida como em ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="671cd-182">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="671cd-183">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="671cd-183">-KeyCredential</span></span>

<span data-ttu-id="671cd-184">A coleção de credenciais principais associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="671cd-184">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="671cd-185">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="671cd-185">-PasswordCredential</span></span>

<span data-ttu-id="671cd-186">A coleção de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="671cd-186">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="671cd-187">-Role</span><span class="sxs-lookup"><span data-stu-id="671cd-187">-Role</span></span>

<span data-ttu-id="671cd-188">A função que a entidade de serviço tem sobre o escopo.</span><span class="sxs-lookup"><span data-stu-id="671cd-188">The role that the service principal has over the scope.</span></span> <span data-ttu-id="671cd-189">Se nenhum valor for fornecido, **a função** será padrão para a **função Colaborador.**</span><span class="sxs-lookup"><span data-stu-id="671cd-189">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="671cd-190">-Scope</span><span class="sxs-lookup"><span data-stu-id="671cd-190">-Scope</span></span>

<span data-ttu-id="671cd-191">O escopo para o que a entidade de serviço tem permissões.</span><span class="sxs-lookup"><span data-stu-id="671cd-191">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="671cd-192">Se nenhum valor for fornecido, **o escopo** será padrão para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="671cd-192">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="671cd-193">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="671cd-193">-SkipAssignment</span></span>

<span data-ttu-id="671cd-194">Se definido, ignore a criação da atribuição de função padrão para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="671cd-194">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="671cd-195">-StartDate</span><span class="sxs-lookup"><span data-stu-id="671cd-195">-StartDate</span></span>

<span data-ttu-id="671cd-196">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="671cd-196">The effective start date of the credential usage.</span></span> <span data-ttu-id="671cd-197">O valor de data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="671cd-197">The default start date value is today.</span></span> <span data-ttu-id="671cd-198">Para uma credencial de tipo assimétrica, ela deve ser definida como em ou após a data da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="671cd-198">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="671cd-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="671cd-199">-Confirm</span></span>

<span data-ttu-id="671cd-200">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="671cd-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="671cd-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="671cd-201">-WhatIf</span></span>

<span data-ttu-id="671cd-202">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="671cd-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="671cd-203">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="671cd-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="671cd-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="671cd-204">CommonParameters</span></span>
<span data-ttu-id="671cd-205">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="671cd-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="671cd-206">Para obter mais informações, [consulte about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="671cd-206">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="671cd-207">INPUTS</span><span class="sxs-lookup"><span data-stu-id="671cd-207">INPUTS</span></span>

### <span data-ttu-id="671cd-208">System.Guid</span><span class="sxs-lookup"><span data-stu-id="671cd-208">System.Guid</span></span>

### <span data-ttu-id="671cd-209">System.String</span><span class="sxs-lookup"><span data-stu-id="671cd-209">System.String</span></span>

### <span data-ttu-id="671cd-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="671cd-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="671cd-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="671cd-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="671cd-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="671cd-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="671cd-213">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="671cd-213">System.DateTime</span></span>

## <span data-ttu-id="671cd-214">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="671cd-214">OUTPUTS</span></span>

### <span data-ttu-id="671cd-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="671cd-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="671cd-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="671cd-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="671cd-217">NOTES</span><span class="sxs-lookup"><span data-stu-id="671cd-217">NOTES</span></span>

<span data-ttu-id="671cd-218">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="671cd-218">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="671cd-219">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="671cd-219">RELATED LINKS</span></span>

[<span data-ttu-id="671cd-220">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="671cd-220">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="671cd-221">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="671cd-221">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="671cd-222">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="671cd-222">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="671cd-223">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="671cd-223">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="671cd-224">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="671cd-224">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="671cd-225">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="671cd-225">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="671cd-226">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="671cd-226">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)