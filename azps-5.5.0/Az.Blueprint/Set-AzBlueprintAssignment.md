---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116940"
---
# <span data-ttu-id="811a1-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="811a1-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="811a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="811a1-102">SYNOPSIS</span></span>
<span data-ttu-id="811a1-103">Atualize uma atribuição de planta existente.</span><span class="sxs-lookup"><span data-stu-id="811a1-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="811a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="811a1-104">SYNTAX</span></span>

### <span data-ttu-id="811a1-105">UpdateBlueprintAssignment (Padrão)</span><span class="sxs-lookup"><span data-stu-id="811a1-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="811a1-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="811a1-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="811a1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="811a1-107">DESCRIPTION</span></span>
<span data-ttu-id="811a1-108">Atualize uma atribuição de planta existente.</span><span class="sxs-lookup"><span data-stu-id="811a1-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="811a1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="811a1-109">EXAMPLES</span></span>

### <span data-ttu-id="811a1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="811a1-110">Example 1</span></span>
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

<span data-ttu-id="811a1-111">Atualize uma atribuição de diagrama existente da definição de diagrama dentro da `$blueprintObject` assinatura especificada, atualizando os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="811a1-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="811a1-112">Usa a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="811a1-112">Uses system-assigned identity.</span></span> <span data-ttu-id="811a1-113">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="811a1-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="811a1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="811a1-114">Example 2</span></span>
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

<span data-ttu-id="811a1-115">Atualize uma tarefa de diagrama existente por meio de um arquivo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="811a1-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="811a1-116">O formato do arquivo de atribuição pode ser encontrado nas amostras de solicitação/resposta em: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="811a1-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="811a1-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="811a1-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="811a1-118">Atualize uma atribuição de plano de trabalho existente da definição de diagrama visando a assinatura especificada dentro do `$blueprintObject` grupo de gerenciamento especificado usando o parâmetro definido.</span><span class="sxs-lookup"><span data-stu-id="811a1-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="811a1-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="811a1-119">PARAMETERS</span></span>

### <span data-ttu-id="811a1-120">-Arquivo de Atribuição</span><span class="sxs-lookup"><span data-stu-id="811a1-120">-AssignmentFile</span></span>
<span data-ttu-id="811a1-121">Local do arquivo de atribuição no formato JSON no disco.</span><span class="sxs-lookup"><span data-stu-id="811a1-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="811a1-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="811a1-122">-Blueprint</span></span>
<span data-ttu-id="811a1-123">Objeto de planta.</span><span class="sxs-lookup"><span data-stu-id="811a1-123">Blueprint object.</span></span>

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

### <span data-ttu-id="811a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="811a1-124">-DefaultProfile</span></span>
<span data-ttu-id="811a1-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="811a1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="811a1-126">-Local</span><span class="sxs-lookup"><span data-stu-id="811a1-126">-Location</span></span>
<span data-ttu-id="811a1-127">Região em que a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="811a1-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="811a1-128">Saiba mais no aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="811a1-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="811a1-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="811a1-129">-Lock</span></span>
<span data-ttu-id="811a1-130">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="811a1-130">Lock resources.</span></span>
<span data-ttu-id="811a1-131">Saiba mais no aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="811a1-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="811a1-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="811a1-132">-ManagementGroupId</span></span>
<span data-ttu-id="811a1-133">A ID do grupo de gerenciamento onde as atribuições do plano de trabalho serão salvas.</span><span class="sxs-lookup"><span data-stu-id="811a1-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="811a1-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="811a1-134">-Name</span></span>
<span data-ttu-id="811a1-135">Nome da tarefa de diagrama.</span><span class="sxs-lookup"><span data-stu-id="811a1-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="811a1-136">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="811a1-136">-Parameter</span></span>
<span data-ttu-id="811a1-137">Parâmetro Artefato.</span><span class="sxs-lookup"><span data-stu-id="811a1-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="811a1-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="811a1-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="811a1-139">Hashtable of parameters to pass to the resource group artifact.</span><span class="sxs-lookup"><span data-stu-id="811a1-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="811a1-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="811a1-140">-SecureStringParameter</span></span>
<span data-ttu-id="811a1-141">Parâmetro de cadeia de caracteres seguro para a ID, o nome e a versão do recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="811a1-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="811a1-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="811a1-142">-SubscriptionId</span></span>
<span data-ttu-id="811a1-143">SubscriptionId para atribuir o Diagrama.</span><span class="sxs-lookup"><span data-stu-id="811a1-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="811a1-144">Pode ser uma lista delimitada por vírgulas de cadeias de caracteres subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="811a1-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="811a1-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="811a1-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="811a1-146">Identidade atribuída pelo sistema (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="811a1-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="811a1-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="811a1-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="811a1-148">Identidade atribuída pelo usuário (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="811a1-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="811a1-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="811a1-149">-Confirm</span></span>
<span data-ttu-id="811a1-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811a1-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811a1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811a1-151">-WhatIf</span></span>
<span data-ttu-id="811a1-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="811a1-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="811a1-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="811a1-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811a1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811a1-154">CommonParameters</span></span>
<span data-ttu-id="811a1-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="811a1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811a1-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="811a1-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811a1-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="811a1-157">INPUTS</span></span>

### <span data-ttu-id="811a1-158">System.String</span><span class="sxs-lookup"><span data-stu-id="811a1-158">System.String</span></span>

### <span data-ttu-id="811a1-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="811a1-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="811a1-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="811a1-160">System.String[]</span></span>

### <span data-ttu-id="811a1-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="811a1-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="811a1-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="811a1-162">OUTPUTS</span></span>

### <span data-ttu-id="811a1-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="811a1-163">System.Object</span></span>
## <span data-ttu-id="811a1-164">Notas</span><span class="sxs-lookup"><span data-stu-id="811a1-164">NOTES</span></span>

## <span data-ttu-id="811a1-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="811a1-165">RELATED LINKS</span></span>
