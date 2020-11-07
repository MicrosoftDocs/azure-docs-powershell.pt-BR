---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: f3ebb13438d88a65e763d81936704db859bc1e97
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775962"
---
# <span data-ttu-id="6d933-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6d933-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="6d933-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d933-102">SYNOPSIS</span></span>
<span data-ttu-id="6d933-103">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6d933-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="6d933-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d933-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d933-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d933-105">DESCRIPTION</span></span>
<span data-ttu-id="6d933-106">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6d933-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="6d933-107">Instâncias que já estão executando a versão do sistema operacional mais recente não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="6d933-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="6d933-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d933-108">EXAMPLES</span></span>

### <span data-ttu-id="6d933-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d933-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="6d933-110">Esse comando inicia uma atualização sem interrupção de todas as instâncias de VM do conjunto de escalas de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="6d933-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="6d933-111">OS</span><span class="sxs-lookup"><span data-stu-id="6d933-111">PARAMETERS</span></span>

### <span data-ttu-id="6d933-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d933-112">-AsJob</span></span>
<span data-ttu-id="6d933-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6d933-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d933-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d933-114">-DefaultProfile</span></span>
<span data-ttu-id="6d933-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d933-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d933-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d933-116">-ResourceGroupName</span></span>
<span data-ttu-id="6d933-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d933-117">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d933-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6d933-118">-VMScaleSetName</span></span>
<span data-ttu-id="6d933-119">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="6d933-119">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d933-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d933-120">-Confirm</span></span>
<span data-ttu-id="6d933-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d933-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d933-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d933-122">-WhatIf</span></span>
<span data-ttu-id="6d933-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d933-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d933-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d933-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d933-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d933-125">CommonParameters</span></span>
<span data-ttu-id="6d933-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d933-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d933-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d933-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d933-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d933-128">INPUTS</span></span>

### <span data-ttu-id="6d933-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6d933-129">System.String</span></span>

## <span data-ttu-id="6d933-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d933-130">OUTPUTS</span></span>

### <span data-ttu-id="6d933-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6d933-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6d933-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d933-132">NOTES</span></span>

## <span data-ttu-id="6d933-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d933-133">RELATED LINKS</span></span>

