---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263888"
---
# <span data-ttu-id="91841-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="91841-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="91841-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91841-102">SYNOPSIS</span></span>
<span data-ttu-id="91841-103">Avaliar o estado do patch de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91841-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="91841-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91841-104">SYNTAX</span></span>

### <span data-ttu-id="91841-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="91841-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91841-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="91841-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91841-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91841-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91841-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91841-108">DESCRIPTION</span></span>
<span data-ttu-id="91841-109">Avalia o status do patch de uma VM e relata todos os patches detectados que estão disponíveis para instalação.</span><span class="sxs-lookup"><span data-stu-id="91841-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="91841-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91841-110">EXAMPLES</span></span>

### <span data-ttu-id="91841-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91841-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="91841-112">OS</span><span class="sxs-lookup"><span data-stu-id="91841-112">PARAMETERS</span></span>

### <span data-ttu-id="91841-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91841-113">-AsJob</span></span>
<span data-ttu-id="91841-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="91841-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91841-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91841-115">-DefaultProfile</span></span>
<span data-ttu-id="91841-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91841-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91841-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91841-117">-ResourceGroupName</span></span>
<span data-ttu-id="91841-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="91841-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91841-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91841-119">-ResourceId</span></span>
<span data-ttu-id="91841-120">ID do recurso para sua máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91841-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91841-121">-VM</span><span class="sxs-lookup"><span data-stu-id="91841-121">-VM</span></span>
<span data-ttu-id="91841-122">Objeto da máquina virtual do PowerShell</span><span class="sxs-lookup"><span data-stu-id="91841-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91841-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="91841-123">-VMName</span></span>
<span data-ttu-id="91841-124">Nome da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="91841-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91841-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91841-125">-Confirm</span></span>
<span data-ttu-id="91841-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91841-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91841-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91841-127">-WhatIf</span></span>
<span data-ttu-id="91841-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91841-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91841-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91841-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91841-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91841-130">CommonParameters</span></span>
<span data-ttu-id="91841-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91841-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91841-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91841-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91841-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91841-133">INPUTS</span></span>

### <span data-ttu-id="91841-134">System. String</span><span class="sxs-lookup"><span data-stu-id="91841-134">System.String</span></span>

## <span data-ttu-id="91841-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91841-135">OUTPUTS</span></span>

### <span data-ttu-id="91841-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="91841-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="91841-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91841-137">NOTES</span></span>

## <span data-ttu-id="91841-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91841-138">RELATED LINKS</span></span>
