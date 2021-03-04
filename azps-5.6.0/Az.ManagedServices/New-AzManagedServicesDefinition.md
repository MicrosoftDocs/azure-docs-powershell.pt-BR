---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 0e0163fd6a73aaf79e105ba78567d3c4048c9220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887501"
---
# <span data-ttu-id="4afe9-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="4afe9-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="4afe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4afe9-102">SYNOPSIS</span></span>
<span data-ttu-id="4afe9-103">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="4afe9-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="4afe9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4afe9-104">SYNTAX</span></span>

### <span data-ttu-id="4afe9-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4afe9-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4afe9-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="4afe9-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4afe9-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="4afe9-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4afe9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4afe9-108">DESCRIPTION</span></span>
<span data-ttu-id="4afe9-109">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="4afe9-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="4afe9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4afe9-110">EXAMPLES</span></span>

### <span data-ttu-id="4afe9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4afe9-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="4afe9-112">Cria uma definição de registro por roleDefinitionId e valores principalId dados diretamente.</span><span class="sxs-lookup"><span data-stu-id="4afe9-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="4afe9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4afe9-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="4afe9-114">Cria ou atualiza uma definição de registro com detalhes de autorização.</span><span class="sxs-lookup"><span data-stu-id="4afe9-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="4afe9-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4afe9-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="4afe9-116">Atualiza uma definição de registro com detalhes de autorização e o nome da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="4afe9-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="4afe9-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4afe9-117">PARAMETERS</span></span>

### <span data-ttu-id="4afe9-118">-Authorization</span><span class="sxs-lookup"><span data-stu-id="4afe9-118">-Authorization</span></span>
<span data-ttu-id="4afe9-119">A lista de mapeamento de autorização com principalId - roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="4afe9-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afe9-120">-DefaultProfile</span></span>
<span data-ttu-id="4afe9-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4afe9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4afe9-122">-Description</span><span class="sxs-lookup"><span data-stu-id="4afe9-122">-Description</span></span>
<span data-ttu-id="4afe9-123">A descrição da Definição de Registro.</span><span class="sxs-lookup"><span data-stu-id="4afe9-123">The description of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4afe9-124">-DisplayName</span></span>
<span data-ttu-id="4afe9-125">O nome de exibição da Definição de Registro.</span><span class="sxs-lookup"><span data-stu-id="4afe9-125">The display name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="4afe9-126">-ManagedByTenantId</span></span>
<span data-ttu-id="4afe9-127">O Identificador de Locatário ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="4afe9-127">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4afe9-128">-Name</span></span>
<span data-ttu-id="4afe9-129">O nome exclusivo da Definição de Registro.</span><span class="sxs-lookup"><span data-stu-id="4afe9-129">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4afe9-130">-PlanName</span></span>
<span data-ttu-id="4afe9-131">O nome do plano.</span><span class="sxs-lookup"><span data-stu-id="4afe9-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="4afe9-132">-PlanProduct</span></span>
<span data-ttu-id="4afe9-133">O nome do Produto.</span><span class="sxs-lookup"><span data-stu-id="4afe9-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4afe9-134">-PlanPublisher</span></span>
<span data-ttu-id="4afe9-135">O nome do Publisher.</span><span class="sxs-lookup"><span data-stu-id="4afe9-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="4afe9-136">-PlanVersion</span></span>
<span data-ttu-id="4afe9-137">O número da versão do plano.</span><span class="sxs-lookup"><span data-stu-id="4afe9-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="4afe9-138">-PrincipalId</span></span>
<span data-ttu-id="4afe9-139">O Identificador De entidade ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="4afe9-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4afe9-140">-RoleDefinitionId</span></span>
<span data-ttu-id="4afe9-141">O identificador de definição de função para conceder permissões ao identificador principal.</span><span class="sxs-lookup"><span data-stu-id="4afe9-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4afe9-142">-AsJob</span></span>
<span data-ttu-id="4afe9-143">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4afe9-143">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4afe9-144">-Confirm</span></span>
<span data-ttu-id="4afe9-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4afe9-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afe9-146">-WhatIf</span></span>
<span data-ttu-id="4afe9-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4afe9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afe9-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4afe9-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afe9-149">CommonParameters</span></span>
<span data-ttu-id="4afe9-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afe9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afe9-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4afe9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afe9-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4afe9-152">INPUTS</span></span>

### <span data-ttu-id="4afe9-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4afe9-153">None</span></span>
## <span data-ttu-id="4afe9-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4afe9-154">OUTPUTS</span></span>

### <span data-ttu-id="4afe9-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="4afe9-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="4afe9-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="4afe9-156">NOTES</span></span>

## <span data-ttu-id="4afe9-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4afe9-157">RELATED LINKS</span></span>
