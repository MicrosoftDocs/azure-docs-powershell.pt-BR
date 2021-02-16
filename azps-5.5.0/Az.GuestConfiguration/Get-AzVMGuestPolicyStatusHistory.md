---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117643"
---
# <span data-ttu-id="4bbdb-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="4bbdb-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="4bbdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbdb-103">Obtém o histórico de status da política de configuração de convidado para uma iniciativa do tipo "Configuração de Convidado" atribuída a um VM.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="4bbdb-104">Uma iniciativa é uma política de tipo de definição "Iniciativa".</span><span class="sxs-lookup"><span data-stu-id="4bbdb-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="4bbdb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bbdb-105">SYNTAX</span></span>

### <span data-ttu-id="4bbdb-106">InitiativeNameScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4bbdb-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbdb-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="4bbdb-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bbdb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bbdb-108">DESCRIPTION</span></span>
<span data-ttu-id="4bbdb-109">O Get-AzVMGuestPolicyStatusHistory cmdlet obtém o histórico de status de conformidade das políticas de configuração de convidado para uma iniciativa do tipo "Configuração de Convidado" atribuída a um VM.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="4bbdb-110">Uma iniciativa é uma política de tipo de definição "Iniciativa".</span><span class="sxs-lookup"><span data-stu-id="4bbdb-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="4bbdb-111">Use Get-AzVMGuestPolicyStatus cmdlet para obter detalhes sobre um único status de conformidade usando ReportId que pode ser encontrado na saída de Get-AzVMGuestPolicyStatusHistory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="4bbdb-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4bbdb-112">EXAMPLES</span></span>

### <span data-ttu-id="4bbdb-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bbdb-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="4bbdb-114">Obtém o histórico de status de conformidade por ID de iniciativa. A opção ShowOnlyChange mostra apenas as alterações de status de histórico.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="4bbdb-115">Ignora os status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="4bbdb-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4bbdb-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="4bbdb-117">Obtém o histórico de status de conformidade pelo nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="4bbdb-118">A opção ShowOnlyChange mostra apenas as alterações de status de histórico.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="4bbdb-119">Ignora os status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="4bbdb-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4bbdb-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="4bbdb-121">Obtém histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas ao VM.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="4bbdb-122">A opção ShowOnlyChange mostra apenas as alterações de status de histórico.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="4bbdb-123">Ignora os status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="4bbdb-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4bbdb-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="4bbdb-125">Obtém o histórico de status de conformidade por ID de iniciativa.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="4bbdb-126">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="4bbdb-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="4bbdb-127">Obtém o histórico de status de conformidade pelo nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="4bbdb-128">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="4bbdb-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="4bbdb-129">Obtém histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas ao VM.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="4bbdb-130">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="4bbdb-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="4bbdb-131">Obter status da política de configuração de convidado pelo ReportId.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="4bbdb-132">O ReportId é a propriedade ReportId que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="4bbdb-133">(consulte outros exemplos)</span><span class="sxs-lookup"><span data-stu-id="4bbdb-133">(please refer other examples)</span></span>

## <span data-ttu-id="4bbdb-134">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bbdb-134">PARAMETERS</span></span>

### <span data-ttu-id="4bbdb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbdb-135">-DefaultProfile</span></span>
<span data-ttu-id="4bbdb-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bbdb-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="4bbdb-137">-InitiativeId</span></span>
<span data-ttu-id="4bbdb-138">ID de definição de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado</span><span class="sxs-lookup"><span data-stu-id="4bbdb-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="4bbdb-139">-Nomeda Iniciativa</span><span class="sxs-lookup"><span data-stu-id="4bbdb-139">-InitiativeName</span></span>
<span data-ttu-id="4bbdb-140">Nome de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado</span><span class="sxs-lookup"><span data-stu-id="4bbdb-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="4bbdb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbdb-141">-ResourceGroupName</span></span>
<span data-ttu-id="4bbdb-142">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-142">Resource group name.</span></span>

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

### <span data-ttu-id="4bbdb-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="4bbdb-143">-ShowOnlyChange</span></span>
<span data-ttu-id="4bbdb-144">Mostra as alterações de status de histórico somente para políticas de configuração de convidado.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="4bbdb-145">Ignora os status que não foram alterados entre duas auditorias de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="4bbdb-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="4bbdb-146">-VMName</span></span>
<span data-ttu-id="4bbdb-147">Nome do VM.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-147">VM name.</span></span>

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

### <span data-ttu-id="4bbdb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbdb-148">CommonParameters</span></span>
<span data-ttu-id="4bbdb-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bbdb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbdb-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbdb-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbdb-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="4bbdb-151">INPUTS</span></span>

### <span data-ttu-id="4bbdb-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4bbdb-152">None</span></span>
## <span data-ttu-id="4bbdb-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="4bbdb-153">OUTPUTS</span></span>

### <span data-ttu-id="4bbdb-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="4bbdb-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="4bbdb-155">Notas</span><span class="sxs-lookup"><span data-stu-id="4bbdb-155">NOTES</span></span>

## <span data-ttu-id="4bbdb-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bbdb-156">RELATED LINKS</span></span>
