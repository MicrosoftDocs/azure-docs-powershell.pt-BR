---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427634"
---
# <span data-ttu-id="d9422-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d9422-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="d9422-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9422-102">SYNOPSIS</span></span>
<span data-ttu-id="d9422-103">Obtém as configurações da extensão DSC em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9422-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9422-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9422-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="d9422-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9422-105">DESCRIPTION</span></span>
<span data-ttu-id="d9422-106">O cmdlet **Get-AzureRmVMDscExtension** Obtém as configurações da extensão da configuração de estado desejada (DSC) em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9422-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="d9422-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9422-107">EXAMPLES</span></span>

### <span data-ttu-id="d9422-108">Exemplo 1: obter as configurações de uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="d9422-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="d9422-109">Esse comando obtém as configurações de extensão nomeada como DSC na máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="d9422-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="d9422-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9422-110">PARAMETERS</span></span>

### <span data-ttu-id="d9422-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9422-111">-Name</span></span>
<span data-ttu-id="d9422-112">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="d9422-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d9422-113">O cmdlet Set-AzureRmVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o mesmo valor que é usado pelo **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="d9422-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="d9422-114">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet **set-AzureRmVMDscExtension** ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9422-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9422-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9422-115">-ResourceGroupName</span></span>
<span data-ttu-id="d9422-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9422-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d9422-117">-Status</span><span class="sxs-lookup"><span data-stu-id="d9422-117">-Status</span></span>
<span data-ttu-id="d9422-118">Indica que esse cmdlet obtém o modo de exibição de instância da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="d9422-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9422-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="d9422-119">-VMName</span></span>
<span data-ttu-id="d9422-120">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="d9422-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9422-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9422-121">CommonParameters</span></span>
<span data-ttu-id="d9422-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9422-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9422-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9422-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9422-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9422-124">INPUTS</span></span>

### <span data-ttu-id="d9422-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d9422-125">None</span></span>
<span data-ttu-id="d9422-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d9422-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9422-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9422-127">OUTPUTS</span></span>

### <span data-ttu-id="d9422-128">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d9422-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="d9422-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9422-129">NOTES</span></span>

## <span data-ttu-id="d9422-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9422-130">RELATED LINKS</span></span>

[<span data-ttu-id="d9422-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d9422-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="d9422-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d9422-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


