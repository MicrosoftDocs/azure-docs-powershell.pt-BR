---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941154"
---
# <span data-ttu-id="29a7e-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="29a7e-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="29a7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="29a7e-103">Obtém status da política de configuração de convidado (detalhado) para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.</span><span class="sxs-lookup"><span data-stu-id="29a7e-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="29a7e-104">Uma iniciativa é uma política de tipo de definição "iniciativa".</span><span class="sxs-lookup"><span data-stu-id="29a7e-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="29a7e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29a7e-105">SYNTAX</span></span>

### <span data-ttu-id="29a7e-106">VmScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="29a7e-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29a7e-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="29a7e-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29a7e-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="29a7e-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29a7e-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="29a7e-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29a7e-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29a7e-110">DESCRIPTION</span></span>
<span data-ttu-id="29a7e-111">O cmdlet Get-AzVMGuestPolicyStatus Obtém status da política de configuração de convidado para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.</span><span class="sxs-lookup"><span data-stu-id="29a7e-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="29a7e-112">Uma iniciativa é uma política de tipo de definição "iniciativa".</span><span class="sxs-lookup"><span data-stu-id="29a7e-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="29a7e-113">Esse cmdlet obtém status de conformidade da VM e os motivos pelos quais ele não é compatível com as políticas individuais na iniciativa.</span><span class="sxs-lookup"><span data-stu-id="29a7e-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="29a7e-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29a7e-114">EXAMPLES</span></span>

### <span data-ttu-id="29a7e-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29a7e-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="29a7e-116">Obtenha todos os status da política de configuração de convidado mais recente para uma VM.</span><span class="sxs-lookup"><span data-stu-id="29a7e-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="29a7e-117">O status inclui o status de conformidade da VM para cada política em todas as iniciativas do tipo "configuração de convidado", motivos de conformidade, hora da verificação de conformidade, informações sobre recursos que foram verificadas quanto à conformidade.</span><span class="sxs-lookup"><span data-stu-id="29a7e-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="29a7e-118">Os resultados incluem status mais recentes, não inclui status histórico anterior.</span><span class="sxs-lookup"><span data-stu-id="29a7e-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="29a7e-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29a7e-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="29a7e-120">Obtenha os status da política de configuração de convidado mais recente por ID da iniciativa. O status inclui o status de conformidade da VM para cada política na iniciativa, motivos de conformidade, hora da verificação de conformidade, informações sobre o recurso que foram verificadas quanto à conformidade.</span><span class="sxs-lookup"><span data-stu-id="29a7e-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="29a7e-121">Os resultados não incluem o status anterior gerado, ele apenas inclui o status mais recente de cada política na iniciativa.</span><span class="sxs-lookup"><span data-stu-id="29a7e-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="29a7e-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="29a7e-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="29a7e-123">Obtenha os status da política de configuração de convidado mais recente por nome da iniciativa.</span><span class="sxs-lookup"><span data-stu-id="29a7e-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="29a7e-124">O status inclui o status de conformidade da VM para cada política na iniciativa, motivos de conformidade, hora da verificação de conformidade, informações sobre o recurso que foram verificadas quanto à conformidade.</span><span class="sxs-lookup"><span data-stu-id="29a7e-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="29a7e-125">Os resultados não incluem o status anterior gerado, ele apenas inclui o status mais recente de cada política na iniciativa.</span><span class="sxs-lookup"><span data-stu-id="29a7e-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="29a7e-126">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="29a7e-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="29a7e-127">Obter status da política de configuração de convidado por ReportID.</span><span class="sxs-lookup"><span data-stu-id="29a7e-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="29a7e-128">O ReportID é a Propriedade ReportID que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatus por initiativeid ou nome da iniciativa (consulte outros exemplos)</span><span class="sxs-lookup"><span data-stu-id="29a7e-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="29a7e-129">OS</span><span class="sxs-lookup"><span data-stu-id="29a7e-129">PARAMETERS</span></span>

### <span data-ttu-id="29a7e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a7e-130">-DefaultProfile</span></span>
<span data-ttu-id="29a7e-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29a7e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29a7e-132">-Initiativeid</span><span class="sxs-lookup"><span data-stu-id="29a7e-132">-InitiativeId</span></span>
<span data-ttu-id="29a7e-133">A ID da definição de uma política na qual o tipo de definição é iniciativa e categoria é configuração de convidado</span><span class="sxs-lookup"><span data-stu-id="29a7e-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="29a7e-134">-Initiativename</span><span class="sxs-lookup"><span data-stu-id="29a7e-134">-InitiativeName</span></span>
<span data-ttu-id="29a7e-135">O nome de uma política em que o tipo de definição é iniciativa e categoria é configuração de convidado</span><span class="sxs-lookup"><span data-stu-id="29a7e-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="29a7e-136">-ReportID</span><span class="sxs-lookup"><span data-stu-id="29a7e-136">-ReportId</span></span>
<span data-ttu-id="29a7e-137">ID de um status de política de configuração de convidado.</span><span class="sxs-lookup"><span data-stu-id="29a7e-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="29a7e-138">Uma política na qual o tipo de definição é iniciativa e categoria é a configuração de convidado deve ser atribuída a um escopo para obter status.</span><span class="sxs-lookup"><span data-stu-id="29a7e-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="29a7e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a7e-139">-ResourceGroupName</span></span>
<span data-ttu-id="29a7e-140">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29a7e-140">Resource group name.</span></span>

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

### <span data-ttu-id="29a7e-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="29a7e-141">-VMName</span></span>
<span data-ttu-id="29a7e-142">Nome da VM.</span><span class="sxs-lookup"><span data-stu-id="29a7e-142">VM name.</span></span>

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

### <span data-ttu-id="29a7e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a7e-143">CommonParameters</span></span>
<span data-ttu-id="29a7e-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a7e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a7e-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a7e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a7e-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29a7e-146">INPUTS</span></span>

### <span data-ttu-id="29a7e-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="29a7e-147">None</span></span>
## <span data-ttu-id="29a7e-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29a7e-148">OUTPUTS</span></span>

### <span data-ttu-id="29a7e-149">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="29a7e-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="29a7e-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29a7e-150">NOTES</span></span>

## <span data-ttu-id="29a7e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29a7e-151">RELATED LINKS</span></span>
