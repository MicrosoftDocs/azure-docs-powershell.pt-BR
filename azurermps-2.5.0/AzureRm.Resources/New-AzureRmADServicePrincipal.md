---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 9d0fb4f188b3753e22258a27cf8632d85fe866dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786249"
---
# <span data-ttu-id="07c8e-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07c8e-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="07c8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="07c8e-103">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07c8e-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07c8e-104">SYNTAX</span></span>

### <span data-ttu-id="07c8e-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="07c8e-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07c8e-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07c8e-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c8e-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c8e-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c8e-121">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07c8e-121">DESCRIPTION</span></span>
<span data-ttu-id="07c8e-122">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07c8e-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="07c8e-123">O conjunto de parâmetros padrão usa valores padrão para parâmetros se o usuário não fornecer um para ele.</span><span class="sxs-lookup"><span data-stu-id="07c8e-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="07c8e-124">Para obter mais informações sobre os valores padrão usados, consulte a descrição para os parâmetros especificados abaixo.</span><span class="sxs-lookup"><span data-stu-id="07c8e-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="07c8e-125">Esse cmdlet tem a capacidade de atribuir uma função à entidade de serviço com os `Role` `Scope` parâmetros e; se nenhum desses parâmetros for fornecido, nenhuma função será atribuída à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="07c8e-126">Os valores padrão para os `Role` `Scope` parâmetros e são "colaborador" e a assinatura atual, respectivamente ( _Observação_ : os padrões são usados apenas quando o usuário fornece um valor para um dos dois parâmetros, mas não para o outro).</span><span class="sxs-lookup"><span data-stu-id="07c8e-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="07c8e-127">O cmdlet também cria implicitamente um aplicativo e define suas propriedades (se a ApplicationId não for fornecida).</span><span class="sxs-lookup"><span data-stu-id="07c8e-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="07c8e-128">Para atualizar os parâmetros específicos do aplicativo, use Set-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c8e-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="07c8e-129">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07c8e-129">EXAMPLES</span></span>

### <span data-ttu-id="07c8e-130">Exemplo 1-criação de entidade de serviço de anúncio simples</span><span class="sxs-lookup"><span data-stu-id="07c8e-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="07c8e-131">O comando acima cria uma entidade de serviço de anúncio usando valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="07c8e-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="07c8e-132">Como uma ID de aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="07c8e-133">Como nenhum valor foi fornecido para `Role` ou `Scope` , a entidade de serviço criada não tem nenhuma permissão.</span><span class="sxs-lookup"><span data-stu-id="07c8e-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="07c8e-134">Exemplo 2-criação de entidade de serviço de anúncio simples com função especificada e escopo padrão</span><span class="sxs-lookup"><span data-stu-id="07c8e-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="07c8e-135">O comando acima cria uma entidade de serviço de anúncio usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="07c8e-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="07c8e-136">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="07c8e-137">A entidade de serviço foi criada com permissões de "leitor" sobre a assinatura atual (já que nenhum valor foi fornecido para o `Scope` parâmetro).</span><span class="sxs-lookup"><span data-stu-id="07c8e-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="07c8e-138">Exemplo 3 – criação de entidade de serviço de anúncio simples com um escopo e função padrão especificados</span><span class="sxs-lookup"><span data-stu-id="07c8e-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="07c8e-139">O comando acima cria uma entidade de serviço de anúncio usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="07c8e-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="07c8e-140">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="07c8e-141">A entidade de serviço foi criada com permissões de "colaborador" (pois nenhum valor foi fornecido para o `Role` parâmetro) pelo escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="07c8e-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="07c8e-142">Exemplo 4 – criação de entidade de serviço de anúncio simples com um escopo e função especificado</span><span class="sxs-lookup"><span data-stu-id="07c8e-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="07c8e-143">O comando acima cria uma entidade de serviço de anúncio usando os valores padrão para parâmetros não fornecidos.</span><span class="sxs-lookup"><span data-stu-id="07c8e-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="07c8e-144">Como a ID do aplicativo não foi fornecida, um aplicativo foi criado para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="07c8e-145">A entidade de serviço foi criada com permissões de "leitor" sobre o escopo do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="07c8e-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="07c8e-146">Exemplo 5-criar uma nova entidade de serviço de anúncio usando a ID do aplicativo com atribuição de função</span><span class="sxs-lookup"><span data-stu-id="07c8e-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="07c8e-147">Cria uma nova entidade de serviço de anúncio para o aplicativo com a ID de aplicativo ' 34a28ad2-dec4-4a41-BC3B-d22ddf90000e '.</span><span class="sxs-lookup"><span data-stu-id="07c8e-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="07c8e-148">Como nenhum valor foi fornecido para `Role` ou `Scope` , a entidade de serviço criada não tem nenhuma permissão.</span><span class="sxs-lookup"><span data-stu-id="07c8e-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="07c8e-149">Exemplo 6-criar uma nova entidade de serviço de anúncio usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="07c8e-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="07c8e-150">Obtém o aplicativo com a ID de objeto ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' e canaliza-o para o cmdlet New-AzureRmADServicePrincipal para criar uma nova entidade de serviço de anúncio para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="07c8e-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="07c8e-151">OS</span><span class="sxs-lookup"><span data-stu-id="07c8e-151">PARAMETERS</span></span>

