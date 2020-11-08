---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116101"
---
# <span data-ttu-id="38859-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="38859-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="38859-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38859-102">SYNOPSIS</span></span>
<span data-ttu-id="38859-103">Atribua uma definição Blueprint a uma assinatura ou a um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="38859-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="38859-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38859-104">SYNTAX</span></span>

### <span data-ttu-id="38859-105">CreateBlueprintAssignment (padrão)</span><span class="sxs-lookup"><span data-stu-id="38859-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38859-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="38859-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38859-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38859-107">DESCRIPTION</span></span>
<span data-ttu-id="38859-108">Atribuir uma definição Blueprint a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="38859-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="38859-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38859-109">EXAMPLES</span></span>

### <span data-ttu-id="38859-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38859-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="38859-111">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o parâmetro definido e o dicionário do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38859-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="38859-112">Usa a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="38859-112">Uses system-assigned identity.</span></span> <span data-ttu-id="38859-113">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="38859-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="38859-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="38859-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="38859-115">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o dicionário definido e o dicionário do grupo de recursos e Configurando o bloqueio de recursos para os próprios **recursos**.</span><span class="sxs-lookup"><span data-stu-id="38859-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="38859-116">O padrão é usar a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="38859-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="38859-117">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="38859-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="38859-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="38859-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="38859-119">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o parâmetro definido e o dicionário do grupo de recursos usando a ID de identidade atribuída pelo usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="38859-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="38859-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="38859-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="38859-121">Crie uma atribuição Blueprint por meio de um arquivo de atribuição.</span><span class="sxs-lookup"><span data-stu-id="38859-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="38859-122">O formato do arquivo de atribuição pode ser encontrado nos exemplos de solicitação/resposta em: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="38859-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="38859-123">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="38859-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="38859-124">Crie uma nova atribuição Blueprint da definição Blueprint que `$blueprintObject` direciona a assinatura especificada dentro do grupo de gerenciamento especificado usando o parâmetro definido.</span><span class="sxs-lookup"><span data-stu-id="38859-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="38859-125">OS</span><span class="sxs-lookup"><span data-stu-id="38859-125">PARAMETERS</span></span>

### <span data-ttu-id="38859-126">-Assignmentfile</span><span class="sxs-lookup"><span data-stu-id="38859-126">-AssignmentFile</span></span>
<span data-ttu-id="38859-127">Local do arquivo de atribuição no formato JSON no disco.</span><span class="sxs-lookup"><span data-stu-id="38859-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38859-128">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="38859-128">-Blueprint</span></span>
<span data-ttu-id="38859-129">Objeto de definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="38859-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38859-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38859-130">-DefaultProfile</span></span>
<span data-ttu-id="38859-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38859-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38859-132">-Local</span><span class="sxs-lookup"><span data-stu-id="38859-132">-Location</span></span>
<span data-ttu-id="38859-133">Região para a qual a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="38859-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="38859-134">Saiba mais em aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="38859-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38859-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="38859-135">-Lock</span></span>
<span data-ttu-id="38859-136">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="38859-136">Lock resources.</span></span>
<span data-ttu-id="38859-137">Saiba mais em aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="38859-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38859-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="38859-138">-ManagementGroupId</span></span>
<span data-ttu-id="38859-139">A ID do grupo de gerenciamento em que a (s) atribuição (ções) de gráfico será salva.</span><span class="sxs-lookup"><span data-stu-id="38859-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38859-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="38859-140">-Name</span></span>
<span data-ttu-id="38859-141">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="38859-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38859-142">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="38859-142">-Parameter</span></span>
<span data-ttu-id="38859-143">Parâmetros de artefato.</span><span class="sxs-lookup"><span data-stu-id="38859-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38859-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="38859-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="38859-145">Hashtable dos parâmetros a serem passados para o artefato do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38859-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38859-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="38859-146">-SecureStringParameter</span></span>
<span data-ttu-id="38859-147">Parâmetro de cadeia de caracteres seguro para ID do recurso de keyvault, nome e versão.</span><span class="sxs-lookup"><span data-stu-id="38859-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38859-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38859-148">-SubscriptionId</span></span>
<span data-ttu-id="38859-149">ID da assinatura para atribuir a definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="38859-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="38859-150">Pode ser uma lista delimitada por vírgula de cadeias de caracteres SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="38859-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38859-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="38859-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="38859-152">Identidade atribuída ao sistema (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="38859-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38859-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="38859-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="38859-154">Identidade atribuída ao usuário (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="38859-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38859-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38859-155">-Confirm</span></span>
<span data-ttu-id="38859-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38859-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38859-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38859-157">-WhatIf</span></span>
<span data-ttu-id="38859-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38859-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38859-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38859-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38859-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38859-160">CommonParameters</span></span>
<span data-ttu-id="38859-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38859-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38859-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38859-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38859-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38859-163">INPUTS</span></span>

### <span data-ttu-id="38859-164">System. String</span><span class="sxs-lookup"><span data-stu-id="38859-164">System.String</span></span>

### <span data-ttu-id="38859-165">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="38859-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="38859-166">System. String []</span><span class="sxs-lookup"><span data-stu-id="38859-166">System.String[]</span></span>

### <span data-ttu-id="38859-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="38859-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="38859-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38859-168">OUTPUTS</span></span>

### <span data-ttu-id="38859-169">System. Object</span><span class="sxs-lookup"><span data-stu-id="38859-169">System.Object</span></span>
## <span data-ttu-id="38859-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38859-170">NOTES</span></span>

## <span data-ttu-id="38859-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38859-171">RELATED LINKS</span></span>
