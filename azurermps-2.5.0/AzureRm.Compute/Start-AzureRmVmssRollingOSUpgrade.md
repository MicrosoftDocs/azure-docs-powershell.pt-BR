---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
ms.openlocfilehash: 7f1cd0680d42ab83ec797b675e4505515a90548e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786553"
---
# <span data-ttu-id="61662-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="61662-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="61662-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61662-102">SYNOPSIS</span></span>
<span data-ttu-id="61662-103">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="61662-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61662-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61662-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61662-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61662-105">DESCRIPTION</span></span>
<span data-ttu-id="61662-106">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="61662-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="61662-107">Instâncias que já estão executando a versão do sistema operacional mais recente não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="61662-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="61662-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61662-108">EXAMPLES</span></span>

### <span data-ttu-id="61662-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61662-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="61662-110">Esse comando inicia uma atualização sem interrupção de todas as instâncias de VM do conjunto de escalas de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="61662-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="61662-111">OS</span><span class="sxs-lookup"><span data-stu-id="61662-111">PARAMETERS</span></span>

### <span data-ttu-id="61662-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61662-112">-AsJob</span></span>
<span data-ttu-id="61662-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="61662-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61662-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61662-114">-DefaultProfile</span></span>
<span data-ttu-id="61662-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61662-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61662-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61662-116">-ResourceGroupName</span></span>
<span data-ttu-id="61662-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61662-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="61662-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="61662-118">-VMScaleSetName</span></span>
<span data-ttu-id="61662-119">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="61662-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="61662-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61662-120">-Confirm</span></span>
<span data-ttu-id="61662-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61662-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61662-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61662-122">-WhatIf</span></span>
<span data-ttu-id="61662-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61662-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61662-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61662-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61662-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61662-125">CommonParameters</span></span>
<span data-ttu-id="61662-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61662-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61662-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61662-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61662-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61662-128">INPUTS</span></span>

### <span data-ttu-id="61662-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61662-129">System.String</span></span>

## <span data-ttu-id="61662-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61662-130">OUTPUTS</span></span>

### <span data-ttu-id="61662-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="61662-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="61662-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61662-132">NOTES</span></span>

## <span data-ttu-id="61662-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61662-133">RELATED LINKS</span></span>

