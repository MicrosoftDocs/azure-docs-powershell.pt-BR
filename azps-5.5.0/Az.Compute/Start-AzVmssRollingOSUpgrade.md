---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116871"
---
# <span data-ttu-id="ad446-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ad446-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="ad446-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad446-102">SYNOPSIS</span></span>
<span data-ttu-id="ad446-103">Inicia uma atualização em implantação para mover todas as instâncias de conjunto de escala de máquina virtual para a versão mais recente do sistema operacional de imagem da plataforma disponível.</span><span class="sxs-lookup"><span data-stu-id="ad446-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="ad446-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad446-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad446-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad446-105">DESCRIPTION</span></span>
<span data-ttu-id="ad446-106">Inicia uma atualização em implantação para mover todas as instâncias de conjunto de escala de máquina virtual para a versão mais recente do sistema operacional de imagem da plataforma disponível.</span><span class="sxs-lookup"><span data-stu-id="ad446-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="ad446-107">As instâncias que já estão executando a versão mais recente do sistema operacional disponível não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="ad446-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="ad446-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad446-108">EXAMPLES</span></span>

### <span data-ttu-id="ad446-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ad446-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ad446-110">Esse comando inicia uma atualização de rolagem de todas as instâncias vm do conjunto de escala de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="ad446-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="ad446-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad446-111">PARAMETERS</span></span>

### <span data-ttu-id="ad446-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad446-112">-AsJob</span></span>
<span data-ttu-id="ad446-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ad446-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad446-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad446-114">-DefaultProfile</span></span>
<span data-ttu-id="ad446-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ad446-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad446-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad446-116">-ResourceGroupName</span></span>
<span data-ttu-id="ad446-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad446-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad446-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ad446-118">-VMScaleSetName</span></span>
<span data-ttu-id="ad446-119">O nome do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="ad446-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="ad446-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ad446-120">-Confirm</span></span>
<span data-ttu-id="ad446-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad446-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad446-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad446-122">-WhatIf</span></span>
<span data-ttu-id="ad446-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ad446-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad446-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad446-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad446-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad446-125">CommonParameters</span></span>
<span data-ttu-id="ad446-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad446-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad446-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad446-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad446-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="ad446-128">INPUTS</span></span>

### <span data-ttu-id="ad446-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ad446-129">System.String</span></span>

## <span data-ttu-id="ad446-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="ad446-130">OUTPUTS</span></span>

### <span data-ttu-id="ad446-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ad446-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ad446-132">Notas</span><span class="sxs-lookup"><span data-stu-id="ad446-132">NOTES</span></span>

## <span data-ttu-id="ad446-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad446-133">RELATED LINKS</span></span>
