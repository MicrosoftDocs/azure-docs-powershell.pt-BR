---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434352"
---
# <span data-ttu-id="76401-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="76401-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="76401-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76401-102">SYNOPSIS</span></span>
<span data-ttu-id="76401-103">Obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="76401-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="76401-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76401-104">SYNTAX</span></span>

### <span data-ttu-id="76401-105">WindowsParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="76401-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76401-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="76401-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76401-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76401-107">DESCRIPTION</span></span>
<span data-ttu-id="76401-108">O cmdlet **Get-AzVMBootDiagnosticsData** obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="76401-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="76401-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76401-109">EXAMPLES</span></span>

### <span data-ttu-id="76401-110">Exemplo 1: obter dados de diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="76401-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="76401-111">Este comando obtém dados de diagnóstico de inicialização para a máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="76401-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="76401-112">Esta máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="76401-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="76401-113">O comando armazena os dados no caminho local especificado.</span><span class="sxs-lookup"><span data-stu-id="76401-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="76401-114">OS</span><span class="sxs-lookup"><span data-stu-id="76401-114">PARAMETERS</span></span>

### <span data-ttu-id="76401-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76401-115">-DefaultProfile</span></span>
<span data-ttu-id="76401-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76401-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76401-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="76401-117">-Linux</span></span>
<span data-ttu-id="76401-118">Indica que a máquina virtual executa o sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="76401-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76401-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="76401-119">-LocalPath</span></span>
<span data-ttu-id="76401-120">Especifica o caminho local para os dados de diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="76401-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76401-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="76401-121">-Name</span></span>
<span data-ttu-id="76401-122">Especifica o nome da máquina virtual para a qual esse cmdlet obtém dados de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="76401-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76401-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76401-123">-ResourceGroupName</span></span>
<span data-ttu-id="76401-124">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="76401-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="76401-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="76401-125">-Windows</span></span>
<span data-ttu-id="76401-126">Indica que a máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="76401-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76401-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76401-127">CommonParameters</span></span>
<span data-ttu-id="76401-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76401-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76401-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76401-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76401-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76401-130">INPUTS</span></span>

### <span data-ttu-id="76401-131">System. String</span><span class="sxs-lookup"><span data-stu-id="76401-131">System.String</span></span>

## <span data-ttu-id="76401-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76401-132">OUTPUTS</span></span>

### <span data-ttu-id="76401-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="76401-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="76401-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="76401-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="76401-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76401-135">NOTES</span></span>

## <span data-ttu-id="76401-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76401-136">RELATED LINKS</span></span>

[<span data-ttu-id="76401-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76401-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


