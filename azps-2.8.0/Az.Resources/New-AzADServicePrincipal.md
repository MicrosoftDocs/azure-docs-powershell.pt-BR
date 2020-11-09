---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9db3e3d0fcb52869a53b4bd2b76603d2935c4dd0
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "93786672"
---
# <span data-ttu-id="b7f05-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7f05-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="b7f05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7f05-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f05-103">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7f05-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="b7f05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7f05-104">SYNTAX</span></span>

### <span data-ttu-id="b7f05-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b7f05-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7f05-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7f05-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f05-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f05-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f05-121">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7f05-121">DESCRIPTION</span></span>
<span data-ttu-id="b7f05-122">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7f05-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="b7f05-123">O conjunto de parâmetros padrão usa valores padrão para parâmetros se o usuário não fornecer um para ele.</span><span class="sxs-lookup"><span data-stu-id="b7f05-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="b7f05-124">Para obter mais informações sobre os valores padrão usados, consulte a descrição para os parâmetros especificados abaixo.</span><span class="sxs-lookup"><span data-stu-id="b7f05-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="b7f05-125">Esse cmdlet tem a capacidade de atribuir uma função à entidade de serviço com os `Role` `Scope` parâmetros e; se nenhum desses parâmetros for fornecido, nenhuma função será atribuída à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7f05-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="b7f05-126">Os valores padrão para os `Role` `Scope` parâmetros e são "colaborador" e a assinatura atual, respectivamente ( _Observação_ : os padrões são usados apenas quando o usuário fornece um valor para um dos dois parâmetros, mas não para o outro).</span><span class="sxs-lookup"><span data-stu-id="b7f05-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="b7f05-127">O cmdlet também cria implicitamente um aplicativo e define suas propriedades (se a ApplicationId não for fornecida).</span><span class="sxs-lookup"><span data-stu-id="b7f05-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="b7f05-128">Para atualizar os parâmetros específicos do aplicativo, use Set-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f05-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="b7f05-129">Quando você cria uma entidade de serviço usando o comando **New-AzADServicePrincipal** , a saída inclui credenciais que você deve proteger.</span><span class="sxs-lookup"><span data-stu-id="b7f05-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="b7f05-130">Certifique-se de que você não inclui essas credenciais em seu código ou verifique as credenciais em seu controle de origem.</span><span class="sxs-lookup"><span data-stu-id="b7f05-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="b7f05-131">Como alternativa, considere o uso de [identidades gerenciadas](/azure/active-directory/managed-identities-azure-resources/overview) para evitar a necessidade de usar credenciais.</span><span class="sxs-lookup"><span data-stu-id="b7f05-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="b7f05-132">Por padrão, **New-AzADServicePrincipal** atribui a função de [colaborador](/azure/role-based-access-control/built-in-roles#contributor) à entidade de serviço no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b7f05-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="b7f05-133">Para reduzir o risco de uma entidade de serviço comprometida, atribua uma função mais específica e restrinja o escopo a um recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7f05-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="b7f05-134">Consulte [as etapas para adicionar uma atribuição de função](/azure/role-based-access-control/role-assignments-steps) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b7f05-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="b7f05-135">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7f05-135">EXAMPLES</span></span>

