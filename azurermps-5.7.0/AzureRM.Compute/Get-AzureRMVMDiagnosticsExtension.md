---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430518"
---
# <span data-ttu-id="a4cd1-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4cd1-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a4cd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cd1-103">Obtém as configurações da extensão do diagnóstico em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4cd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4cd1-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="a4cd1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4cd1-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cd1-106">O cmdlet **Get-AzureRmVMDiagnosticsExtension** Obtém as configurações da extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a4cd1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4cd1-107">EXAMPLES</span></span>

### <span data-ttu-id="a4cd1-108">Exemplo 1: obter a extensão do diagnóstico aplicada a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="a4cd1-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="a4cd1-109">Esse comando obtém a extensão de diagnóstico aplicada à máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="a4cd1-110">OS</span><span class="sxs-lookup"><span data-stu-id="a4cd1-110">PARAMETERS</span></span>

### <span data-ttu-id="a4cd1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4cd1-111">-Name</span></span>
<span data-ttu-id="a4cd1-112">Especifica o nome da extensão do diagnóstico para a qual esse cmdlet obtém configurações.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="a4cd1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4cd1-113">-ResourceGroupName</span></span>
<span data-ttu-id="a4cd1-114">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a4cd1-115">-Status</span><span class="sxs-lookup"><span data-stu-id="a4cd1-115">-Status</span></span>
<span data-ttu-id="a4cd1-116">Indica que esse cmdlet usa o valor de status.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-116">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="a4cd1-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="a4cd1-117">-VMName</span></span>
<span data-ttu-id="a4cd1-118">Especifica o nome da máquina virtual a partir da qual esse cmdlet obtém a extensão do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="a4cd1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cd1-119">CommonParameters</span></span>
<span data-ttu-id="a4cd1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cd1-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4cd1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cd1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4cd1-122">INPUTS</span></span>

### <span data-ttu-id="a4cd1-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a4cd1-123">None</span></span>
<span data-ttu-id="a4cd1-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a4cd1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4cd1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4cd1-125">OUTPUTS</span></span>

## <span data-ttu-id="a4cd1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4cd1-126">NOTES</span></span>

## <span data-ttu-id="a4cd1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4cd1-127">RELATED LINKS</span></span>

[<span data-ttu-id="a4cd1-128">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4cd1-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="a4cd1-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4cd1-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


