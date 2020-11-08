---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115398"
---
# <span data-ttu-id="b32ae-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="b32ae-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="b32ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b32ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b32ae-103">Obtém o histórico de status de conformidade da política de configuração de convidado para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.</span><span class="sxs-lookup"><span data-stu-id="b32ae-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="b32ae-104">Uma iniciativa é uma política de tipo de definição "iniciativa".</span><span class="sxs-lookup"><span data-stu-id="b32ae-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="b32ae-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b32ae-105">SYNTAX</span></span>

### <span data-ttu-id="b32ae-106">InitiativeNameScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="b32ae-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b32ae-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="b32ae-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b32ae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b32ae-108">DESCRIPTION</span></span>
<span data-ttu-id="b32ae-109">O cmdlet Get-AzVMGuestPolicyStatusHistory Obtém o histórico do status de conformidade das políticas de configuração de convidado para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.</span><span class="sxs-lookup"><span data-stu-id="b32ae-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="b32ae-110">Uma iniciativa é uma política de tipo de definição "iniciativa".</span><span class="sxs-lookup"><span data-stu-id="b32ae-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="b32ae-111">Use o cmdlet Get-AzVMGuestPolicyStatus para obter detalhes de um único status de conformidade usando o ReportID que pode ser encontrado na saída do cmdlet Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="b32ae-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="b32ae-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b32ae-112">EXAMPLES</span></span>

### <span data-ttu-id="b32ae-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b32ae-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="b32ae-114">Obtém o histórico de status de conformidade por ID da iniciativa. ShowOnlyChange opção mostra apenas alterações de status históricas.</span><span class="sxs-lookup"><span data-stu-id="b32ae-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="b32ae-115">Ignora status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="b32ae-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="b32ae-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b32ae-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="b32ae-117">Obtém o histórico do status de conformidade por nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="b32ae-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="b32ae-118">A opção ShowOnlyChange mostra apenas alterações de status históricas.</span><span class="sxs-lookup"><span data-stu-id="b32ae-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="b32ae-119">Ignora status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="b32ae-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="b32ae-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b32ae-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="b32ae-121">Obtém o histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas à VM.</span><span class="sxs-lookup"><span data-stu-id="b32ae-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="b32ae-122">A opção ShowOnlyChange mostra apenas alterações de status históricas.</span><span class="sxs-lookup"><span data-stu-id="b32ae-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="b32ae-123">Ignora status que não foram alterados entre duas verificações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="b32ae-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="b32ae-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b32ae-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="b32ae-125">Obtém o histórico de status de conformidade por ID da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="b32ae-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="b32ae-126">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="b32ae-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="b32ae-127">Obtém o histórico do status de conformidade por nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="b32ae-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="b32ae-128">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="b32ae-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="b32ae-129">Obtém o histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas à VM.</span><span class="sxs-lookup"><span data-stu-id="b32ae-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="b32ae-130">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="b32ae-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="b32ae-131">Obter status da política de configuração de convidado por ReportID.</span><span class="sxs-lookup"><span data-stu-id="b32ae-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="b32ae-132">O ReportID é a Propriedade ReportID que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="b32ae-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="b32ae-133">(por favor, consulte outros exemplos)</span><span class="sxs-lookup"><span data-stu-id="b32ae-133">(please refer other examples)</span></span>

## <span data-ttu-id="b32ae-134">OS</span><span class="sxs-lookup"><span data-stu-id="b32ae-134">PARAMETERS</span></span>

### <span data-ttu-id="b32ae-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32ae-135">-DefaultProfile</span></span>
<span data-ttu-id="b32ae-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b32ae-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b32ae-137">-Initiativeid</span><span class="sxs-lookup"><span data-stu-id="b32ae-137">-InitiativeId</span></span>
<span data-ttu-id="b32ae-138">A ID da definição de uma política na qual o tipo de definição é iniciativa e categoria é configuração de convidado</span><span class="sxs-lookup"><span data-stu-id="b32ae-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="b32ae-139">-Initiativename</span><span class="sxs-lookup"><span data-stu-id="b32ae-139">-InitiativeName</span></span>
<span data-ttu-id="b32ae-140">O nome de uma política em que o tipo de definição é iniciativa e categoria é configuração de convidado</span><span class="sxs-lookup"><span data-stu-id="b32ae-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="b32ae-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32ae-141">-ResourceGroupName</span></span>
<span data-ttu-id="b32ae-142">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b32ae-142">Resource group name.</span></span>

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

### <span data-ttu-id="b32ae-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="b32ae-143">-ShowOnlyChange</span></span>
<span data-ttu-id="b32ae-144">Mostra as alterações do status histórico somente para políticas de configuração de convidado.</span><span class="sxs-lookup"><span data-stu-id="b32ae-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="b32ae-145">Ignora status que não foram alterados entre duas execuções de auditoria de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="b32ae-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="b32ae-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="b32ae-146">-VMName</span></span>
<span data-ttu-id="b32ae-147">Nome da VM.</span><span class="sxs-lookup"><span data-stu-id="b32ae-147">VM name.</span></span>

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

### <span data-ttu-id="b32ae-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32ae-148">CommonParameters</span></span>
<span data-ttu-id="b32ae-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b32ae-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32ae-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b32ae-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32ae-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b32ae-151">INPUTS</span></span>

### <span data-ttu-id="b32ae-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b32ae-152">None</span></span>
## <span data-ttu-id="b32ae-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b32ae-153">OUTPUTS</span></span>

### <span data-ttu-id="b32ae-154">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="b32ae-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="b32ae-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b32ae-155">NOTES</span></span>

## <span data-ttu-id="b32ae-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b32ae-156">RELATED LINKS</span></span>
