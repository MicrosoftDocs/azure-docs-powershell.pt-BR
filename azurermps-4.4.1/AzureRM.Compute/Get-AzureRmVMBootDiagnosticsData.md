---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: dfe9324644115d00054961e8e159c672d1aba588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441583"
---
# <span data-ttu-id="45812-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="45812-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="45812-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45812-102">SYNOPSIS</span></span>
<span data-ttu-id="45812-103">Obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="45812-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45812-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45812-104">SYNTAX</span></span>

### <span data-ttu-id="45812-105">WindowsParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="45812-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45812-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="45812-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45812-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45812-107">DESCRIPTION</span></span>
<span data-ttu-id="45812-108">O cmdlet **Get-AzureRmVMBootDiagnosticsData** obtém dados de diagnóstico de inicialização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="45812-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="45812-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45812-109">EXAMPLES</span></span>

### <span data-ttu-id="45812-110">Exemplo 1: obter dados de diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="45812-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="45812-111">Este comando obtém dados de diagnóstico de inicialização para a máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="45812-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="45812-112">Esta máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="45812-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="45812-113">O comando armazena os dados no caminho local especificado.</span><span class="sxs-lookup"><span data-stu-id="45812-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="45812-114">OS</span><span class="sxs-lookup"><span data-stu-id="45812-114">PARAMETERS</span></span>

### <span data-ttu-id="45812-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45812-115">-DefaultProfile</span></span>
<span data-ttu-id="45812-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45812-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45812-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="45812-117">-Linux</span></span>
<span data-ttu-id="45812-118">Indica que a máquina virtual executa o sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="45812-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="45812-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="45812-119">-LocalPath</span></span>
<span data-ttu-id="45812-120">Especifica o caminho local para os dados de diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="45812-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="45812-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="45812-121">-Name</span></span>
<span data-ttu-id="45812-122">Especifica o nome da máquina virtual para a qual esse cmdlet obtém dados de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="45812-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="45812-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45812-123">-ResourceGroupName</span></span>
<span data-ttu-id="45812-124">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="45812-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="45812-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="45812-125">-Windows</span></span>
<span data-ttu-id="45812-126">Indica que a máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="45812-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="45812-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45812-127">CommonParameters</span></span>
<span data-ttu-id="45812-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45812-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45812-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45812-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45812-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45812-130">INPUTS</span></span>

## <span data-ttu-id="45812-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45812-131">OUTPUTS</span></span>

## <span data-ttu-id="45812-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45812-132">NOTES</span></span>

## <span data-ttu-id="45812-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45812-133">RELATED LINKS</span></span>

[<span data-ttu-id="45812-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="45812-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


