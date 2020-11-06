---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610424"
---
# <span data-ttu-id="d93ed-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d93ed-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="d93ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d93ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d93ed-103">Obtém informações sobre a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="d93ed-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d93ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d93ed-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d93ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d93ed-105">DESCRIPTION</span></span>
<span data-ttu-id="d93ed-106">O cmdlet **Get-AzureRmVMAEMExtension** Obtém informações sobre a extensão do Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="d93ed-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="d93ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d93ed-107">EXAMPLES</span></span>

### <span data-ttu-id="d93ed-108">Exemplo 1: obter a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="d93ed-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="d93ed-109">Esse comando obtém informações para a extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="d93ed-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="d93ed-110">OS</span><span class="sxs-lookup"><span data-stu-id="d93ed-110">PARAMETERS</span></span>

### <span data-ttu-id="d93ed-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d93ed-111">-Name</span></span>
<span data-ttu-id="d93ed-112">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d93ed-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d93ed-113">Esse cmdlet obtém informações para a extensão do AEM na máquina virtual que esse cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="d93ed-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="d93ed-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="d93ed-114">-OSType</span></span>
<span data-ttu-id="d93ed-115">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d93ed-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d93ed-116">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d93ed-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d93ed-117">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="d93ed-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93ed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93ed-118">-ResourceGroupName</span></span>
<span data-ttu-id="d93ed-119">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d93ed-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="d93ed-120">Este cmdlet obtém informações para a extensão do AEM nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d93ed-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="d93ed-121">-Status</span><span class="sxs-lookup"><span data-stu-id="d93ed-121">-Status</span></span>
<span data-ttu-id="d93ed-122">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="d93ed-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d93ed-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="d93ed-123">-VMName</span></span>
<span data-ttu-id="d93ed-124">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d93ed-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d93ed-125">Este cmdlet obtém informações sobre a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d93ed-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d93ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93ed-126">CommonParameters</span></span>
<span data-ttu-id="d93ed-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d93ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93ed-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d93ed-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93ed-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d93ed-129">INPUTS</span></span>

### <span data-ttu-id="d93ed-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d93ed-130">None</span></span>
<span data-ttu-id="d93ed-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d93ed-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d93ed-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d93ed-132">OUTPUTS</span></span>

## <span data-ttu-id="d93ed-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d93ed-133">NOTES</span></span>

## <span data-ttu-id="d93ed-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d93ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="d93ed-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d93ed-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="d93ed-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d93ed-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="d93ed-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d93ed-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


