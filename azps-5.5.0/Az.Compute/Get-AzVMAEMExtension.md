---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 0879458284c7e08b2e8371b9b8d8b894a482a9df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112144"
---
# <span data-ttu-id="87e21-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="87e21-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="87e21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87e21-102">SYNOPSIS</span></span>
<span data-ttu-id="87e21-103">Obtém informações sobre a extensão AEM.</span><span class="sxs-lookup"><span data-stu-id="87e21-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="87e21-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87e21-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e21-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="87e21-105">DESCRIPTION</span></span>
<span data-ttu-id="87e21-106">O cmdlet **Get-AzVMAEMExtension obtém** informações sobre a extensão Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="87e21-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="87e21-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87e21-107">EXAMPLES</span></span>

### <span data-ttu-id="87e21-108">Exemplo 1: Obter a extensão AEM</span><span class="sxs-lookup"><span data-stu-id="87e21-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="87e21-109">Esse comando obtém informações sobre a extensão AEM da máquina virtual chamada contoso-server.</span><span class="sxs-lookup"><span data-stu-id="87e21-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="87e21-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87e21-110">PARAMETERS</span></span>

### <span data-ttu-id="87e21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e21-111">-DefaultProfile</span></span>
<span data-ttu-id="87e21-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="87e21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e21-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="87e21-113">-Name</span></span>
<span data-ttu-id="87e21-114">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87e21-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="87e21-115">Este cmdlet obtém informações sobre a extensão AEM na máquina virtual especificada por este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87e21-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e21-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="87e21-116">-OSType</span></span>
<span data-ttu-id="87e21-117">Especifica o tipo do sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="87e21-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="87e21-118">Se o disco do sistema operacional não tiver um tipo, você deverá especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87e21-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="87e21-119">Os valores aceitáveis para este parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="87e21-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e21-120">-ResourceGroupName</span></span>
<span data-ttu-id="87e21-121">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87e21-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="87e21-122">Este cmdlet obtém informações sobre a extensão AEM nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87e21-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e21-123">-Status</span><span class="sxs-lookup"><span data-stu-id="87e21-123">-Status</span></span>
<span data-ttu-id="87e21-124">Indica que esse cmdlet obtém apenas a exibição de instância da extensão AEM.</span><span class="sxs-lookup"><span data-stu-id="87e21-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e21-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="87e21-125">-VMName</span></span>
<span data-ttu-id="87e21-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87e21-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="87e21-127">Este cmdlet obtém informações sobre a extensão AEM para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87e21-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e21-128">CommonParameters</span></span>
<span data-ttu-id="87e21-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e21-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87e21-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e21-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="87e21-131">INPUTS</span></span>

### <span data-ttu-id="87e21-132">System.String</span><span class="sxs-lookup"><span data-stu-id="87e21-132">System.String</span></span>

### <span data-ttu-id="87e21-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87e21-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87e21-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="87e21-134">OUTPUTS</span></span>

### <span data-ttu-id="87e21-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="87e21-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="87e21-136">Notas</span><span class="sxs-lookup"><span data-stu-id="87e21-136">NOTES</span></span>

## <span data-ttu-id="87e21-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87e21-137">RELATED LINKS</span></span>

[<span data-ttu-id="87e21-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="87e21-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="87e21-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="87e21-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="87e21-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="87e21-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


