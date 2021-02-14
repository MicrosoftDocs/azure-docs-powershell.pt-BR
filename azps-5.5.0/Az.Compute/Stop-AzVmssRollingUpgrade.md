---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111082"
---
# <span data-ttu-id="6ab7f-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ab7f-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="6ab7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ab7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab7f-103">Cancela a atualização atual em escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="6ab7f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ab7f-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ab7f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ab7f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ab7f-106">Cancela a atualização atual em escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="6ab7f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6ab7f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ab7f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ab7f-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="6ab7f-109">Esse comando cancela a atualização em movimento do conjunto de escala VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="6ab7f-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="6ab7f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ab7f-110">PARAMETERS</span></span>

### <span data-ttu-id="6ab7f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ab7f-111">-AsJob</span></span>
<span data-ttu-id="6ab7f-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6ab7f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ab7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab7f-113">-DefaultProfile</span></span>
<span data-ttu-id="6ab7f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab7f-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6ab7f-115">-Force</span></span>
<span data-ttu-id="6ab7f-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ab7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab7f-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ab7f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ab7f-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6ab7f-119">-VMScaleSetName</span></span>
<span data-ttu-id="6ab7f-120">O nome do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="6ab7f-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6ab7f-121">-Confirm</span></span>
<span data-ttu-id="6ab7f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab7f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab7f-123">-WhatIf</span></span>
<span data-ttu-id="6ab7f-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab7f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ab7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab7f-126">CommonParameters</span></span>
<span data-ttu-id="6ab7f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab7f-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ab7f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab7f-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="6ab7f-129">INPUTS</span></span>

### <span data-ttu-id="6ab7f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6ab7f-130">System.String</span></span>

## <span data-ttu-id="6ab7f-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="6ab7f-131">OUTPUTS</span></span>

### <span data-ttu-id="6ab7f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6ab7f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6ab7f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="6ab7f-133">NOTES</span></span>

## <span data-ttu-id="6ab7f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ab7f-134">RELATED LINKS</span></span>
