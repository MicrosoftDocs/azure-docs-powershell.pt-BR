---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 915dd31b522fdbc7955494c0f76d69ee5a4b8376
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775949"
---
# <span data-ttu-id="6bab5-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6bab5-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="6bab5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bab5-102">SYNOPSIS</span></span>
<span data-ttu-id="6bab5-103">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="6bab5-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="6bab5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bab5-104">SYNTAX</span></span>

### <span data-ttu-id="6bab5-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="6bab5-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bab5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="6bab5-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bab5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bab5-107">DESCRIPTION</span></span>
<span data-ttu-id="6bab5-108">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="6bab5-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="6bab5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bab5-109">EXAMPLES</span></span>

### <span data-ttu-id="6bab5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6bab5-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="6bab5-111">Esse comando cancela a atualização em andamento do conjunto de dimensionamento de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="6bab5-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="6bab5-112">OS</span><span class="sxs-lookup"><span data-stu-id="6bab5-112">PARAMETERS</span></span>

### <span data-ttu-id="6bab5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bab5-113">-AsJob</span></span>
<span data-ttu-id="6bab5-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6bab5-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bab5-115">-DefaultProfile</span></span>
<span data-ttu-id="6bab5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bab5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bab5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6bab5-117">-Force</span></span>
<span data-ttu-id="6bab5-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6bab5-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bab5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bab5-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bab5-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bab5-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bab5-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6bab5-121">-VMScaleSetName</span></span>
<span data-ttu-id="6bab5-122">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="6bab5-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bab5-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6bab5-123">-Confirm</span></span>
<span data-ttu-id="6bab5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bab5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bab5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bab5-125">-WhatIf</span></span>
<span data-ttu-id="6bab5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6bab5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bab5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6bab5-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bab5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bab5-128">CommonParameters</span></span>
<span data-ttu-id="6bab5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bab5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bab5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bab5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bab5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bab5-131">INPUTS</span></span>

### <span data-ttu-id="6bab5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6bab5-132">System.String</span></span>

## <span data-ttu-id="6bab5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bab5-133">OUTPUTS</span></span>

### <span data-ttu-id="6bab5-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6bab5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6bab5-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bab5-135">NOTES</span></span>

## <span data-ttu-id="6bab5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bab5-136">RELATED LINKS</span></span>

