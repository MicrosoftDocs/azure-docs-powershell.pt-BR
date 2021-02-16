---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113584"
---
# <span data-ttu-id="a334d-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a334d-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="a334d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a334d-102">SYNOPSIS</span></span>
<span data-ttu-id="a334d-103">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="a334d-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="a334d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a334d-104">SYNTAX</span></span>

### <span data-ttu-id="a334d-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a334d-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a334d-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="a334d-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a334d-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="a334d-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a334d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a334d-108">DESCRIPTION</span></span>
<span data-ttu-id="a334d-109">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="a334d-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="a334d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a334d-110">EXAMPLES</span></span>

### <span data-ttu-id="a334d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a334d-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="a334d-112">Cria uma definição de registro por roleDefinitionId e valores principalId dados diretamente.</span><span class="sxs-lookup"><span data-stu-id="a334d-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="a334d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a334d-113">Example 2</span></span>
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

<span data-ttu-id="a334d-114">Cria ou atualiza uma definição de registro com detalhes de autorização.</span><span class="sxs-lookup"><span data-stu-id="a334d-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="a334d-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a334d-115">Example 3</span></span>
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

<span data-ttu-id="a334d-116">Atualiza uma definição de registro com detalhes de autorização e o nome da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="a334d-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="a334d-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a334d-117">PARAMETERS</span></span>

### <span data-ttu-id="a334d-118">-Autorização</span><span class="sxs-lookup"><span data-stu-id="a334d-118">-Authorization</span></span>
<span data-ttu-id="a334d-119">A lista de mapeamento de autorização com principalId - roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="a334d-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

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

### <span data-ttu-id="a334d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a334d-120">-DefaultProfile</span></span>
<span data-ttu-id="a334d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a334d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a334d-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a334d-122">-Description</span></span>
<span data-ttu-id="a334d-123">A descrição da Definição de Registro.</span><span class="sxs-lookup"><span data-stu-id="a334d-123">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="a334d-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a334d-124">-DisplayName</span></span>
<span data-ttu-id="a334d-125">O nome de exibição da Definição de Registro.</span><span class="sxs-lookup"><span data-stu-id="a334d-125">The display name of the Registration Definition.</span></span>

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

### <span data-ttu-id="a334d-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="a334d-126">-ManagedByTenantId</span></span>
<span data-ttu-id="a334d-127">O Identificador de Locatário ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="a334d-127">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="a334d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a334d-128">-Name</span></span>
<span data-ttu-id="a334d-129">O nome exclusivo da Definição de Registro.</span><span class="sxs-lookup"><span data-stu-id="a334d-129">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="a334d-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="a334d-130">-PlanName</span></span>
<span data-ttu-id="a334d-131">O nome do plano.</span><span class="sxs-lookup"><span data-stu-id="a334d-131">The name of the plan.</span></span>

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

### <span data-ttu-id="a334d-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="a334d-132">-PlanProduct</span></span>
<span data-ttu-id="a334d-133">O nome do Produto.</span><span class="sxs-lookup"><span data-stu-id="a334d-133">The name of the Product.</span></span>

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

### <span data-ttu-id="a334d-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="a334d-134">-PlanPublisher</span></span>
<span data-ttu-id="a334d-135">O nome do Publisher.</span><span class="sxs-lookup"><span data-stu-id="a334d-135">The name of the Publisher.</span></span>

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

### <span data-ttu-id="a334d-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="a334d-136">-PlanVersion</span></span>
<span data-ttu-id="a334d-137">O número da versão do plano.</span><span class="sxs-lookup"><span data-stu-id="a334d-137">The version number of the plan.</span></span>

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

### <span data-ttu-id="a334d-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="a334d-138">-PrincipalId</span></span>
<span data-ttu-id="a334d-139">O Identificador ManagedBy Principal.</span><span class="sxs-lookup"><span data-stu-id="a334d-139">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="a334d-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a334d-140">-RoleDefinitionId</span></span>
<span data-ttu-id="a334d-141">O identificador de definição de função para conceder permissões ao identificador principal.</span><span class="sxs-lookup"><span data-stu-id="a334d-141">The role definition identifier to grant permissions to principal identifier.</span></span>

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

### <span data-ttu-id="a334d-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a334d-142">-AsJob</span></span>
<span data-ttu-id="a334d-143">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a334d-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a334d-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a334d-144">-Confirm</span></span>
<span data-ttu-id="a334d-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a334d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a334d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a334d-146">-WhatIf</span></span>
<span data-ttu-id="a334d-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a334d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a334d-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a334d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a334d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a334d-149">CommonParameters</span></span>
<span data-ttu-id="a334d-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a334d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a334d-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a334d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a334d-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="a334d-152">INPUTS</span></span>

### <span data-ttu-id="a334d-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a334d-153">None</span></span>
## <span data-ttu-id="a334d-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="a334d-154">OUTPUTS</span></span>

### <span data-ttu-id="a334d-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="a334d-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="a334d-156">Notas</span><span class="sxs-lookup"><span data-stu-id="a334d-156">NOTES</span></span>

## <span data-ttu-id="a334d-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a334d-157">RELATED LINKS</span></span>
