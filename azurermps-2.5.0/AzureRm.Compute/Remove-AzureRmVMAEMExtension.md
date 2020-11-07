---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: cf70191c47f3778268b0087ea542a6812155ebbb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786137"
---
# <span data-ttu-id="ee645-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ee645-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="ee645-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee645-102">SYNOPSIS</span></span>
<span data-ttu-id="ee645-103">Remove a extensão do AEM de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee645-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee645-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee645-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee645-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee645-105">DESCRIPTION</span></span>
<span data-ttu-id="ee645-106">O cmdlet **Remove-AzureRmVMAEMExtension** remove a extensão do Azure Enhanced Monitoring (AEM) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee645-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="ee645-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee645-107">EXAMPLES</span></span>

### <span data-ttu-id="ee645-108">Exemplo 1: remover a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="ee645-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ee645-109">Esse comando Remove a extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="ee645-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ee645-110">OS</span><span class="sxs-lookup"><span data-stu-id="ee645-110">PARAMETERS</span></span>

### <span data-ttu-id="ee645-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee645-111">-DefaultProfile</span></span>
<span data-ttu-id="ee645-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee645-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee645-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee645-113">-Name</span></span>
<span data-ttu-id="ee645-114">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="ee645-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="ee645-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="ee645-115">-OSType</span></span>
<span data-ttu-id="ee645-116">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ee645-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ee645-117">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ee645-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ee645-118">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ee645-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="ee645-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee645-119">-ResourceGroupName</span></span>
<span data-ttu-id="ee645-120">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee645-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ee645-121">Esse cmdlet Remove a extensão do AEM da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee645-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="ee645-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="ee645-122">-VMName</span></span>
<span data-ttu-id="ee645-123">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee645-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ee645-124">Esse cmdlet Remove a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ee645-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee645-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee645-125">CommonParameters</span></span>
<span data-ttu-id="ee645-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee645-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee645-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee645-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee645-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee645-128">INPUTS</span></span>

### <span data-ttu-id="ee645-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ee645-129">None</span></span>
<span data-ttu-id="ee645-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ee645-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee645-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee645-131">OUTPUTS</span></span>

### <span data-ttu-id="ee645-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ee645-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ee645-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee645-133">NOTES</span></span>

## <span data-ttu-id="ee645-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee645-134">RELATED LINKS</span></span>

[<span data-ttu-id="ee645-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ee645-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ee645-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ee645-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ee645-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ee645-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