### <span data-ttu-id="07c8e-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="07c8e-152">-ApplicationId</span></span>
<span data-ttu-id="07c8e-153">A ID do aplicativo exclusivo para uma entidade de serviço em um locatário.</span><span class="sxs-lookup"><span data-stu-id="07c8e-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="07c8e-154">Uma vez criado, essa propriedade não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="07c8e-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="07c8e-155">Se uma ID de aplicativo não for especificada, uma será gerada.</span><span class="sxs-lookup"><span data-stu-id="07c8e-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="07c8e-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="07c8e-156">-ApplicationObject</span></span>
<span data-ttu-id="07c8e-157">O objeto que representa o aplicativo para o qual a entidade de serviço é criada.</span><span class="sxs-lookup"><span data-stu-id="07c8e-157">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07c8e-158">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="07c8e-158">-CertValue</span></span>
<span data-ttu-id="07c8e-159">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="07c8e-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="07c8e-160">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="07c8e-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="07c8e-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c8e-161">-DefaultProfile</span></span>
<span data-ttu-id="07c8e-162">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="07c8e-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07c8e-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="07c8e-163">-DisplayName</span></span>
<span data-ttu-id="07c8e-164">O nome amigável da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-164">The friendly name of the service principal.</span></span> <span data-ttu-id="07c8e-165">Se um nome de exibição não for fornecido, esse valor será definido como padrão ' Azure-PowerShell-MM-DD-YYYY-HH-mm-ss ', em que o sufixo é a hora da criação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="07c8e-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="07c8e-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="07c8e-166">-EndDate</span></span>
<span data-ttu-id="07c8e-167">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="07c8e-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="07c8e-168">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="07c8e-168">The default end date value is one year from today.</span></span> <span data-ttu-id="07c8e-169">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="07c8e-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="07c8e-170">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="07c8e-170">-KeyCredential</span></span>
<span data-ttu-id="07c8e-171">A coleção de credenciais de chave associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="07c8e-171">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07c8e-172">-Senha</span><span class="sxs-lookup"><span data-stu-id="07c8e-172">-Password</span></span>
<span data-ttu-id="07c8e-173">A senha a ser associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="07c8e-174">Se uma senha não for fornecida, um GUID aleatório será gerado e usado como senha.</span><span class="sxs-lookup"><span data-stu-id="07c8e-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07c8e-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="07c8e-175">-PasswordCredential</span></span>
<span data-ttu-id="07c8e-176">A coleção de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="07c8e-176">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07c8e-177">-Função</span><span class="sxs-lookup"><span data-stu-id="07c8e-177">-Role</span></span>
<span data-ttu-id="07c8e-178">A função que a entidade de serviço tem sobre o escopo.</span><span class="sxs-lookup"><span data-stu-id="07c8e-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="07c8e-179">Se um valor for `Scope` fornecido, mas nenhum valor for fornecido `Role` , `Role` o padrão será a função "colaborador".</span><span class="sxs-lookup"><span data-stu-id="07c8e-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="07c8e-180">-Escopo</span><span class="sxs-lookup"><span data-stu-id="07c8e-180">-Scope</span></span>
<span data-ttu-id="07c8e-181">O escopo do qual a entidade de serviço tem permissões.</span><span class="sxs-lookup"><span data-stu-id="07c8e-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="07c8e-182">Se um valor for `Role` fornecido, mas nenhum valor for fornecido `Scope` , `Scope` o padrão será a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="07c8e-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="07c8e-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="07c8e-183">-SkipAssignment</span></span>
<span data-ttu-id="07c8e-184">Se definido, vai ignorar a criação da atribuição de função padrão para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="07c8e-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="07c8e-185">-StartDate</span><span class="sxs-lookup"><span data-stu-id="07c8e-185">-StartDate</span></span>
<span data-ttu-id="07c8e-186">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="07c8e-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="07c8e-187">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="07c8e-187">The default start date value is today.</span></span> <span data-ttu-id="07c8e-188">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="07c8e-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="07c8e-189">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07c8e-189">-Confirm</span></span>
<span data-ttu-id="07c8e-190">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c8e-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c8e-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c8e-191">-WhatIf</span></span>
<span data-ttu-id="07c8e-192">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07c8e-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07c8e-193">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07c8e-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c8e-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c8e-194">CommonParameters</span></span>
<span data-ttu-id="07c8e-195">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c8e-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c8e-196">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c8e-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c8e-197">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07c8e-197">INPUTS</span></span>

### <span data-ttu-id="07c8e-198">System. GUID</span><span class="sxs-lookup"><span data-stu-id="07c8e-198">System.Guid</span></span>

### <span data-ttu-id="07c8e-199">System. String</span><span class="sxs-lookup"><span data-stu-id="07c8e-199">System.String</span></span>

### <span data-ttu-id="07c8e-200">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="07c8e-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="07c8e-201">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="07c8e-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="07c8e-202">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="07c8e-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="07c8e-203">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="07c8e-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="07c8e-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="07c8e-204">System.Security.SecureString</span></span>

### <span data-ttu-id="07c8e-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="07c8e-205">System.DateTime</span></span>

## <span data-ttu-id="07c8e-206">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07c8e-206">OUTPUTS</span></span>

### <span data-ttu-id="07c8e-207">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07c8e-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="07c8e-208">Microsoft. Azure. Commands. Resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="07c8e-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="07c8e-209">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07c8e-209">NOTES</span></span>
<span data-ttu-id="07c8e-210">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="07c8e-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="07c8e-211">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07c8e-211">RELATED LINKS</span></span>

[<span data-ttu-id="07c8e-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07c8e-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="07c8e-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07c8e-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="07c8e-214">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="07c8e-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="07c8e-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="07c8e-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="07c8e-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="07c8e-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="07c8e-217">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="07c8e-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="07c8e-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="07c8e-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

