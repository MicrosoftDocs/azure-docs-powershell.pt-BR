---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 9161b3c9c55c1014b64419a3644bf7ec80af8648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890265"
---
# <span data-ttu-id="06244-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="06244-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="06244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06244-102">SYNOPSIS</span></span>
<span data-ttu-id="06244-103">Obtém o histórico de status de conformidade da política de configuração de convidado para uma iniciativa do tipo "Configuração de Convidado" atribuída a uma VM.</span><span class="sxs-lookup"><span data-stu-id="06244-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="06244-104">Uma iniciativa é uma política do tipo de definição "Iniciativa".</span><span class="sxs-lookup"><span data-stu-id="06244-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="06244-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="06244-105">SYNTAX</span></span>

### <span data-ttu-id="06244-106">InitiativeNameScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="06244-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06244-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="06244-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06244-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="06244-108">DESCRIPTION</span></span>
<span data-ttu-id="06244-109">O Get-AzVMGuestPolicyStatusHistory cmdlet obtém o histórico de status de conformidade das políticas de configuração de convidados para uma iniciativa do tipo "Configuração de Convidado" atribuída a uma VM.</span><span class="sxs-lookup"><span data-stu-id="06244-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="06244-110">Uma iniciativa é uma política do tipo de definição "Iniciativa".</span><span class="sxs-lookup"><span data-stu-id="06244-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="06244-111">Use Get-AzVMGuestPolicyStatus cmdlet para obter detalhes de um único status de conformidade usando ReportId que pode ser encontrado na saída de Get-AzVMGuestPolicyStatusHistory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06244-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="06244-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06244-112">EXAMPLES</span></span>

### <span data-ttu-id="06244-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06244-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="06244-114">Obtém o histórico de status de conformidade por ID de iniciativa. A opção ShowOnlyChange mostra apenas alterações de status histórico.</span><span class="sxs-lookup"><span data-stu-id="06244-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="06244-115">Ignora os status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="06244-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="06244-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06244-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="06244-117">Obtém o histórico de status de conformidade pelo nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="06244-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="06244-118">A opção ShowOnlyChange mostra apenas alterações de status histórico.</span><span class="sxs-lookup"><span data-stu-id="06244-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="06244-119">Ignora os status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="06244-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="06244-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="06244-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="06244-121">Obtém o histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas à VM.</span><span class="sxs-lookup"><span data-stu-id="06244-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="06244-122">A opção ShowOnlyChange mostra apenas alterações de status histórico.</span><span class="sxs-lookup"><span data-stu-id="06244-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="06244-123">Ignora os status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="06244-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="06244-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="06244-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="06244-125">Obtém o histórico de status de conformidade por ID de iniciativa.</span><span class="sxs-lookup"><span data-stu-id="06244-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="06244-126">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="06244-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="06244-127">Obtém o histórico de status de conformidade pelo nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="06244-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="06244-128">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="06244-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="06244-129">Obtém o histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas à VM.</span><span class="sxs-lookup"><span data-stu-id="06244-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="06244-130">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="06244-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="06244-131">Obter o status da política de configuração de convidado por ReportId.</span><span class="sxs-lookup"><span data-stu-id="06244-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="06244-132">ReportId é a propriedade ReportId que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="06244-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="06244-133">(Consulte outros exemplos)</span><span class="sxs-lookup"><span data-stu-id="06244-133">(please refer other examples)</span></span>

## <span data-ttu-id="06244-134">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="06244-134">PARAMETERS</span></span>

### <span data-ttu-id="06244-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06244-135">-DefaultProfile</span></span>
<span data-ttu-id="06244-136">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06244-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06244-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="06244-137">-InitiativeId</span></span>
<span data-ttu-id="06244-138">ID de definição de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado</span><span class="sxs-lookup"><span data-stu-id="06244-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06244-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="06244-139">-InitiativeName</span></span>
<span data-ttu-id="06244-140">Nome de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado</span><span class="sxs-lookup"><span data-stu-id="06244-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06244-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06244-141">-ResourceGroupName</span></span>
<span data-ttu-id="06244-142">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06244-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06244-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="06244-143">-ShowOnlyChange</span></span>
<span data-ttu-id="06244-144">Mostra alterações de status históricas somente para políticas de configuração de convidados.</span><span class="sxs-lookup"><span data-stu-id="06244-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="06244-145">Ignora os status que não foram alterados entre duas executações de auditoria de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="06244-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06244-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="06244-146">-VMName</span></span>
<span data-ttu-id="06244-147">Nome da VM.</span><span class="sxs-lookup"><span data-stu-id="06244-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06244-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06244-148">CommonParameters</span></span>
<span data-ttu-id="06244-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06244-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06244-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06244-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06244-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06244-151">INPUTS</span></span>

### <span data-ttu-id="06244-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06244-152">None</span></span>
## <span data-ttu-id="06244-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="06244-153">OUTPUTS</span></span>

### <span data-ttu-id="06244-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="06244-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="06244-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="06244-155">NOTES</span></span>

## <span data-ttu-id="06244-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06244-156">RELATED LINKS</span></span>
