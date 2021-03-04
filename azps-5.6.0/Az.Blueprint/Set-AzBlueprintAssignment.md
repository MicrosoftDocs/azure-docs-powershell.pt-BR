---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 0e5c562d5b536e95d40bdbc1c08b2d778574fd41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891885"
---
# <span data-ttu-id="57661-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="57661-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="57661-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57661-102">SYNOPSIS</span></span>
<span data-ttu-id="57661-103">Atualize uma atribuição de projeto existente.</span><span class="sxs-lookup"><span data-stu-id="57661-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="57661-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57661-104">SYNTAX</span></span>

### <span data-ttu-id="57661-105">UpdateBlueprintAssignment (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57661-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57661-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="57661-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57661-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57661-107">DESCRIPTION</span></span>
<span data-ttu-id="57661-108">Atualize uma atribuição de projeto existente.</span><span class="sxs-lookup"><span data-stu-id="57661-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="57661-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57661-109">EXAMPLES</span></span>

### <span data-ttu-id="57661-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="57661-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="57661-111">Atualize uma atribuição de projeto existente da definição de projeto dentro `$blueprintObject` da assinatura especificada, atualizando os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="57661-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="57661-112">Usa a identidade atribuída ao sistema.</span><span class="sxs-lookup"><span data-stu-id="57661-112">Uses system-assigned identity.</span></span> <span data-ttu-id="57661-113">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="57661-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="57661-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="57661-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="57661-115">Atualize uma atribuição de projeto existente por meio de um arquivo de atribuição.</span><span class="sxs-lookup"><span data-stu-id="57661-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="57661-116">O formato do arquivo de atribuição pode ser encontrado nos exemplos de solicitação/resposta em: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="57661-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="57661-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="57661-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="57661-118">Atualize uma atribuição de projeto existente da definição de projeto direcionando a assinatura especificada dentro do grupo de `$blueprintObject` gerenciamento especificado usando o parâmetro definido.</span><span class="sxs-lookup"><span data-stu-id="57661-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="57661-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57661-119">PARAMETERS</span></span>

### <span data-ttu-id="57661-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="57661-120">-AssignmentFile</span></span>
<span data-ttu-id="57661-121">Local do arquivo de atribuição no formato JSON no disco.</span><span class="sxs-lookup"><span data-stu-id="57661-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57661-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="57661-122">-Blueprint</span></span>
<span data-ttu-id="57661-123">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="57661-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57661-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57661-124">-DefaultProfile</span></span>
<span data-ttu-id="57661-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57661-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57661-126">-Location</span><span class="sxs-lookup"><span data-stu-id="57661-126">-Location</span></span>
<span data-ttu-id="57661-127">Região em que a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="57661-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="57661-128">Saiba mais em aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="57661-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57661-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="57661-129">-Lock</span></span>
<span data-ttu-id="57661-130">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="57661-130">Lock resources.</span></span>
<span data-ttu-id="57661-131">Saiba mais em aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="57661-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57661-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="57661-132">-ManagementGroupId</span></span>
<span data-ttu-id="57661-133">A ID do grupo de gerenciamento em que as atribuições de blueprint serão salvas.</span><span class="sxs-lookup"><span data-stu-id="57661-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57661-134">-Name</span><span class="sxs-lookup"><span data-stu-id="57661-134">-Name</span></span>
<span data-ttu-id="57661-135">Nome da atribuição de projeto.</span><span class="sxs-lookup"><span data-stu-id="57661-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57661-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="57661-136">-Parameter</span></span>
<span data-ttu-id="57661-137">Parâmetro Artifact.</span><span class="sxs-lookup"><span data-stu-id="57661-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57661-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="57661-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="57661-139">Hashtable de parâmetros para passar para o artefato do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57661-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57661-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="57661-140">-SecureStringParameter</span></span>
<span data-ttu-id="57661-141">Parâmetro de cadeia de caracteres seguro para id de recurso KeyVault, nome e versão.</span><span class="sxs-lookup"><span data-stu-id="57661-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57661-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57661-142">-SubscriptionId</span></span>
<span data-ttu-id="57661-143">SubscriptionId para atribuir o Blueprint.</span><span class="sxs-lookup"><span data-stu-id="57661-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="57661-144">Pode ser uma lista delimitada por vírgulas de cadeias de caracteres subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="57661-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57661-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="57661-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="57661-146">MSI (identidade atribuída ao sistema) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="57661-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57661-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="57661-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="57661-148">MSI (identidade atribuída pelo usuário) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="57661-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57661-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57661-149">-Confirm</span></span>
<span data-ttu-id="57661-150">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57661-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57661-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57661-151">-WhatIf</span></span>
<span data-ttu-id="57661-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57661-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57661-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57661-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57661-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57661-154">CommonParameters</span></span>
<span data-ttu-id="57661-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57661-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57661-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57661-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57661-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57661-157">INPUTS</span></span>

### <span data-ttu-id="57661-158">System.String</span><span class="sxs-lookup"><span data-stu-id="57661-158">System.String</span></span>

### <span data-ttu-id="57661-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="57661-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="57661-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="57661-160">System.String[]</span></span>

### <span data-ttu-id="57661-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="57661-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57661-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57661-162">OUTPUTS</span></span>

### <span data-ttu-id="57661-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="57661-163">System.Object</span></span>
## <span data-ttu-id="57661-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="57661-164">NOTES</span></span>

## <span data-ttu-id="57661-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57661-165">RELATED LINKS</span></span>
