---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771287"
---
# <span data-ttu-id="6753d-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="6753d-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="6753d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6753d-102">SYNOPSIS</span></span>
<span data-ttu-id="6753d-103">Atribuir uma definição Blueprint a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6753d-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="6753d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6753d-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6753d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6753d-105">DESCRIPTION</span></span>
<span data-ttu-id="6753d-106">Atribuir uma definição Blueprint a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6753d-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="6753d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6753d-107">EXAMPLES</span></span>

### <span data-ttu-id="6753d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6753d-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="6753d-109">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o parâmetro definido e o dicionário do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6753d-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="6753d-110">Usa a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6753d-110">Uses system-assigned identity.</span></span> <span data-ttu-id="6753d-111">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6753d-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="6753d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6753d-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="6753d-113">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o dicionário definido e o dicionário do grupo de recursos e Configurando o bloqueio de recursos para os próprios **recursos**.</span><span class="sxs-lookup"><span data-stu-id="6753d-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="6753d-114">O padrão é usar a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6753d-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="6753d-115">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6753d-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="6753d-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6753d-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="6753d-117">Crie uma nova atribuição Blueprint da definição Blueprint `$blueprintObject` dentro da assinatura especificada usando o parâmetro definido e o dicionário do grupo de recursos usando a ID de identidade atribuída pelo usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="6753d-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="6753d-118">OS</span><span class="sxs-lookup"><span data-stu-id="6753d-118">PARAMETERS</span></span>

### <span data-ttu-id="6753d-119">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="6753d-119">-Blueprint</span></span>
<span data-ttu-id="6753d-120">Objeto de definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6753d-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="6753d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6753d-121">-DefaultProfile</span></span>
<span data-ttu-id="6753d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6753d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6753d-123">-Local</span><span class="sxs-lookup"><span data-stu-id="6753d-123">-Location</span></span>
<span data-ttu-id="6753d-124">Região para a qual a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="6753d-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="6753d-125">Saiba mais em aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="6753d-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="6753d-126">-Lock</span><span class="sxs-lookup"><span data-stu-id="6753d-126">-Lock</span></span>
<span data-ttu-id="6753d-127">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="6753d-127">Lock resources.</span></span>
<span data-ttu-id="6753d-128">Saiba mais em aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="6753d-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="6753d-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="6753d-129">-Name</span></span>
<span data-ttu-id="6753d-130">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6753d-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="6753d-131">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6753d-131">-Parameter</span></span>
<span data-ttu-id="6753d-132">Parâmetros de artefato.</span><span class="sxs-lookup"><span data-stu-id="6753d-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="6753d-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="6753d-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="6753d-134">{{Fill ResourceGroupParameter descrição}}</span><span class="sxs-lookup"><span data-stu-id="6753d-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="6753d-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="6753d-135">-SecureStringParameter</span></span>
<span data-ttu-id="6753d-136">Parâmetro de cadeia de caracteres seguro para ID do recurso de keyvault, nome e versão.</span><span class="sxs-lookup"><span data-stu-id="6753d-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="6753d-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6753d-137">-SubscriptionId</span></span>
<span data-ttu-id="6753d-138">ID da assinatura para atribuir a definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6753d-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="6753d-139">Pode ser uma lista delimitada por vírgula de cadeias de caracteres SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="6753d-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="6753d-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6753d-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="6753d-141">Identidade atribuída ao sistema (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="6753d-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="6753d-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6753d-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="6753d-143">Identidade atribuída ao usuário (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="6753d-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="6753d-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6753d-144">-Confirm</span></span>
<span data-ttu-id="6753d-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6753d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6753d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6753d-146">-WhatIf</span></span>
<span data-ttu-id="6753d-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6753d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6753d-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6753d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6753d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6753d-149">CommonParameters</span></span>
<span data-ttu-id="6753d-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6753d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6753d-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6753d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6753d-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6753d-152">INPUTS</span></span>

### <span data-ttu-id="6753d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6753d-153">System.String</span></span>

### <span data-ttu-id="6753d-154">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="6753d-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="6753d-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="6753d-155">System.String[]</span></span>

### <span data-ttu-id="6753d-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6753d-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6753d-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6753d-157">OUTPUTS</span></span>

### <span data-ttu-id="6753d-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="6753d-158">System.Object</span></span>
## <span data-ttu-id="6753d-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6753d-159">NOTES</span></span>

## <span data-ttu-id="6753d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6753d-160">RELATED LINKS</span></span>
