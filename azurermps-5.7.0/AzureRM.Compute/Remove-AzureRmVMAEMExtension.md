---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429862"
---
# <span data-ttu-id="ac275-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ac275-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="ac275-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac275-102">SYNOPSIS</span></span>
<span data-ttu-id="ac275-103">Remove a extensão do AEM de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ac275-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac275-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac275-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ac275-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac275-105">DESCRIPTION</span></span>
<span data-ttu-id="ac275-106">O cmdlet **Remove-AzureRmVMAEMExtension** remove a extensão do Azure Enhanced Monitoring (AEM) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ac275-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="ac275-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac275-107">EXAMPLES</span></span>

### <span data-ttu-id="ac275-108">Exemplo 1: remover a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="ac275-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ac275-109">Esse comando Remove a extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="ac275-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ac275-110">OS</span><span class="sxs-lookup"><span data-stu-id="ac275-110">PARAMETERS</span></span>

### <span data-ttu-id="ac275-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac275-111">-Name</span></span>
<span data-ttu-id="ac275-112">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="ac275-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac275-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="ac275-113">-OSType</span></span>
<span data-ttu-id="ac275-114">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ac275-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ac275-115">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ac275-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ac275-116">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ac275-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac275-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac275-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac275-118">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ac275-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ac275-119">Esse cmdlet Remove a extensão do AEM da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ac275-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac275-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="ac275-120">-VMName</span></span>
<span data-ttu-id="ac275-121">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ac275-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ac275-122">Esse cmdlet Remove a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ac275-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac275-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac275-123">CommonParameters</span></span>
<span data-ttu-id="ac275-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac275-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac275-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac275-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac275-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac275-126">INPUTS</span></span>

### <span data-ttu-id="ac275-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ac275-127">None</span></span>
<span data-ttu-id="ac275-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ac275-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac275-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac275-129">OUTPUTS</span></span>

## <span data-ttu-id="ac275-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac275-130">NOTES</span></span>

## <span data-ttu-id="ac275-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac275-131">RELATED LINKS</span></span>

[<span data-ttu-id="ac275-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ac275-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ac275-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ac275-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ac275-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ac275-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


