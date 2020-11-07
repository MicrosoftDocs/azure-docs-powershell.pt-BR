---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771289"
---
# <span data-ttu-id="a7a18-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a7a18-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="a7a18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7a18-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a18-103">Atualize uma atribuição Blueprint existente.</span><span class="sxs-lookup"><span data-stu-id="a7a18-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a7a18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7a18-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a18-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7a18-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a18-106">Atualize uma atribuição Blueprint existente.</span><span class="sxs-lookup"><span data-stu-id="a7a18-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a7a18-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7a18-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a18-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7a18-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="a7a18-109">Atualize uma atribuição Blueprint existente da definição Blueprint `$blueprintObject` dentro da assinatura especificada, atualizando os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a7a18-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="a7a18-110">Usa a identidade atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a7a18-110">Uses system-assigned identity.</span></span> <span data-ttu-id="a7a18-111">O local define a região para a criação da identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="a7a18-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="a7a18-112">OS</span><span class="sxs-lookup"><span data-stu-id="a7a18-112">PARAMETERS</span></span>

### <span data-ttu-id="a7a18-113">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="a7a18-113">-Blueprint</span></span>
<span data-ttu-id="a7a18-114">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a7a18-114">Blueprint object.</span></span>

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

### <span data-ttu-id="a7a18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a18-115">-DefaultProfile</span></span>
<span data-ttu-id="a7a18-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7a18-117">-Local</span><span class="sxs-lookup"><span data-stu-id="a7a18-117">-Location</span></span>
<span data-ttu-id="a7a18-118">Região para a qual a identidade gerenciada deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a7a18-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="a7a18-119">Saiba mais em aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="a7a18-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="a7a18-120">-Lock</span><span class="sxs-lookup"><span data-stu-id="a7a18-120">-Lock</span></span>
<span data-ttu-id="a7a18-121">Bloquear recursos.</span><span class="sxs-lookup"><span data-stu-id="a7a18-121">Lock resources.</span></span>
<span data-ttu-id="a7a18-122">Saiba mais em aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="a7a18-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="a7a18-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7a18-123">-Name</span></span>
<span data-ttu-id="a7a18-124">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a7a18-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="a7a18-125">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7a18-125">-Parameter</span></span>
<span data-ttu-id="a7a18-126">Parâmetro artefato.</span><span class="sxs-lookup"><span data-stu-id="a7a18-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="a7a18-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="a7a18-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="a7a18-128">{{Fill ResourceGroupParameter descrição}}</span><span class="sxs-lookup"><span data-stu-id="a7a18-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="a7a18-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="a7a18-129">-SecureStringParameter</span></span>
<span data-ttu-id="a7a18-130">Parâmetro de cadeia de caracteres seguro para ID do recurso de keyvault, nome e versão.</span><span class="sxs-lookup"><span data-stu-id="a7a18-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="a7a18-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7a18-131">-SubscriptionId</span></span>
<span data-ttu-id="a7a18-132">SubscriptionId para atribuir o plano gráfico.</span><span class="sxs-lookup"><span data-stu-id="a7a18-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="a7a18-133">Pode ser uma lista delimitada por vírgula de cadeias de caracteres SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="a7a18-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="a7a18-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a7a18-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a7a18-135">Identidade atribuída ao sistema (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="a7a18-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a7a18-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a7a18-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="a7a18-137">Identidade atribuída ao usuário (MSI) para implantar os artefatos.</span><span class="sxs-lookup"><span data-stu-id="a7a18-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a7a18-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7a18-138">-Confirm</span></span>
<span data-ttu-id="a7a18-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a18-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a18-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a18-140">-WhatIf</span></span>
<span data-ttu-id="a7a18-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7a18-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a18-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7a18-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a18-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a18-143">CommonParameters</span></span>
<span data-ttu-id="a7a18-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a18-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a18-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a18-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a18-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7a18-146">INPUTS</span></span>

### <span data-ttu-id="a7a18-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a18-147">System.String</span></span>

### <span data-ttu-id="a7a18-148">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a7a18-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a7a18-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="a7a18-149">System.String[]</span></span>

### <span data-ttu-id="a7a18-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a7a18-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a7a18-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7a18-151">OUTPUTS</span></span>

### <span data-ttu-id="a7a18-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="a7a18-152">System.Object</span></span>
## <span data-ttu-id="a7a18-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7a18-153">NOTES</span></span>

## <span data-ttu-id="a7a18-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7a18-154">RELATED LINKS</span></span>
