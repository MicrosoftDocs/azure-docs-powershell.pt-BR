---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602386"
---
# <span data-ttu-id="99f66-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="99f66-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="99f66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99f66-102">SYNOPSIS</span></span>
<span data-ttu-id="99f66-103">Obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99f66-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99f66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99f66-104">SYNTAX</span></span>

### <span data-ttu-id="99f66-105">WindowsParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="99f66-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="99f66-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="99f66-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="99f66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99f66-107">DESCRIPTION</span></span>
<span data-ttu-id="99f66-108">O cmdlet **Get-AzureRmVMBootDiagnosticsData** obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99f66-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="99f66-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99f66-109">EXAMPLES</span></span>

### <span data-ttu-id="99f66-110">Exemplo 1: obter dados de diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="99f66-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="99f66-111">Este comando obtém dados de diagnóstico de inicialização para a máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="99f66-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="99f66-112">Esta máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="99f66-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="99f66-113">O comando armazena os dados no caminho local especificado.</span><span class="sxs-lookup"><span data-stu-id="99f66-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="99f66-114">OS</span><span class="sxs-lookup"><span data-stu-id="99f66-114">PARAMETERS</span></span>

### <span data-ttu-id="99f66-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="99f66-115">-Linux</span></span>
<span data-ttu-id="99f66-116">Indica que a máquina virtual executa o sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="99f66-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f66-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="99f66-117">-LocalPath</span></span>
<span data-ttu-id="99f66-118">Especifica o caminho local para os dados de diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="99f66-118">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99f66-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="99f66-119">-Name</span></span>
<span data-ttu-id="99f66-120">Especifica o nome da máquina virtual para a qual esse cmdlet obtém dados de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="99f66-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99f66-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f66-121">-ResourceGroupName</span></span>
<span data-ttu-id="99f66-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99f66-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="99f66-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="99f66-123">-Windows</span></span>
<span data-ttu-id="99f66-124">Indica que a máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="99f66-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f66-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f66-125">CommonParameters</span></span>
<span data-ttu-id="99f66-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f66-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f66-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f66-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f66-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99f66-128">INPUTS</span></span>

### <span data-ttu-id="99f66-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="99f66-129">None</span></span>
<span data-ttu-id="99f66-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="99f66-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99f66-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99f66-131">OUTPUTS</span></span>

## <span data-ttu-id="99f66-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99f66-132">NOTES</span></span>

## <span data-ttu-id="99f66-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99f66-133">RELATED LINKS</span></span>

[<span data-ttu-id="99f66-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="99f66-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