### <span data-ttu-id="b7f05-136">Exemplo 1-criação de entidade de serviço de anúncio simples</span><span class="sxs-lookup"><span data-stu-id="b7f05-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="b7f05-137">O comando acima cria uma entidade de serviço de anúncio usando valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b7f05-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="b7f05-138">Como uma ID de aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7f05-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b7f05-139">Como nenhum valor foi fornecido para `Role` ou `Scope` , a entidade de serviço criada não tem nenhuma permissão.</span><span class="sxs-lookup"><span data-stu-id="b7f05-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="b7f05-140">Exemplo 2-criação de entidade de serviço de anúncio simples com função especificada e escopo padrão</span><span class="sxs-lookup"><span data-stu-id="b7f05-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="b7f05-141">O comando acima cria uma entidade de serviço de anúncio usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b7f05-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b7f05-142">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7f05-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b7f05-143">A entidade de serviço foi criada com permissões de "leitor" sobre a assinatura atual (já que nenhum valor foi fornecido para o `Scope` parâmetro).</span><span class="sxs-lookup"><span data-stu-id="b7f05-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="b7f05-144">Exemplo 3 – criação de entidade de serviço de anúncio simples com um escopo e função padrão especificados</span><span class="sxs-lookup"><span data-stu-id="b7f05-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="b7f05-145">O comando acima cria uma entidade de serviço de anúncio usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b7f05-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b7f05-146">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7f05-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b7f05-147">A entidade de serviço foi criada com permissões de "colaborador" (pois nenhum valor foi fornecido para o `Role` parâmetro) pelo escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="b7f05-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="b7f05-148">Exemplo 4 – criação de entidade de serviço de anúncio simples com um escopo e função especificado</span><span class="sxs-lookup"><span data-stu-id="b7f05-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="b7f05-149">O comando acima cria uma entidade de serviço de anúncio usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b7f05-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b7f05-150">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7f05-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b7f05-151">A entidade de serviço foi criada com permissões de "leitor" sobre o escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="b7f05-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="b7f05-152">Exemplo 5-criar uma nova entidade de serviço de anúncio usando a ID do aplicativo com atribuição de função</span><span class="sxs-lookup"><span data-stu-id="b7f05-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="b7f05-153">Cria uma nova entidade de serviço de anúncio para o aplicativo com a ID de aplicativo ' 34a28ad2-dec4-4a41-BC3B-d22ddf90000e '.</span><span class="sxs-lookup"><span data-stu-id="b7f05-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="b7f05-154">Como nenhum valor foi fornecido para `Role` ou `Scope` , a entidade de serviço criada não tem nenhuma permissão.</span><span class="sxs-lookup"><span data-stu-id="b7f05-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="b7f05-155">Exemplo 6-criar uma nova entidade de serviço de anúncio usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="b7f05-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="b7f05-156">Obtém o aplicativo com a ID de objeto ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' e canaliza-o para o cmdlet New-AzADServicePrincipal para criar uma nova entidade de serviço de anúncio para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7f05-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="b7f05-157">OS</span><span class="sxs-lookup"><span data-stu-id="b7f05-157">PARAMETERS</span></span>

