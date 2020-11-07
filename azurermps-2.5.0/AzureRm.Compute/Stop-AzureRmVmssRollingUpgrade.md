---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 8893f5fc8f6bf798635fdfd5e9a16bc4179815e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786550"
---
# <span data-ttu-id="ca5b3-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ca5b3-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="ca5b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5b3-103">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca5b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca5b3-104">SYNTAX</span></span>

### <span data-ttu-id="ca5b3-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca5b3-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca5b3-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ca5b3-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca5b3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca5b3-107">DESCRIPTION</span></span>
<span data-ttu-id="ca5b3-108">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="ca5b3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca5b3-109">EXAMPLES</span></span>

### <span data-ttu-id="ca5b3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca5b3-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ca5b3-111">Esse comando cancela a atualização em andamento do conjunto de dimensionamento de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="ca5b3-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="ca5b3-112">OS</span><span class="sxs-lookup"><span data-stu-id="ca5b3-112">PARAMETERS</span></span>

### <span data-ttu-id="ca5b3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca5b3-113">-AsJob</span></span>
<span data-ttu-id="ca5b3-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ca5b3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca5b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5b3-115">-DefaultProfile</span></span>
<span data-ttu-id="ca5b3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca5b3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ca5b3-117">-Force</span></span>
<span data-ttu-id="ca5b3-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca5b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca5b3-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca5b3-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ca5b3-121">-VMScaleSetName</span></span>
<span data-ttu-id="ca5b3-122">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-122">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="ca5b3-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca5b3-123">-Confirm</span></span>
<span data-ttu-id="ca5b3-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca5b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5b3-125">-WhatIf</span></span>
<span data-ttu-id="ca5b3-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca5b3-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca5b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5b3-128">CommonParameters</span></span>
<span data-ttu-id="ca5b3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5b3-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca5b3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5b3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca5b3-131">INPUTS</span></span>

### <span data-ttu-id="ca5b3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca5b3-132">System.String</span></span>

## <span data-ttu-id="ca5b3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca5b3-133">OUTPUTS</span></span>

### <span data-ttu-id="ca5b3-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ca5b3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ca5b3-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca5b3-135">NOTES</span></span>

## <span data-ttu-id="ca5b3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca5b3-136">RELATED LINKS</span></span>

