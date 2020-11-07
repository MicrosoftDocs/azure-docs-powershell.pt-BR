---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948105"
---
# <span data-ttu-id="cba69-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="cba69-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="cba69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cba69-102">SYNOPSIS</span></span>
<span data-ttu-id="cba69-103">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="cba69-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cba69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cba69-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cba69-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cba69-105">DESCRIPTION</span></span>
<span data-ttu-id="cba69-106">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="cba69-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cba69-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cba69-107">EXAMPLES</span></span>

### <span data-ttu-id="cba69-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cba69-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cba69-109">Esse comando cancela a atualização em andamento do conjunto de dimensionamento de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="cba69-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="cba69-110">OS</span><span class="sxs-lookup"><span data-stu-id="cba69-110">PARAMETERS</span></span>

### <span data-ttu-id="cba69-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cba69-111">-AsJob</span></span>
<span data-ttu-id="cba69-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cba69-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cba69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba69-113">-DefaultProfile</span></span>
<span data-ttu-id="cba69-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cba69-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba69-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cba69-115">-Force</span></span>
<span data-ttu-id="cba69-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cba69-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cba69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba69-117">-ResourceGroupName</span></span>
<span data-ttu-id="cba69-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cba69-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cba69-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cba69-119">-VMScaleSetName</span></span>
<span data-ttu-id="cba69-120">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="cba69-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="cba69-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cba69-121">-Confirm</span></span>
<span data-ttu-id="cba69-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cba69-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cba69-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cba69-123">-WhatIf</span></span>
<span data-ttu-id="cba69-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cba69-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cba69-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cba69-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cba69-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba69-126">CommonParameters</span></span>
<span data-ttu-id="cba69-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba69-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba69-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cba69-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba69-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cba69-129">INPUTS</span></span>

### <span data-ttu-id="cba69-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cba69-130">System.String</span></span>

## <span data-ttu-id="cba69-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cba69-131">OUTPUTS</span></span>

### <span data-ttu-id="cba69-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cba69-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cba69-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cba69-133">NOTES</span></span>

## <span data-ttu-id="cba69-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cba69-134">RELATED LINKS</span></span>
