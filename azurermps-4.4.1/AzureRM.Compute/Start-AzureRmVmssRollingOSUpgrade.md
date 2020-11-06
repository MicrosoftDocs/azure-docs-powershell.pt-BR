---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 7f4e28c00b0238b519ad2b038676a295147b5c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432242"
---
# <span data-ttu-id="eb98d-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="eb98d-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="eb98d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb98d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb98d-103">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="eb98d-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb98d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb98d-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb98d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb98d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb98d-106">Inicia uma atualização sem interrupção para mover todas as instâncias do conjunto de escala da máquina virtual para a versão do sistema operacional da plataforma mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="eb98d-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="eb98d-107">Instâncias que já estão executando a versão do sistema operacional mais recente não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="eb98d-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="eb98d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb98d-108">EXAMPLES</span></span>

### <span data-ttu-id="eb98d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb98d-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="eb98d-110">Esse comando inicia uma atualização sem interrupção de todas as instâncias de VM do conjunto de escalas de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="eb98d-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="eb98d-111">OS</span><span class="sxs-lookup"><span data-stu-id="eb98d-111">PARAMETERS</span></span>

### <span data-ttu-id="eb98d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb98d-112">-DefaultProfile</span></span>
<span data-ttu-id="eb98d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb98d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb98d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb98d-114">-ResourceGroupName</span></span>
<span data-ttu-id="eb98d-115">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb98d-115">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb98d-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="eb98d-116">-VMScaleSetName</span></span>
<span data-ttu-id="eb98d-117">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="eb98d-117">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb98d-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eb98d-118">-Confirm</span></span>
<span data-ttu-id="eb98d-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb98d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb98d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb98d-120">-WhatIf</span></span>
<span data-ttu-id="eb98d-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eb98d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb98d-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb98d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb98d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb98d-123">CommonParameters</span></span>
<span data-ttu-id="eb98d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb98d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb98d-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb98d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb98d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb98d-126">INPUTS</span></span>

### <span data-ttu-id="eb98d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="eb98d-127">System.String</span></span>

## <span data-ttu-id="eb98d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb98d-128">OUTPUTS</span></span>

### <span data-ttu-id="eb98d-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="eb98d-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eb98d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb98d-130">NOTES</span></span>

## <span data-ttu-id="eb98d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb98d-131">RELATED LINKS</span></span>

