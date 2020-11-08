---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116773"
---
# <span data-ttu-id="89e00-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="89e00-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="89e00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89e00-102">SYNOPSIS</span></span>
<span data-ttu-id="89e00-103">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="89e00-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="89e00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89e00-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e00-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89e00-105">DESCRIPTION</span></span>
<span data-ttu-id="89e00-106">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="89e00-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="89e00-107">Instâncias que já estão executando a versão do sistema operacional mais recente não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="89e00-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="89e00-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89e00-108">EXAMPLES</span></span>

### <span data-ttu-id="89e00-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89e00-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="89e00-110">Esse comando inicia uma atualização sem interrupção de todas as instâncias de VM do conjunto de escalas de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="89e00-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="89e00-111">OS</span><span class="sxs-lookup"><span data-stu-id="89e00-111">PARAMETERS</span></span>

### <span data-ttu-id="89e00-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89e00-112">-AsJob</span></span>
<span data-ttu-id="89e00-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89e00-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89e00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e00-114">-DefaultProfile</span></span>
<span data-ttu-id="89e00-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89e00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e00-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e00-116">-ResourceGroupName</span></span>
<span data-ttu-id="89e00-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89e00-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="89e00-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="89e00-118">-VMScaleSetName</span></span>
<span data-ttu-id="89e00-119">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="89e00-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="89e00-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89e00-120">-Confirm</span></span>
<span data-ttu-id="89e00-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89e00-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e00-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e00-122">-WhatIf</span></span>
<span data-ttu-id="89e00-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89e00-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89e00-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89e00-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e00-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e00-125">CommonParameters</span></span>
<span data-ttu-id="89e00-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e00-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e00-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89e00-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e00-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89e00-128">INPUTS</span></span>

### <span data-ttu-id="89e00-129">System. String</span><span class="sxs-lookup"><span data-stu-id="89e00-129">System.String</span></span>

## <span data-ttu-id="89e00-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89e00-130">OUTPUTS</span></span>

### <span data-ttu-id="89e00-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="89e00-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="89e00-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89e00-132">NOTES</span></span>

## <span data-ttu-id="89e00-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89e00-133">RELATED LINKS</span></span>
