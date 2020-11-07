---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: fb35bac6f43ca444762ed1cbf8511d93eab10daf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771088"
---
# <span data-ttu-id="d2333-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="d2333-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="d2333-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2333-102">SYNOPSIS</span></span>
<span data-ttu-id="d2333-103">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="d2333-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="d2333-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2333-104">SYNTAX</span></span>

### <span data-ttu-id="d2333-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2333-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2333-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d2333-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2333-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2333-107">DESCRIPTION</span></span>
<span data-ttu-id="d2333-108">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="d2333-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="d2333-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2333-109">EXAMPLES</span></span>

### <span data-ttu-id="d2333-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2333-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="d2333-111">Esse comando cancela a atualização em andamento do conjunto de dimensionamento de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="d2333-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="d2333-112">OS</span><span class="sxs-lookup"><span data-stu-id="d2333-112">PARAMETERS</span></span>

### <span data-ttu-id="d2333-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2333-113">-AsJob</span></span>
<span data-ttu-id="d2333-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d2333-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2333-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2333-115">-DefaultProfile</span></span>
<span data-ttu-id="d2333-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2333-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2333-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d2333-117">-Force</span></span>
<span data-ttu-id="d2333-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d2333-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2333-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2333-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2333-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2333-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2333-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d2333-121">-VMScaleSetName</span></span>
<span data-ttu-id="d2333-122">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="d2333-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2333-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2333-123">-Confirm</span></span>
<span data-ttu-id="d2333-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2333-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2333-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2333-125">-WhatIf</span></span>
<span data-ttu-id="d2333-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2333-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2333-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2333-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2333-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2333-128">CommonParameters</span></span>
<span data-ttu-id="d2333-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2333-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2333-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2333-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2333-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2333-131">INPUTS</span></span>

### <span data-ttu-id="d2333-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d2333-132">System.String</span></span>

## <span data-ttu-id="d2333-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2333-133">OUTPUTS</span></span>

### <span data-ttu-id="d2333-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d2333-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d2333-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2333-135">NOTES</span></span>

## <span data-ttu-id="d2333-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2333-136">RELATED LINKS</span></span>
