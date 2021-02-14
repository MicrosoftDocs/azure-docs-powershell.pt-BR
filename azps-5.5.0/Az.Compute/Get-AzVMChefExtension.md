---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111148"
---
# <span data-ttu-id="0d00b-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0d00b-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="0d00b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d00b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d00b-103">Obtém informações sobre uma extensão Deeira.</span><span class="sxs-lookup"><span data-stu-id="0d00b-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="0d00b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d00b-104">SYNTAX</span></span>

### <span data-ttu-id="0d00b-105">Linux</span><span class="sxs-lookup"><span data-stu-id="0d00b-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d00b-106">Windows</span><span class="sxs-lookup"><span data-stu-id="0d00b-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d00b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d00b-107">DESCRIPTION</span></span>
<span data-ttu-id="0d00b-108">O cmdlet **Get-AzVM Eletension obtém** informações sobre uma extensão Desarmada instalada em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0d00b-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="0d00b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d00b-109">EXAMPLES</span></span>

### <span data-ttu-id="0d00b-110">Exemplo 1: Obter os detalhes da extensão Dera para uma máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="0d00b-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="0d00b-111">Esse comando obtém a extensão De uma máquina virtual do Windows chamada WindowsVM001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="0d00b-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0d00b-112">Exemplo 2: Obter os detalhes da extensão Dera para uma máquina virtual do Linux</span><span class="sxs-lookup"><span data-stu-id="0d00b-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="0d00b-113">Esse comando obtém a extensão De uma máquina virtual linux chamada LinuxVM001 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="0d00b-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0d00b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d00b-114">PARAMETERS</span></span>

### <span data-ttu-id="0d00b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d00b-115">-DefaultProfile</span></span>
<span data-ttu-id="0d00b-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0d00b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d00b-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0d00b-117">-Linux</span></span>
<span data-ttu-id="0d00b-118">Indica que esse cmdlet funciona em uma máquina virtual do Linux.</span><span class="sxs-lookup"><span data-stu-id="0d00b-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d00b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d00b-119">-Name</span></span>
<span data-ttu-id="0d00b-120">Especifica o nome da extensão Deeira.</span><span class="sxs-lookup"><span data-stu-id="0d00b-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="0d00b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d00b-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d00b-122">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0d00b-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="0d00b-123">-Status</span><span class="sxs-lookup"><span data-stu-id="0d00b-123">-Status</span></span>
<span data-ttu-id="0d00b-124">Indica que esse cmdlet obtém apenas a exibição de instância da extensão Descarros.</span><span class="sxs-lookup"><span data-stu-id="0d00b-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="0d00b-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="0d00b-125">-VMName</span></span>
<span data-ttu-id="0d00b-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0d00b-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="0d00b-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="0d00b-127">-Windows</span></span>
<span data-ttu-id="0d00b-128">Indica que esse cmdlet é para uma máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="0d00b-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d00b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d00b-129">CommonParameters</span></span>
<span data-ttu-id="0d00b-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d00b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d00b-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d00b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d00b-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d00b-132">INPUTS</span></span>

### <span data-ttu-id="0d00b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0d00b-133">System.String</span></span>

### <span data-ttu-id="0d00b-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0d00b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0d00b-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d00b-135">OUTPUTS</span></span>

### <span data-ttu-id="0d00b-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0d00b-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="0d00b-137">Notas</span><span class="sxs-lookup"><span data-stu-id="0d00b-137">NOTES</span></span>

## <span data-ttu-id="0d00b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d00b-138">RELATED LINKS</span></span>

[<span data-ttu-id="0d00b-139">Set-AzVM Eletension</span><span class="sxs-lookup"><span data-stu-id="0d00b-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="0d00b-140">Remove-AzVM Eletension</span><span class="sxs-lookup"><span data-stu-id="0d00b-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


