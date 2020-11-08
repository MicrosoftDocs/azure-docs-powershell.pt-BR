---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125164"
---
# <span data-ttu-id="26afb-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="26afb-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="26afb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26afb-102">SYNOPSIS</span></span>
<span data-ttu-id="26afb-103">Atualize uma atribuição Blueprint existente.</span><span class="sxs-lookup"><span data-stu-id="26afb-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="26afb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26afb-104">SYNTAX</span></span>

### <span data-ttu-id="26afb-105">UpdateBlueprintAssignment (padrão)</span><span class="sxs-lookup"><span data-stu-id="26afb-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26afb-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="26afb-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26afb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26afb-107">DESCRIPTION</span></span>
<span data-ttu-id="26afb-108">Atualize uma atribuição Blueprint existente.</span><span class="sxs-lookup"><span data-stu-id="26afb-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="26afb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26afb-109">EXAMPLES</span></span>

### <span data-ttu-id="26afb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="26afb-110">Example 1</span></span>
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

<span data-ttu-id="26afb-111">Atualize uma atribuição Blueprint existente da definição Blueprint `$blueprintObject` dentro da assinatura especificada, atualizando os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="26afb-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="26afb-112">Usa a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="26afb-112">Uses system-assigned identity.</span></span> <span data-ttu-id="26afb-113">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="26afb-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="26afb-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="26afb-114">Example 2</span></span>
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

<span data-ttu-id="26afb-115">Atualize uma atribuição Blueprint existente por meio de um arquivo de atribuição.</span><span class="sxs-lookup"><span data-stu-id="26afb-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="26afb-116">O formato do arquivo de atribuição pode ser encontrado nos exemplos de solicitação/resposta em: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="26afb-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="26afb-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="26afb-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="26afb-118">Atualize uma atribuição Blueprint existente da definição Blueprint que `$blueprintObject` direciona a assinatura especificada dentro do grupo de gerenciamento especificado usando o parâmetro definido.</span><span class="sxs-lookup"><span data-stu-id="26afb-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="26afb-119">OS</span><span class="sxs-lookup"><span data-stu-id="26afb-119">PARAMETERS</span></span>

### <span data-ttu-id="26afb-120">-Assignmentfile</span><span class="sxs-lookup"><span data-stu-id="26afb-120">-AssignmentFile</span></span>
<span data-ttu-id="26afb-121">Local do arquivo de atribuição no formato JSON no disco.</span><span class="sxs-lookup"><span data-stu-id="26afb-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="26afb-122">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="26afb-122">-Blueprint</span></span>
<span data-ttu-id="26afb-123">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="26afb-123">Blueprint object.</span></span>

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

### <span data-ttu-id="26afb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26afb-124">-DefaultProfile</span></span>
<span data-ttu-id="26afb-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26afb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26afb-126">-Local</span><span class="sxs-lookup"><span data-stu-id="26afb-126">-Location</span></span>
<span data-ttu-id="26afb-127">Região para a qual a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="26afb-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="26afb-128">Saiba mais em aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="26afb-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="26afb-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="26afb-129">-Lock</span></span>
<span data-ttu-id="26afb-130">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="26afb-130">Lock resources.</span></span>
<span data-ttu-id="26afb-131">Saiba mais em aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="26afb-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="26afb-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="26afb-132">-ManagementGroupId</span></span>
<span data-ttu-id="26afb-133">A ID do grupo de gerenciamento em que a (s) atribuição (ções) de gráfico será salva.</span><span class="sxs-lookup"><span data-stu-id="26afb-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="26afb-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="26afb-134">-Name</span></span>
<span data-ttu-id="26afb-135">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="26afb-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="26afb-136">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="26afb-136">-Parameter</span></span>
<span data-ttu-id="26afb-137">Parâmetro artefato.</span><span class="sxs-lookup"><span data-stu-id="26afb-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="26afb-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="26afb-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="26afb-139">Hashtable dos parâmetros a serem passados para o artefato do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26afb-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="26afb-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="26afb-140">-SecureStringParameter</span></span>
<span data-ttu-id="26afb-141">Parâmetro de cadeia de caracteres seguro para ID do recurso de keyvault, nome e versão.</span><span class="sxs-lookup"><span data-stu-id="26afb-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="26afb-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26afb-142">-SubscriptionId</span></span>
<span data-ttu-id="26afb-143">SubscriptionId para atribuir o plano gráfico.</span><span class="sxs-lookup"><span data-stu-id="26afb-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="26afb-144">Pode ser uma lista delimitada por vírgula de cadeias de caracteres SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="26afb-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="26afb-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="26afb-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="26afb-146">Identidade atribuída ao sistema (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="26afb-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="26afb-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="26afb-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="26afb-148">Identidade atribuída ao usuário (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="26afb-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="26afb-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26afb-149">-Confirm</span></span>
<span data-ttu-id="26afb-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26afb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26afb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26afb-151">-WhatIf</span></span>
<span data-ttu-id="26afb-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26afb-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26afb-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26afb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26afb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26afb-154">CommonParameters</span></span>
<span data-ttu-id="26afb-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26afb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26afb-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26afb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26afb-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26afb-157">INPUTS</span></span>

### <span data-ttu-id="26afb-158">System. String</span><span class="sxs-lookup"><span data-stu-id="26afb-158">System.String</span></span>

### <span data-ttu-id="26afb-159">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="26afb-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="26afb-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="26afb-160">System.String[]</span></span>

### <span data-ttu-id="26afb-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26afb-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26afb-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26afb-162">OUTPUTS</span></span>

### <span data-ttu-id="26afb-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="26afb-163">System.Object</span></span>
## <span data-ttu-id="26afb-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26afb-164">NOTES</span></span>

## <span data-ttu-id="26afb-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26afb-165">RELATED LINKS</span></span>
