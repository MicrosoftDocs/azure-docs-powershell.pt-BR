---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426773"
---
# <span data-ttu-id="4a3c6-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4a3c6-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="4a3c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3c6-103">Verifica a configuração da extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a3c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a3c6-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="4a3c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a3c6-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3c6-106">O cmdlet **Test-AzureRmVMAEMExtension** verifica a configuração da extensão do Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="4a3c6-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="4a3c6-107">A extensão do AEM coleta os dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="4a3c6-108">Este cmdlet verifica se os dados de desempenho estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="4a3c6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-109">EXAMPLES</span></span>

### <span data-ttu-id="4a3c6-110">Exemplo 1: verificar a configuração da extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="4a3c6-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="4a3c6-111">Esse comando verifica a configuração da extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="4a3c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-112">PARAMETERS</span></span>

### <span data-ttu-id="4a3c6-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="4a3c6-113">-OSType</span></span>
<span data-ttu-id="4a3c6-114">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="4a3c6-115">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="4a3c6-116">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a3c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a3c6-118">Especifica o nome do grupo de recursos da máquina virtual que este cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="4a3c6-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="4a3c6-119">-SkipStorageCheck</span></span>
<span data-ttu-id="4a3c6-120">Indica que esse cmdlet ignora a verificação de configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="4a3c6-121">-VMName</span></span>
<span data-ttu-id="4a3c6-122">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4a3c6-123">Esse cmdlet testa a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a3c6-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="4a3c6-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="4a3c6-125">Especifica um período de tempo limite, em minutos, para a verificação da configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3c6-126">CommonParameters</span></span>
<span data-ttu-id="4a3c6-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3c6-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a3c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3c6-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a3c6-129">INPUTS</span></span>

### <span data-ttu-id="4a3c6-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4a3c6-130">None</span></span>
<span data-ttu-id="4a3c6-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a3c6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a3c6-132">OUTPUTS</span></span>

## <span data-ttu-id="4a3c6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a3c6-133">NOTES</span></span>

## <span data-ttu-id="4a3c6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a3c6-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4a3c6-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4a3c6-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4a3c6-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4a3c6-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4a3c6-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


