---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: fb3d6f08eaa540e208830a15563b8edd8c2432ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886692"
---
# <span data-ttu-id="483b5-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="483b5-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="483b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483b5-102">SYNOPSIS</span></span>
<span data-ttu-id="483b5-103">Inicia uma atualização de rolagem para mover todas as instâncias de conjunto de escala de máquina virtual para a versão mais recente disponível do sistema operacional de imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="483b5-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="483b5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="483b5-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="483b5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="483b5-105">DESCRIPTION</span></span>
<span data-ttu-id="483b5-106">Inicia uma atualização de rolagem para mover todas as instâncias de conjunto de escala de máquina virtual para a versão mais recente disponível do sistema operacional de imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="483b5-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="483b5-107">As instâncias que já estão executando a versão mais recente do sistema operacional disponível não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="483b5-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="483b5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="483b5-108">EXAMPLES</span></span>

### <span data-ttu-id="483b5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="483b5-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="483b5-110">Este comando inicia uma atualização de rolagem de todas as instâncias de vm do conjunto de escala de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="483b5-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="483b5-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="483b5-111">PARAMETERS</span></span>

### <span data-ttu-id="483b5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="483b5-112">-AsJob</span></span>
<span data-ttu-id="483b5-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="483b5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="483b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483b5-114">-DefaultProfile</span></span>
<span data-ttu-id="483b5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="483b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="483b5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483b5-116">-ResourceGroupName</span></span>
<span data-ttu-id="483b5-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="483b5-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="483b5-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="483b5-118">-VMScaleSetName</span></span>
<span data-ttu-id="483b5-119">O nome do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="483b5-119">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483b5-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="483b5-120">-Confirm</span></span>
<span data-ttu-id="483b5-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="483b5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483b5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483b5-122">-WhatIf</span></span>
<span data-ttu-id="483b5-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="483b5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483b5-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="483b5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483b5-125">CommonParameters</span></span>
<span data-ttu-id="483b5-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483b5-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="483b5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483b5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="483b5-128">INPUTS</span></span>

### <span data-ttu-id="483b5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="483b5-129">System.String</span></span>

## <span data-ttu-id="483b5-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="483b5-130">OUTPUTS</span></span>

### <span data-ttu-id="483b5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="483b5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="483b5-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="483b5-132">NOTES</span></span>

## <span data-ttu-id="483b5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="483b5-133">RELATED LINKS</span></span>
