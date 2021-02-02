---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3a410dfb43cc767b0a73086147042425d42764d1
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251617"
---
# <span data-ttu-id="db2c3-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c3-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="db2c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="db2c3-103">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db2c3-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="db2c3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db2c3-104">SYNTAX</span></span>

### <span data-ttu-id="db2c3-105">SimpleParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db2c3-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db2c3-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db2c3-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2c3-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c3-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2c3-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="db2c3-120">DESCRIPTION</span></span>
<span data-ttu-id="db2c3-121">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db2c3-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="db2c3-122">O conjunto de parâmetros padrão usará valores padrão para parâmetros se o usuário não fornecer um para eles.</span><span class="sxs-lookup"><span data-stu-id="db2c3-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="db2c3-123">Para saber mais sobre os valores padrão usados, consulte a descrição dos parâmetros abaixo.</span><span class="sxs-lookup"><span data-stu-id="db2c3-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="db2c3-124">Este cmdlet tem a capacidade de atribuir uma função à entidade de serviço com os parâmetros e os parâmetros; se nenhum desses parâmetros for fornecido, nenhuma função será atribuída à entidade de `Role` `Scope` serviço.</span><span class="sxs-lookup"><span data-stu-id="db2c3-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="db2c3-125">Os valores padrão para os parâmetros e "Colaborador" e a assinatura atual, respectivamente ( observação: os padrões só são usados quando o usuário fornece um valor para um dos dois parâmetros, mas não o `Role` `Scope` outro).</span><span class="sxs-lookup"><span data-stu-id="db2c3-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="db2c3-126">O cmdlet também cria implicitamente um aplicativo e define suas propriedades (se o ApplicationId não for fornecido).</span><span class="sxs-lookup"><span data-stu-id="db2c3-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="db2c3-127">Para atualizar os parâmetros específicos do aplicativo, use Set-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db2c3-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="db2c3-128">Quando você cria uma entidade de serviço usando o comando **New-AzADServicePrincipal,** a saída inclui credenciais que você deve proteger.</span><span class="sxs-lookup"><span data-stu-id="db2c3-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="db2c3-129">Como alternativa, considere usar identidades [gerenciadas](/azure/active-directory/managed-identities-azure-resources/overview) para evitar a necessidade de usar credenciais.</span><span class="sxs-lookup"><span data-stu-id="db2c3-129">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="db2c3-130">Por padrão, **o New-AzADServicePrincipal** atribui a função Colaborador à entidade de serviço no escopo da assinatura. [](/azure/role-based-access-control/built-in-roles#contributor)</span><span class="sxs-lookup"><span data-stu-id="db2c3-130">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="db2c3-131">Para reduzir o risco de uma entidade de serviço comprometida, atribua uma função mais específica e restria o escopo a um grupo de recursos ou recursos.</span><span class="sxs-lookup"><span data-stu-id="db2c3-131">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="db2c3-132">Consulte [Etapas para adicionar uma atribuição de função](/azure/role-based-access-control/role-assignments-steps) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="db2c3-132">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="db2c3-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db2c3-133">EXAMPLES</span></span>

### <span data-ttu-id="db2c3-134">Exemplo 1 - Criação de entidade de serviço AD simples</span><span class="sxs-lookup"><span data-stu-id="db2c3-134">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="db2c3-135">O comando acima cria uma entidade de serviço AD usando valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="db2c3-135">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="db2c3-136">Como uma ID de aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db2c3-136">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="db2c3-137">Como nenhum valor foi fornecido ou, a entidade de serviço criada `Role` `Scope` não tem permissões.</span><span class="sxs-lookup"><span data-stu-id="db2c3-137">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="db2c3-138">Exemplo 2 - Criação de entidade de serviço AD simples com uma função especificada e escopo padrão</span><span class="sxs-lookup"><span data-stu-id="db2c3-138">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="db2c3-139">O comando acima cria uma entidade de serviço AD usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="db2c3-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="db2c3-140">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db2c3-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="db2c3-141">A entidade de serviço foi criada com permissões de "Leitor" sobre a assinatura atual (uma vez que nenhum valor foi fornecido para o `Scope` parâmetro).</span><span class="sxs-lookup"><span data-stu-id="db2c3-141">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="db2c3-142">Exemplo 3 - Criação de entidade de serviço AD simples com um escopo especificado e uma função padrão</span><span class="sxs-lookup"><span data-stu-id="db2c3-142">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="db2c3-143">O comando acima cria uma entidade de serviço AD usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="db2c3-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="db2c3-144">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db2c3-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="db2c3-145">A entidade de serviço foi criada com permissões de "Colaborador" (uma vez que nenhum valor foi fornecido para o parâmetro) sobre o `Role` escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="db2c3-145">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="db2c3-146">Exemplo 4 - Criação de entidade de serviço AD simples com um escopo e função especificados</span><span class="sxs-lookup"><span data-stu-id="db2c3-146">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="db2c3-147">O comando acima cria uma entidade de serviço AD usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="db2c3-147">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="db2c3-148">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db2c3-148">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="db2c3-149">A entidade de serviço foi criada com permissões de "Leitor" sobre o escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="db2c3-149">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="db2c3-150">Exemplo 5 - Criar uma nova entidade de serviço AD usando a ID do aplicativo com atribuição de função</span><span class="sxs-lookup"><span data-stu-id="db2c3-150">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="db2c3-151">Cria uma nova entidade de serviço do AD para o aplicativo com a ID do aplicativo '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span><span class="sxs-lookup"><span data-stu-id="db2c3-151">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="db2c3-152">Como nenhum valor foi fornecido ou, a entidade de serviço criada `Role` `Scope` não tem permissões.</span><span class="sxs-lookup"><span data-stu-id="db2c3-152">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="db2c3-153">Exemplo 6 - Criar uma nova entidade de serviço AD usando a canalização</span><span class="sxs-lookup"><span data-stu-id="db2c3-153">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="db2c3-154">Obtém o aplicativo com a ID do objeto '3ede3c26-b443-4e0b-9efc-b05e68338dc3' e os canos que para o cmdlet do New-AzADServicePrincipal para criar uma nova entidade de serviço AD para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db2c3-154">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="db2c3-155">Exemplo 7 - Criar uma nova entidade de serviço AD usando DisplayName e credencial de senha</span><span class="sxs-lookup"><span data-stu-id="db2c3-155">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="db2c3-156">Cria um novo aplicativo com o nome "ServicePrincipalName" e a senha "StrongPassworld!23" e cria a entidade de serviço com base no aplicativo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="db2c3-156">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="db2c3-157">A data de início e a data de término são adicionadas à credencial de senha.</span><span class="sxs-lookup"><span data-stu-id="db2c3-157">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="db2c3-158">Exemplo 8 - Criar uma nova entidade de serviço AD usando o DisplayName e a credencial de chave simples</span><span class="sxs-lookup"><span data-stu-id="db2c3-158">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="db2c3-159">Cria um novo aplicativo com o nome "ServicePrincipalName" e certifica "$cert" e cria a entidade de serviço com base no aplicativo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="db2c3-159">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="db2c3-160">A data de término é adicionada à credencial de chave.</span><span class="sxs-lookup"><span data-stu-id="db2c3-160">The end date is added to key credential.</span></span>

## <span data-ttu-id="db2c3-161">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db2c3-161">PARAMETERS</span></span>

### <span data-ttu-id="db2c3-162">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="db2c3-162">-ApplicationId</span></span>
<span data-ttu-id="db2c3-163">A ID do aplicativo exclusiva para uma entidade de serviço em um locatário.</span><span class="sxs-lookup"><span data-stu-id="db2c3-163">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="db2c3-164">Depois de criada, essa propriedade não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="db2c3-164">Once created this property cannot be changed.</span></span>
<span data-ttu-id="db2c3-165">Se uma ID de aplicativo não for especificada, uma será gerada.</span><span class="sxs-lookup"><span data-stu-id="db2c3-165">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="db2c3-166">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="db2c3-166">-ApplicationObject</span></span>
<span data-ttu-id="db2c3-167">O objeto que representa o aplicativo para o qual a entidade de serviço é criada.</span><span class="sxs-lookup"><span data-stu-id="db2c3-167">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="db2c3-168">-CertValue</span><span class="sxs-lookup"><span data-stu-id="db2c3-168">-CertValue</span></span>
<span data-ttu-id="db2c3-169">O valor do tipo de credencial "assimétrica".</span><span class="sxs-lookup"><span data-stu-id="db2c3-169">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="db2c3-170">Ele representa o certificado codificado de base 64.</span><span class="sxs-lookup"><span data-stu-id="db2c3-170">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="db2c3-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2c3-171">-DefaultProfile</span></span>
<span data-ttu-id="db2c3-172">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="db2c3-172">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db2c3-173">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db2c3-173">-DisplayName</span></span>
<span data-ttu-id="db2c3-174">O nome amigável da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db2c3-174">The friendly name of the service principal.</span></span> <span data-ttu-id="db2c3-175">Se um nome de exibição não for fornecido, esse valor será padrão para 'azure-powershell-MM-dd-yyyy-HH-mm-ss', onde o sufixo é o momento de criação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db2c3-175">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="db2c3-176">-EndDate</span><span class="sxs-lookup"><span data-stu-id="db2c3-176">-EndDate</span></span>
<span data-ttu-id="db2c3-177">A data de término efetiva do uso das credenciais.</span><span class="sxs-lookup"><span data-stu-id="db2c3-177">The effective end date of the credential usage.</span></span>
<span data-ttu-id="db2c3-178">O valor de data de término padrão é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="db2c3-178">The default end date value is one year from today.</span></span> <span data-ttu-id="db2c3-179">Para uma credencial de tipo "assimétrica", ela deve ser definida como em ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="db2c3-179">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="db2c3-180">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="db2c3-180">-KeyCredential</span></span>
<span data-ttu-id="db2c3-181">O conjunto de credenciais de chave associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db2c3-181">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="db2c3-182">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="db2c3-182">-PasswordCredential</span></span>
<span data-ttu-id="db2c3-183">O conjunto de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db2c3-183">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="db2c3-184">-Função</span><span class="sxs-lookup"><span data-stu-id="db2c3-184">-Role</span></span>
<span data-ttu-id="db2c3-185">A função que a entidade de serviço tem sobre o escopo.</span><span class="sxs-lookup"><span data-stu-id="db2c3-185">The role that the service principal has over the scope.</span></span> <span data-ttu-id="db2c3-186">Se um valor for fornecido, mas nenhum valor for fornecido, a função `Scope` `Role` `Role` "Colaborador" será padrão.</span><span class="sxs-lookup"><span data-stu-id="db2c3-186">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="db2c3-187">-Escopo</span><span class="sxs-lookup"><span data-stu-id="db2c3-187">-Scope</span></span>
<span data-ttu-id="db2c3-188">O escopo em que a entidade de serviço tem permissões.</span><span class="sxs-lookup"><span data-stu-id="db2c3-188">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="db2c3-189">Se um valor for fornecido, mas nenhum valor for fornecido, a assinatura atual será `Role` `Scope` `Scope` padrão.</span><span class="sxs-lookup"><span data-stu-id="db2c3-189">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="db2c3-190">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="db2c3-190">-SkipAssignment</span></span>
<span data-ttu-id="db2c3-191">Se definido, ignorará a criação da atribuição de função padrão para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db2c3-191">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="db2c3-192">-Data Inicial</span><span class="sxs-lookup"><span data-stu-id="db2c3-192">-StartDate</span></span>
<span data-ttu-id="db2c3-193">A data de início efetiva do uso das credenciais.</span><span class="sxs-lookup"><span data-stu-id="db2c3-193">The effective start date of the credential usage.</span></span>
<span data-ttu-id="db2c3-194">O valor de data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="db2c3-194">The default start date value is today.</span></span> <span data-ttu-id="db2c3-195">Para uma credencial de tipo "assimétrica", ela deve ser definida como na ou após a data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="db2c3-195">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="db2c3-196">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db2c3-196">-Confirm</span></span>
<span data-ttu-id="db2c3-197">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db2c3-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2c3-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2c3-198">-WhatIf</span></span>
<span data-ttu-id="db2c3-199">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db2c3-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2c3-200">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db2c3-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2c3-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2c3-201">CommonParameters</span></span>
<span data-ttu-id="db2c3-202">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2c3-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2c3-203">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db2c3-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2c3-204">Entradas</span><span class="sxs-lookup"><span data-stu-id="db2c3-204">INPUTS</span></span>

### <span data-ttu-id="db2c3-205">System.Guid</span><span class="sxs-lookup"><span data-stu-id="db2c3-205">System.Guid</span></span>

### <span data-ttu-id="db2c3-206">System.String</span><span class="sxs-lookup"><span data-stu-id="db2c3-206">System.String</span></span>

### <span data-ttu-id="db2c3-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="db2c3-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="db2c3-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="db2c3-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="db2c3-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="db2c3-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="db2c3-210">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="db2c3-210">System.DateTime</span></span>

## <span data-ttu-id="db2c3-211">Saídas</span><span class="sxs-lookup"><span data-stu-id="db2c3-211">OUTPUTS</span></span>

### <span data-ttu-id="db2c3-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c3-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="db2c3-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="db2c3-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="db2c3-214">Notas</span><span class="sxs-lookup"><span data-stu-id="db2c3-214">NOTES</span></span>
<span data-ttu-id="db2c3-215">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="db2c3-215">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="db2c3-216">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db2c3-216">RELATED LINKS</span></span>

[<span data-ttu-id="db2c3-217">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c3-217">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="db2c3-218">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c3-218">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="db2c3-219">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="db2c3-219">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="db2c3-220">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="db2c3-220">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="db2c3-221">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="db2c3-221">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="db2c3-222">Novo-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="db2c3-222">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="db2c3-223">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="db2c3-223">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

