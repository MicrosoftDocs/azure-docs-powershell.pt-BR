---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 5efda3a73cc94d2e196b5817d5b3c1e507192da0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777041"
---
# <span data-ttu-id="99784-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="99784-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="99784-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99784-102">SYNOPSIS</span></span>
<span data-ttu-id="99784-103">Obtém informações sobre a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="99784-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="99784-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99784-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99784-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99784-105">DESCRIPTION</span></span>
<span data-ttu-id="99784-106">O cmdlet **Get-AzVMAEMExtension** Obtém informações sobre a extensão do Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="99784-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="99784-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99784-107">EXAMPLES</span></span>

### <span data-ttu-id="99784-108">Exemplo 1: obter a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="99784-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="99784-109">Esse comando obtém informações para a extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="99784-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="99784-110">OS</span><span class="sxs-lookup"><span data-stu-id="99784-110">PARAMETERS</span></span>

### <span data-ttu-id="99784-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99784-111">-DefaultProfile</span></span>
<span data-ttu-id="99784-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99784-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99784-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="99784-113">-Name</span></span>
<span data-ttu-id="99784-114">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99784-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="99784-115">Esse cmdlet obtém informações para a extensão do AEM na máquina virtual que esse cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="99784-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="99784-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="99784-116">-OSType</span></span>
<span data-ttu-id="99784-117">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="99784-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="99784-118">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="99784-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="99784-119">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="99784-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="99784-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99784-120">-ResourceGroupName</span></span>
<span data-ttu-id="99784-121">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99784-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="99784-122">Este cmdlet obtém informações para a extensão do AEM nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99784-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="99784-123">-Status</span><span class="sxs-lookup"><span data-stu-id="99784-123">-Status</span></span>
<span data-ttu-id="99784-124">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="99784-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="99784-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="99784-125">-VMName</span></span>
<span data-ttu-id="99784-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99784-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="99784-127">Este cmdlet obtém informações sobre a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="99784-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="99784-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99784-128">CommonParameters</span></span>
<span data-ttu-id="99784-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99784-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99784-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99784-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99784-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99784-131">INPUTS</span></span>

### <span data-ttu-id="99784-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="99784-132">None</span></span>
<span data-ttu-id="99784-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="99784-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99784-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99784-134">OUTPUTS</span></span>

### <span data-ttu-id="99784-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="99784-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="99784-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99784-136">NOTES</span></span>

## <span data-ttu-id="99784-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99784-137">RELATED LINKS</span></span>

[<span data-ttu-id="99784-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="99784-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="99784-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="99784-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="99784-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="99784-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


