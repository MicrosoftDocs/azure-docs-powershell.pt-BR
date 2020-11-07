---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 418bb8a9ba8362e799d619705eccdc60e5418fc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940986"
---
# <span data-ttu-id="2a53c-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="2a53c-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="2a53c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a53c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a53c-103">Atualize uma atribuição Blueprint existente.</span><span class="sxs-lookup"><span data-stu-id="2a53c-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2a53c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a53c-104">SYNTAX</span></span>

### <span data-ttu-id="2a53c-105">UpdateBlueprintAssignment (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a53c-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a53c-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="2a53c-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a53c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a53c-107">DESCRIPTION</span></span>
<span data-ttu-id="2a53c-108">Atualize uma atribuição Blueprint existente.</span><span class="sxs-lookup"><span data-stu-id="2a53c-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2a53c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a53c-109">EXAMPLES</span></span>

### <span data-ttu-id="2a53c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a53c-110">Example 1</span></span>
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

<span data-ttu-id="2a53c-111">Atualize uma atribuição Blueprint existente da definição Blueprint `$blueprintObject` dentro da assinatura especificada, atualizando os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2a53c-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="2a53c-112">Usa a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="2a53c-112">Uses system-assigned identity.</span></span> <span data-ttu-id="2a53c-113">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="2a53c-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="2a53c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2a53c-114">Example 2</span></span>
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

<span data-ttu-id="2a53c-115">Atualize uma atribuição Blueprint existente por meio de um arquivo de atribuição.</span><span class="sxs-lookup"><span data-stu-id="2a53c-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="2a53c-116">O formato do arquivo de atribuição pode ser encontrado nos exemplos de solicitação/resposta em: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="2a53c-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="2a53c-117">OS</span><span class="sxs-lookup"><span data-stu-id="2a53c-117">PARAMETERS</span></span>

### <span data-ttu-id="2a53c-118">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="2a53c-118">-Blueprint</span></span>
<span data-ttu-id="2a53c-119">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="2a53c-119">Blueprint object.</span></span>

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

### <span data-ttu-id="2a53c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a53c-120">-DefaultProfile</span></span>
<span data-ttu-id="2a53c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a53c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a53c-122">-Local</span><span class="sxs-lookup"><span data-stu-id="2a53c-122">-Location</span></span>
<span data-ttu-id="2a53c-123">Região para a qual a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2a53c-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="2a53c-124">Saiba mais em aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="2a53c-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="2a53c-125">-Lock</span><span class="sxs-lookup"><span data-stu-id="2a53c-125">-Lock</span></span>
<span data-ttu-id="2a53c-126">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="2a53c-126">Lock resources.</span></span>
<span data-ttu-id="2a53c-127">Saiba mais em aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="2a53c-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="2a53c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a53c-128">-Name</span></span>
<span data-ttu-id="2a53c-129">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="2a53c-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="2a53c-130">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a53c-130">-Parameter</span></span>
<span data-ttu-id="2a53c-131">Parâmetro artefato.</span><span class="sxs-lookup"><span data-stu-id="2a53c-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="2a53c-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="2a53c-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="2a53c-133">{{Fill ResourceGroupParameter descrição}}</span><span class="sxs-lookup"><span data-stu-id="2a53c-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="2a53c-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="2a53c-134">-SecureStringParameter</span></span>
<span data-ttu-id="2a53c-135">Parâmetro de cadeia de caracteres seguro para ID do recurso de keyvault, nome e versão.</span><span class="sxs-lookup"><span data-stu-id="2a53c-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="2a53c-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a53c-136">-SubscriptionId</span></span>
<span data-ttu-id="2a53c-137">SubscriptionId para atribuir o plano gráfico.</span><span class="sxs-lookup"><span data-stu-id="2a53c-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="2a53c-138">Pode ser uma lista delimitada por vírgula de cadeias de caracteres SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="2a53c-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="2a53c-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2a53c-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="2a53c-140">Identidade atribuída ao sistema (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="2a53c-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="2a53c-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2a53c-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="2a53c-142">Identidade atribuída ao usuário (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="2a53c-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a53c-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a53c-143">-Confirm</span></span>
<span data-ttu-id="2a53c-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a53c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a53c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a53c-145">-WhatIf</span></span>
<span data-ttu-id="2a53c-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a53c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a53c-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a53c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a53c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a53c-148">CommonParameters</span></span>
<span data-ttu-id="2a53c-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a53c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a53c-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a53c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a53c-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a53c-151">INPUTS</span></span>

### <span data-ttu-id="2a53c-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2a53c-152">System.String</span></span>

### <span data-ttu-id="2a53c-153">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="2a53c-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2a53c-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="2a53c-154">System.String[]</span></span>

### <span data-ttu-id="2a53c-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a53c-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2a53c-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a53c-156">OUTPUTS</span></span>

### <span data-ttu-id="2a53c-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="2a53c-157">System.Object</span></span>
## <span data-ttu-id="2a53c-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a53c-158">NOTES</span></span>

## <span data-ttu-id="2a53c-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a53c-159">RELATED LINKS</span></span>
