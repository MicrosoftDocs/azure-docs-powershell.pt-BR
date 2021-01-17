---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429750"
---
# <span data-ttu-id="490e7-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="490e7-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="490e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="490e7-102">SYNOPSIS</span></span>
<span data-ttu-id="490e7-103">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="490e7-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="490e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="490e7-104">SYNTAX</span></span>

### <span data-ttu-id="490e7-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="490e7-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="490e7-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="490e7-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="490e7-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="490e7-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="490e7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="490e7-108">DESCRIPTION</span></span>
<span data-ttu-id="490e7-109">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="490e7-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="490e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="490e7-110">EXAMPLES</span></span>

### <span data-ttu-id="490e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="490e7-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="490e7-112">Cria uma definição de registro pelos valores roleDefinitionId e dirigeid fornecidos diretamente.</span><span class="sxs-lookup"><span data-stu-id="490e7-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="490e7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="490e7-113">Example 2</span></span>
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

<span data-ttu-id="490e7-114">Cria ou atualiza uma definição de registro com detalhes de autorização.</span><span class="sxs-lookup"><span data-stu-id="490e7-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="490e7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="490e7-115">Example 3</span></span>
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

<span data-ttu-id="490e7-116">Atualiza uma definição de registro com detalhes de autorização e o nome da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="490e7-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="490e7-117">OS</span><span class="sxs-lookup"><span data-stu-id="490e7-117">PARAMETERS</span></span>

### <span data-ttu-id="490e7-118">-Authorization</span><span class="sxs-lookup"><span data-stu-id="490e7-118">-Authorization</span></span>
<span data-ttu-id="490e7-119">Lista de mapeamento de autorização com entidade de segurança-roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="490e7-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

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

### <span data-ttu-id="490e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490e7-120">-DefaultProfile</span></span>
<span data-ttu-id="490e7-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="490e7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="490e7-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="490e7-122">-Description</span></span>
<span data-ttu-id="490e7-123">A descrição da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="490e7-123">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="490e7-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="490e7-124">-DisplayName</span></span>
<span data-ttu-id="490e7-125">O nome de exibição da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="490e7-125">The display name of the Registration Definition.</span></span>

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

### <span data-ttu-id="490e7-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="490e7-126">-ManagedByTenantId</span></span>
<span data-ttu-id="490e7-127">O identificador de locatário ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="490e7-127">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="490e7-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="490e7-128">-Name</span></span>
<span data-ttu-id="490e7-129">O nome exclusivo da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="490e7-129">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="490e7-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="490e7-130">-PlanName</span></span>
<span data-ttu-id="490e7-131">O nome do plano.</span><span class="sxs-lookup"><span data-stu-id="490e7-131">The name of the plan.</span></span>

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

### <span data-ttu-id="490e7-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="490e7-132">-PlanProduct</span></span>
<span data-ttu-id="490e7-133">O nome do produto.</span><span class="sxs-lookup"><span data-stu-id="490e7-133">The name of the Product.</span></span>

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

### <span data-ttu-id="490e7-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="490e7-134">-PlanPublisher</span></span>
<span data-ttu-id="490e7-135">O nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="490e7-135">The name of the Publisher.</span></span>

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

### <span data-ttu-id="490e7-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="490e7-136">-PlanVersion</span></span>
<span data-ttu-id="490e7-137">O número da versão do plano.</span><span class="sxs-lookup"><span data-stu-id="490e7-137">The version number of the plan.</span></span>

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

### <span data-ttu-id="490e7-138">-Entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="490e7-138">-PrincipalId</span></span>
<span data-ttu-id="490e7-139">O identificador principal do ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="490e7-139">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="490e7-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="490e7-140">-RoleDefinitionId</span></span>
<span data-ttu-id="490e7-141">O identificador de definição de função para conceder permissões ao identificador principal.</span><span class="sxs-lookup"><span data-stu-id="490e7-141">The role definition identifier to grant permissions to principal identifier.</span></span>

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

### <span data-ttu-id="490e7-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="490e7-142">-AsJob</span></span>
<span data-ttu-id="490e7-143">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="490e7-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="490e7-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="490e7-144">-Confirm</span></span>
<span data-ttu-id="490e7-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="490e7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="490e7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="490e7-146">-WhatIf</span></span>
<span data-ttu-id="490e7-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="490e7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="490e7-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="490e7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="490e7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490e7-149">CommonParameters</span></span>
<span data-ttu-id="490e7-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490e7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490e7-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="490e7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490e7-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="490e7-152">INPUTS</span></span>

### <span data-ttu-id="490e7-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="490e7-153">None</span></span>
## <span data-ttu-id="490e7-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="490e7-154">OUTPUTS</span></span>

### <span data-ttu-id="490e7-155">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="490e7-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="490e7-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="490e7-156">NOTES</span></span>

## <span data-ttu-id="490e7-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="490e7-157">RELATED LINKS</span></span>
