---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: f87399901e00e19686d879799dbb799c7d79172c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441151"
---
# <span data-ttu-id="f9b4d-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f9b4d-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="f9b4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b4d-103">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9b4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9b4d-104">SYNTAX</span></span>

### <span data-ttu-id="f9b4d-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9b4d-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b4d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f9b4d-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9b4d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9b4d-107">DESCRIPTION</span></span>
<span data-ttu-id="f9b4d-108">Cancela a atualização sem interrupção da configuração da máquina virtual atual.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f9b4d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9b4d-109">EXAMPLES</span></span>

### <span data-ttu-id="f9b4d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9b4d-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f9b4d-111">Esse comando cancela a atualização em andamento do conjunto de dimensionamento de VM "VMSS001" no grupo de recursos "Group001".</span><span class="sxs-lookup"><span data-stu-id="f9b4d-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="f9b4d-112">OS</span><span class="sxs-lookup"><span data-stu-id="f9b4d-112">PARAMETERS</span></span>

### <span data-ttu-id="f9b4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b4d-113">-DefaultProfile</span></span>
<span data-ttu-id="f9b4d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9b4d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f9b4d-115">-Force</span></span>
<span data-ttu-id="f9b4d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9b4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9b4d-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b4d-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f9b4d-119">-VMScaleSetName</span></span>
<span data-ttu-id="f9b4d-120">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b4d-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9b4d-121">-Confirm</span></span>
<span data-ttu-id="f9b4d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b4d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b4d-123">-WhatIf</span></span>
<span data-ttu-id="f9b4d-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b4d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b4d-126">CommonParameters</span></span>
<span data-ttu-id="f9b4d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b4d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9b4d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b4d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9b4d-129">INPUTS</span></span>

### <span data-ttu-id="f9b4d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f9b4d-130">System.String</span></span>

## <span data-ttu-id="f9b4d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9b4d-131">OUTPUTS</span></span>

### <span data-ttu-id="f9b4d-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f9b4d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f9b4d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9b4d-133">NOTES</span></span>

## <span data-ttu-id="f9b4d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9b4d-134">RELATED LINKS</span></span>

