---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 6adc5674674de903b30993b09d5bb680f8569398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597637"
---
# <span data-ttu-id="75382-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="75382-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="75382-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75382-102">SYNOPSIS</span></span>
<span data-ttu-id="75382-103">Atribuir uma definição Blueprint a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="75382-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="75382-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75382-104">SYNTAX</span></span>

### <span data-ttu-id="75382-105">CreateBlueprintAssignment (padrão)</span><span class="sxs-lookup"><span data-stu-id="75382-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75382-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="75382-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75382-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75382-107">DESCRIPTION</span></span>
<span data-ttu-id="75382-108">Atribuir uma definição Blueprint a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="75382-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="75382-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75382-109">EXAMPLES</span></span>

### <span data-ttu-id="75382-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75382-110">Example 1</span></span>
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

<span data-ttu-id="75382-111">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o parâmetro definido e o dicionário do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75382-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="75382-112">Usa a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="75382-112">Uses system-assigned identity.</span></span> <span data-ttu-id="75382-113">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="75382-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="75382-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75382-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="75382-115">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o dicionário definido e o dicionário do grupo de recursos e Configurando o bloqueio de recursos para os próprios **recursos**.</span><span class="sxs-lookup"><span data-stu-id="75382-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="75382-116">O padrão é usar a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="75382-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="75382-117">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="75382-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="75382-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="75382-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="75382-119">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o parâmetro definido e o dicionário do grupo de recursos usando a ID de identidade atribuída pelo usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="75382-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="75382-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="75382-120">Example 4</span></span>
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

<span data-ttu-id="75382-121">Crie uma atribuição Blueprint por meio de um arquivo de atribuição.</span><span class="sxs-lookup"><span data-stu-id="75382-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="75382-122">O formato do arquivo de atribuição pode ser encontrado nos exemplos de solicitação/resposta em: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="75382-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="75382-123">OS</span><span class="sxs-lookup"><span data-stu-id="75382-123">PARAMETERS</span></span>

### <span data-ttu-id="75382-124">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="75382-124">-Blueprint</span></span>
<span data-ttu-id="75382-125">Objeto de definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="75382-125">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75382-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75382-126">-DefaultProfile</span></span>
<span data-ttu-id="75382-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75382-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75382-128">-Local</span><span class="sxs-lookup"><span data-stu-id="75382-128">-Location</span></span>
<span data-ttu-id="75382-129">Região para a qual a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="75382-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="75382-130">Saiba mais em aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="75382-130">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75382-131">-Lock</span><span class="sxs-lookup"><span data-stu-id="75382-131">-Lock</span></span>
<span data-ttu-id="75382-132">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="75382-132">Lock resources.</span></span>
<span data-ttu-id="75382-133">Saiba mais em aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="75382-133">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75382-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="75382-134">-Name</span></span>
<span data-ttu-id="75382-135">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="75382-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75382-136">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="75382-136">-Parameter</span></span>
<span data-ttu-id="75382-137">Parâmetros de artefato.</span><span class="sxs-lookup"><span data-stu-id="75382-137">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75382-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="75382-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="75382-139">{{Fill ResourceGroupParameter descrição}}</span><span class="sxs-lookup"><span data-stu-id="75382-139">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75382-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="75382-140">-SecureStringParameter</span></span>
<span data-ttu-id="75382-141">Parâmetro de cadeia de caracteres seguro para ID do recurso de keyvault, nome e versão.</span><span class="sxs-lookup"><span data-stu-id="75382-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75382-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75382-142">-SubscriptionId</span></span>
<span data-ttu-id="75382-143">ID da assinatura para atribuir a definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="75382-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="75382-144">Pode ser uma lista delimitada por vírgula de cadeias de caracteres SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="75382-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75382-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="75382-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="75382-146">Identidade atribuída ao sistema (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="75382-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="75382-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="75382-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="75382-148">Identidade atribuída ao usuário (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="75382-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="75382-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75382-149">-Confirm</span></span>
<span data-ttu-id="75382-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75382-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75382-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75382-151">-WhatIf</span></span>
<span data-ttu-id="75382-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75382-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75382-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75382-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75382-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75382-154">CommonParameters</span></span>
<span data-ttu-id="75382-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75382-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75382-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75382-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75382-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75382-157">INPUTS</span></span>

### <span data-ttu-id="75382-158">System. String</span><span class="sxs-lookup"><span data-stu-id="75382-158">System.String</span></span>

### <span data-ttu-id="75382-159">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="75382-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="75382-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="75382-160">System.String[]</span></span>

### <span data-ttu-id="75382-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="75382-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="75382-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75382-162">OUTPUTS</span></span>

### <span data-ttu-id="75382-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="75382-163">System.Object</span></span>
## <span data-ttu-id="75382-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75382-164">NOTES</span></span>

## <span data-ttu-id="75382-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75382-165">RELATED LINKS</span></span>
