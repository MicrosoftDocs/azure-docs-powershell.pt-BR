---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 9d8da69f401f17aa757d5bb5e152f1557ee5356a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609405"
---
# <span data-ttu-id="7beca-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7beca-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="7beca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7beca-102">SYNOPSIS</span></span>
<span data-ttu-id="7beca-103">Obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7beca-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7beca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7beca-104">SYNTAX</span></span>

### <span data-ttu-id="7beca-105">WindowsParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7beca-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7beca-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="7beca-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7beca-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7beca-107">DESCRIPTION</span></span>
<span data-ttu-id="7beca-108">O cmdlet **Get-AzureRmVMBootDiagnosticsData** obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7beca-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="7beca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7beca-109">EXAMPLES</span></span>

### <span data-ttu-id="7beca-110">Exemplo 1: obter dados de diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="7beca-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="7beca-111">Este comando obtém dados de diagnóstico de inicialização para a máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="7beca-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="7beca-112">Esta máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="7beca-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="7beca-113">O comando armazena os dados no caminho local especificado.</span><span class="sxs-lookup"><span data-stu-id="7beca-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="7beca-114">OS</span><span class="sxs-lookup"><span data-stu-id="7beca-114">PARAMETERS</span></span>

### <span data-ttu-id="7beca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7beca-115">-DefaultProfile</span></span>
<span data-ttu-id="7beca-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7beca-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7beca-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="7beca-117">-Linux</span></span>
<span data-ttu-id="7beca-118">Indica que a máquina virtual executa o sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="7beca-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="7beca-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="7beca-119">-LocalPath</span></span>
<span data-ttu-id="7beca-120">Especifica o caminho local para os dados de diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="7beca-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="7beca-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7beca-121">-Name</span></span>
<span data-ttu-id="7beca-122">Especifica o nome da máquina virtual para a qual esse cmdlet obtém dados de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7beca-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="7beca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7beca-123">-ResourceGroupName</span></span>
<span data-ttu-id="7beca-124">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7beca-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7beca-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="7beca-125">-Windows</span></span>
<span data-ttu-id="7beca-126">Indica que a máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="7beca-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="7beca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7beca-127">CommonParameters</span></span>
<span data-ttu-id="7beca-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7beca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7beca-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7beca-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7beca-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7beca-130">INPUTS</span></span>

### <span data-ttu-id="7beca-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7beca-131">System.String</span></span>

## <span data-ttu-id="7beca-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7beca-132">OUTPUTS</span></span>

### <span data-ttu-id="7beca-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7beca-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7beca-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="7beca-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="7beca-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7beca-135">NOTES</span></span>

## <span data-ttu-id="7beca-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7beca-136">RELATED LINKS</span></span>

[<span data-ttu-id="7beca-137">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7beca-137">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


