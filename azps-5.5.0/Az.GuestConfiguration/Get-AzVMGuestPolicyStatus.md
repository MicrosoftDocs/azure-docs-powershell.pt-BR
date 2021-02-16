---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113632"
---
# <span data-ttu-id="14b3f-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="14b3f-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="14b3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="14b3f-103">Obtém status da política de configuração de convidado (detalhado) para uma iniciativa do tipo "Configuração de Convidado" atribuída a um VM.</span><span class="sxs-lookup"><span data-stu-id="14b3f-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="14b3f-104">Uma iniciativa é uma política de tipo de definição "Iniciativa".</span><span class="sxs-lookup"><span data-stu-id="14b3f-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="14b3f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14b3f-105">SYNTAX</span></span>

### <span data-ttu-id="14b3f-106">VmScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14b3f-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b3f-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="14b3f-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b3f-108">NomeDaEminciação</span><span class="sxs-lookup"><span data-stu-id="14b3f-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b3f-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="14b3f-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b3f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="14b3f-110">DESCRIPTION</span></span>
<span data-ttu-id="14b3f-111">O Get-AzVMGuestPolicyStatus cmdlet obtém status de política de configuração de convidado para uma iniciativa do tipo "Configuração de Convidado" atribuída a um VM.</span><span class="sxs-lookup"><span data-stu-id="14b3f-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="14b3f-112">Uma iniciativa é uma política de tipo de definição "Iniciativa".</span><span class="sxs-lookup"><span data-stu-id="14b3f-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="14b3f-113">Este cmdlet obtém status de conformidade do VM e os motivos pelos quais ele não está em conformidade com as políticas individuais da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="14b3f-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="14b3f-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14b3f-114">EXAMPLES</span></span>

### <span data-ttu-id="14b3f-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14b3f-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="14b3f-116">Obter todos os status de política de configuração de convidado mais recentes para um VM.</span><span class="sxs-lookup"><span data-stu-id="14b3f-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="14b3f-117">O status inclui o status de conformidade do VM para cada política em todas as iniciativas do tipo "Configuração de Convidado", motivos de conformidade, tempo da verificação de conformidade, informações de recurso que foram verificadas para conformidade.</span><span class="sxs-lookup"><span data-stu-id="14b3f-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="14b3f-118">Os resultados incluem status mais recentes, não incluem status históricos anteriores.</span><span class="sxs-lookup"><span data-stu-id="14b3f-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="14b3f-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="14b3f-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="14b3f-120">Obter os status da política de configuração de convidado mais recente por ID de iniciativa. O status inclui o status de conformidade do VM para cada política na iniciativa, motivos de conformidade, tempo da verificação de conformidade, informações de recurso que foram verificadas para conformidade.</span><span class="sxs-lookup"><span data-stu-id="14b3f-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="14b3f-121">Os resultados não incluem status anteriores gerados, apenas inclui o status mais recente para cada política na iniciativa.</span><span class="sxs-lookup"><span data-stu-id="14b3f-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="14b3f-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="14b3f-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="14b3f-123">Obter os status da política de configuração de convidado mais recente por nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="14b3f-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="14b3f-124">O status inclui o status de conformidade do VM para cada política na iniciativa, motivos de conformidade, tempo da verificação de conformidade, informações de recurso que foram verificadas para conformidade.</span><span class="sxs-lookup"><span data-stu-id="14b3f-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="14b3f-125">Os resultados não incluem status anteriores gerados, apenas inclui o status mais recente para cada política na iniciativa.</span><span class="sxs-lookup"><span data-stu-id="14b3f-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="14b3f-126">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="14b3f-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="14b3f-127">Obter status da política de configuração de convidado pelo ReportId.</span><span class="sxs-lookup"><span data-stu-id="14b3f-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="14b3f-128">O ReportId é a propriedade ReportId que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatus nome da iniciativaId ou Iniciativa (consulte outros exemplos)</span><span class="sxs-lookup"><span data-stu-id="14b3f-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="14b3f-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14b3f-129">PARAMETERS</span></span>

### <span data-ttu-id="14b3f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b3f-130">-DefaultProfile</span></span>
<span data-ttu-id="14b3f-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14b3f-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b3f-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="14b3f-132">-InitiativeId</span></span>
<span data-ttu-id="14b3f-133">ID de definição de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado</span><span class="sxs-lookup"><span data-stu-id="14b3f-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b3f-134">-Nomeda Iniciativa</span><span class="sxs-lookup"><span data-stu-id="14b3f-134">-InitiativeName</span></span>
<span data-ttu-id="14b3f-135">Nome de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado</span><span class="sxs-lookup"><span data-stu-id="14b3f-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="14b3f-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="14b3f-136">-ReportId</span></span>
<span data-ttu-id="14b3f-137">ID de um status de política de Configuração de Convidado.</span><span class="sxs-lookup"><span data-stu-id="14b3f-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="14b3f-138">Uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado deve ser atribuída a um escopo para obter status.</span><span class="sxs-lookup"><span data-stu-id="14b3f-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b3f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b3f-139">-ResourceGroupName</span></span>
<span data-ttu-id="14b3f-140">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14b3f-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b3f-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="14b3f-141">-VMName</span></span>
<span data-ttu-id="14b3f-142">Nome do VM.</span><span class="sxs-lookup"><span data-stu-id="14b3f-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b3f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b3f-143">CommonParameters</span></span>
<span data-ttu-id="14b3f-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b3f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b3f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b3f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b3f-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="14b3f-146">INPUTS</span></span>

### <span data-ttu-id="14b3f-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="14b3f-147">None</span></span>
## <span data-ttu-id="14b3f-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="14b3f-148">OUTPUTS</span></span>

### <span data-ttu-id="14b3f-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="14b3f-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="14b3f-150">Notas</span><span class="sxs-lookup"><span data-stu-id="14b3f-150">NOTES</span></span>

## <span data-ttu-id="14b3f-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14b3f-151">RELATED LINKS</span></span>
