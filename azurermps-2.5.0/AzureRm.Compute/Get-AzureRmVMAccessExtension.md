---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785554"
---
# <span data-ttu-id="555c6-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="555c6-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="555c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="555c6-102">SYNOPSIS</span></span>
<span data-ttu-id="555c6-103">Obtém informações sobre a extensão VMAccess.</span><span class="sxs-lookup"><span data-stu-id="555c6-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="555c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="555c6-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="555c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="555c6-105">DESCRIPTION</span></span>
<span data-ttu-id="555c6-106">O cmdlet **Get-AzureRmVMAccessExtension** Obtém informações sobre a extensão da máquina virtual do VMAccess (acesso à máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="555c6-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="555c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="555c6-107">EXAMPLES</span></span>

### <span data-ttu-id="555c6-108">Exemplo 1: obter a extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="555c6-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="555c6-109">Esse comando obtém a extensão VMAccess chamada ContosoTest para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="555c6-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="555c6-110">Exemplo 2: obter o modo de exibição de instância da extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="555c6-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="555c6-111">Esse comando obtém o modo de exibição de instância da extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="555c6-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="555c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="555c6-112">PARAMETERS</span></span>

### <span data-ttu-id="555c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555c6-113">-DefaultProfile</span></span>
<span data-ttu-id="555c6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="555c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="555c6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="555c6-115">-Name</span></span>
<span data-ttu-id="555c6-116">Especifica o nome da extensão obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="555c6-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="555c6-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="555c6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="555c6-119">-Status</span><span class="sxs-lookup"><span data-stu-id="555c6-119">-Status</span></span>
<span data-ttu-id="555c6-120">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão.</span><span class="sxs-lookup"><span data-stu-id="555c6-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="555c6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="555c6-121">-VMName</span></span>
<span data-ttu-id="555c6-122">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="555c6-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="555c6-123">Este cmdlet obtém informações sobre VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="555c6-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="555c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555c6-124">CommonParameters</span></span>
<span data-ttu-id="555c6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555c6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555c6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555c6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="555c6-127">INPUTS</span></span>

### <span data-ttu-id="555c6-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="555c6-128">None</span></span>
<span data-ttu-id="555c6-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="555c6-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="555c6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="555c6-130">OUTPUTS</span></span>

### <span data-ttu-id="555c6-131">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="555c6-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="555c6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="555c6-132">NOTES</span></span>

## <span data-ttu-id="555c6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="555c6-133">RELATED LINKS</span></span>

[<span data-ttu-id="555c6-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="555c6-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="555c6-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="555c6-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="555c6-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="555c6-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