### <span data-ttu-id="b7f05-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b7f05-158">-ApplicationId</span></span>
<span data-ttu-id="b7f05-159">A ID do aplicativo exclusivo para uma entidade de serviço em um locatário.</span><span class="sxs-lookup"><span data-stu-id="b7f05-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="b7f05-160">Uma vez criado, essa propriedade não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="b7f05-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="b7f05-161">Se uma ID de aplicativo não for especificada, uma será gerada.</span><span class="sxs-lookup"><span data-stu-id="b7f05-161">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="b7f05-162">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="b7f05-162">-ApplicationObject</span></span>
<span data-ttu-id="b7f05-163">O objeto que representa o aplicativo para o qual a entidade de serviço é criada.</span><span class="sxs-lookup"><span data-stu-id="b7f05-163">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f05-164">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="b7f05-164">-CertValue</span></span>
<span data-ttu-id="b7f05-165">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="b7f05-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b7f05-166">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="b7f05-166">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="b7f05-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f05-167">-DefaultProfile</span></span>
<span data-ttu-id="b7f05-168">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b7f05-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7f05-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7f05-169">-DisplayName</span></span>
<span data-ttu-id="b7f05-170">O nome amigável da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7f05-170">The friendly name of the service principal.</span></span> <span data-ttu-id="b7f05-171">Se um nome de exibição não for fornecido, esse valor será definido como padrão ' Azure-PowerShell-MM-DD-YYYY-HH-mm-ss ', em que o sufixo é a hora da criação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7f05-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="b7f05-172">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b7f05-172">-EndDate</span></span>
<span data-ttu-id="b7f05-173">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="b7f05-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b7f05-174">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="b7f05-174">The default end date value is one year from today.</span></span> <span data-ttu-id="b7f05-175">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="b7f05-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b7f05-176">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="b7f05-176">-KeyCredential</span></span>
<span data-ttu-id="b7f05-177">A coleção de credenciais de chave associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7f05-177">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="b7f05-178">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="b7f05-178">-PasswordCredential</span></span>
<span data-ttu-id="b7f05-179">A coleção de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7f05-179">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="b7f05-180">-Função</span><span class="sxs-lookup"><span data-stu-id="b7f05-180">-Role</span></span>
<span data-ttu-id="b7f05-181">A função que a entidade de serviço tem sobre o escopo.</span><span class="sxs-lookup"><span data-stu-id="b7f05-181">The role that the service principal has over the scope.</span></span> <span data-ttu-id="b7f05-182">Se um valor for `Scope` fornecido, mas nenhum valor for fornecido `Role` , `Role` o padrão será a função "colaborador".</span><span class="sxs-lookup"><span data-stu-id="b7f05-182">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="b7f05-183">-Escopo</span><span class="sxs-lookup"><span data-stu-id="b7f05-183">-Scope</span></span>
<span data-ttu-id="b7f05-184">O escopo do qual a entidade de serviço tem permissões.</span><span class="sxs-lookup"><span data-stu-id="b7f05-184">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="b7f05-185">Se um valor for `Role` fornecido, mas nenhum valor for fornecido `Scope` , `Scope` o padrão será a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b7f05-185">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="b7f05-186">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="b7f05-186">-SkipAssignment</span></span>
<span data-ttu-id="b7f05-187">Se definido, vai ignorar a criação da atribuição de função padrão para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7f05-187">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="b7f05-188">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b7f05-188">-StartDate</span></span>
<span data-ttu-id="b7f05-189">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="b7f05-189">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b7f05-190">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="b7f05-190">The default start date value is today.</span></span> <span data-ttu-id="b7f05-191">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="b7f05-191">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b7f05-192">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7f05-192">-Confirm</span></span>
<span data-ttu-id="b7f05-193">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f05-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f05-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f05-194">-WhatIf</span></span>
<span data-ttu-id="b7f05-195">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7f05-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7f05-196">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7f05-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f05-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f05-197">CommonParameters</span></span>
<span data-ttu-id="b7f05-198">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f05-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f05-199">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f05-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f05-200">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7f05-200">INPUTS</span></span>

### <span data-ttu-id="b7f05-201">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b7f05-201">System.Guid</span></span>

### <span data-ttu-id="b7f05-202">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f05-202">System.String</span></span>

### <span data-ttu-id="b7f05-203">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b7f05-203">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="b7f05-204">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="b7f05-204">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="b7f05-205">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="b7f05-205">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="b7f05-206">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="b7f05-206">System.DateTime</span></span>

## <span data-ttu-id="b7f05-207">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7f05-207">OUTPUTS</span></span>

### <span data-ttu-id="b7f05-208">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7f05-208">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="b7f05-209">Microsoft. Azure. Commands. Resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="b7f05-209">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="b7f05-210">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7f05-210">NOTES</span></span>
<span data-ttu-id="b7f05-211">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="b7f05-211">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b7f05-212">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7f05-212">RELATED LINKS</span></span>

[<span data-ttu-id="b7f05-213">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7f05-213">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="b7f05-214">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7f05-214">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="b7f05-215">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b7f05-215">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="b7f05-216">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b7f05-216">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="b7f05-217">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7f05-217">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="b7f05-218">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7f05-218">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="b7f05-219">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7f05-219">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

