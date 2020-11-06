---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: d06e2ca5ed51b89b78999c1e146ca75805c8a674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432650"
---
# <span data-ttu-id="770b6-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="770b6-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="770b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="770b6-102">SYNOPSIS</span></span>
<span data-ttu-id="770b6-103">Obtém informações sobre uma extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="770b6-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="770b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="770b6-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="770b6-105">DESCRIPTION</span></span>
<span data-ttu-id="770b6-106">O cmdlet **Get-AzureRmVMCustomScriptExtension** Obtém informações sobre uma extensão de máquina virtual de script personalizado em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="770b6-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="770b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="770b6-107">EXAMPLES</span></span>

### <span data-ttu-id="770b6-108">Exemplo 1: obter uma extensão de script personalizada</span><span class="sxs-lookup"><span data-stu-id="770b6-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="770b6-109">Esse comando obtém a extensão de script personalizada chamada ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="770b6-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="770b6-110">Exemplo 2: obter o modo de exibição de instância de uma extensão de script personalizado</span><span class="sxs-lookup"><span data-stu-id="770b6-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="770b6-111">Este comando obtém o modo de exibição de instância da extensão de script personalizado chamado ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="770b6-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="770b6-112">OS</span><span class="sxs-lookup"><span data-stu-id="770b6-112">PARAMETERS</span></span>

### <span data-ttu-id="770b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770b6-113">-DefaultProfile</span></span>
<span data-ttu-id="770b6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="770b6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="770b6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="770b6-115">-Name</span></span>
<span data-ttu-id="770b6-116">Especifica o nome da extensão de script personalizada sobre a qual esse cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="770b6-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="770b6-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="770b6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="770b6-119">-Status</span><span class="sxs-lookup"><span data-stu-id="770b6-119">-Status</span></span>
<span data-ttu-id="770b6-120">Indica que esse cmdlet obtém o modo de exibição de instância da extensão de script personalizado.</span><span class="sxs-lookup"><span data-stu-id="770b6-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="770b6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="770b6-121">-VMName</span></span>
<span data-ttu-id="770b6-122">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém a extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="770b6-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="770b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770b6-123">CommonParameters</span></span>
<span data-ttu-id="770b6-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770b6-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770b6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770b6-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="770b6-126">INPUTS</span></span>

## <span data-ttu-id="770b6-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="770b6-127">OUTPUTS</span></span>

## <span data-ttu-id="770b6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="770b6-128">NOTES</span></span>

## <span data-ttu-id="770b6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="770b6-129">RELATED LINKS</span></span>

[<span data-ttu-id="770b6-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="770b6-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="770b6-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="770b6-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="770b6-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="770b6-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


