---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426924"
---
# <span data-ttu-id="c3bbc-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="c3bbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bbc-103">Define ações específicas em um VMSS especificado.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3bbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3bbc-104">SYNTAX</span></span>

### <span data-ttu-id="c3bbc-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3bbc-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3bbc-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c3bbc-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3bbc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="c3bbc-108">O cmdlet **set-AzureRmVmss** define ações específicas no conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c3bbc-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c3bbc-109">A única ação aceita por este cmdlet é a reimagem.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="c3bbc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3bbc-110">EXAMPLES</span></span>

### <span data-ttu-id="c3bbc-111">Exemplo 1: reimagem de um VMSS</span><span class="sxs-lookup"><span data-stu-id="c3bbc-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c3bbc-112">Esse comando faz a nova imagem do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="c3bbc-113">OS</span><span class="sxs-lookup"><span data-stu-id="c3bbc-113">PARAMETERS</span></span>

### <span data-ttu-id="c3bbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3bbc-114">-DefaultProfile</span></span>
<span data-ttu-id="c3bbc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3bbc-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c3bbc-116">-InstanceId</span></span>
<span data-ttu-id="c3bbc-117">A ID de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-117">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3bbc-118">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="c3bbc-118">-Reimage</span></span>
<span data-ttu-id="c3bbc-119">Indica que o cmdlet reimagemia o VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-119">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bbc-120">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="c3bbc-120">-ReimageAll</span></span>
<span data-ttu-id="c3bbc-121">Indica que o cmdlet reimagemia todos os discos no VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bbc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3bbc-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3bbc-123">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-123">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c3bbc-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c3bbc-124">-VMScaleSetName</span></span>
<span data-ttu-id="c3bbc-125">Especifica o nome do VMSS para o qual esse cmdlet define ações.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="c3bbc-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3bbc-126">-Confirm</span></span>
<span data-ttu-id="c3bbc-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3bbc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3bbc-128">-WhatIf</span></span>
<span data-ttu-id="c3bbc-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3bbc-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3bbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3bbc-131">CommonParameters</span></span>
<span data-ttu-id="c3bbc-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3bbc-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3bbc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3bbc-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3bbc-134">INPUTS</span></span>

## <span data-ttu-id="c3bbc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3bbc-135">OUTPUTS</span></span>

### <span data-ttu-id="c3bbc-136">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c3bbc-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c3bbc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3bbc-137">NOTES</span></span>

## <span data-ttu-id="c3bbc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3bbc-138">RELATED LINKS</span></span>

[<span data-ttu-id="c3bbc-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c3bbc-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c3bbc-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c3bbc-142">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c3bbc-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c3bbc-144">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c3bbc-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3bbc-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


