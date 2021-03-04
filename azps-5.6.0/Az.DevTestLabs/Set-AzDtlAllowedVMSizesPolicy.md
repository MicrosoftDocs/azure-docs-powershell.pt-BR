---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 04538710a078c72c7b91725823601a55c21ef846
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890858"
---
# <span data-ttu-id="ee7ee-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ee7ee-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="ee7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7ee-103">Define a política de tamanhos de máquina virtual permitidos de um laboratório em Laboratórios DevTest.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ee7ee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee7ee-104">SYNTAX</span></span>

### <span data-ttu-id="ee7ee-105">Habilitar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee7ee-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee7ee-106">Desabilitar</span><span class="sxs-lookup"><span data-stu-id="ee7ee-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee7ee-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee7ee-107">DESCRIPTION</span></span>
<span data-ttu-id="ee7ee-108">O cmdlet **Set-AzDtlAllowedVMSizesPolicy** define a política de tamanhos de máquina virtual permitidos, que especifica uma lista de tamanhos de máquina virtual permitidos em um laboratório.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="ee7ee-109">O cmdlet usa o grupo de recursos especificado e o nome do laboratório para definir a política.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="ee7ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee7ee-110">EXAMPLES</span></span>

## <span data-ttu-id="ee7ee-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee7ee-111">PARAMETERS</span></span>

### <span data-ttu-id="ee7ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee7ee-112">-DefaultProfile</span></span>
<span data-ttu-id="ee7ee-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ee7ee-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee7ee-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="ee7ee-114">-Disable</span></span>
<span data-ttu-id="ee7ee-115">Indica que esse cmdlet desabilita a política.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7ee-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="ee7ee-116">-Enable</span></span>
<span data-ttu-id="ee7ee-117">Indica que esse cmdlet habilita a política.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7ee-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="ee7ee-118">-LabName</span></span>
<span data-ttu-id="ee7ee-119">Especifica o nome do laboratório para o qual este cmdlet define a política de tamanhos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee7ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee7ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee7ee-121">Especifica o nome do grupo de recursos ao que o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee7ee-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="ee7ee-122">-VmSizes</span></span>
<span data-ttu-id="ee7ee-123">Especifica, como uma matriz de cadeias de caracteres, a lista de tamanhos de máquina virtual permitidos no laboratório.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7ee-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee7ee-124">-Confirm</span></span>
<span data-ttu-id="ee7ee-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7ee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee7ee-126">-WhatIf</span></span>
<span data-ttu-id="ee7ee-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee7ee-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7ee-129">CommonParameters</span></span>
<span data-ttu-id="ee7ee-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee7ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7ee-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee7ee-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7ee-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee7ee-132">INPUTS</span></span>

### <span data-ttu-id="ee7ee-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ee7ee-133">System.String</span></span>

## <span data-ttu-id="ee7ee-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee7ee-134">OUTPUTS</span></span>

### <span data-ttu-id="ee7ee-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ee7ee-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="ee7ee-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee7ee-136">NOTES</span></span>

## <span data-ttu-id="ee7ee-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee7ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee7ee-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ee7ee-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


