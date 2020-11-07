---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: 23120c9225d6905a528ac113bd055ec8fa585870
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777038"
---
# <span data-ttu-id="1679c-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1679c-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="1679c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1679c-102">SYNOPSIS</span></span>
<span data-ttu-id="1679c-103">Obtém informações sobre a extensão VMAccess.</span><span class="sxs-lookup"><span data-stu-id="1679c-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="1679c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1679c-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1679c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1679c-105">DESCRIPTION</span></span>
<span data-ttu-id="1679c-106">O cmdlet **Get-AzVMAccessExtension** Obtém informações sobre a extensão da máquina virtual do VMAccess (acesso à máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="1679c-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="1679c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1679c-107">EXAMPLES</span></span>

### <span data-ttu-id="1679c-108">Exemplo 1: obter a extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="1679c-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="1679c-109">Esse comando obtém a extensão VMAccess chamada ContosoTest para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="1679c-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="1679c-110">Exemplo 2: obter o modo de exibição de instância da extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="1679c-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="1679c-111">Esse comando obtém o modo de exibição de instância da extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="1679c-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="1679c-112">OS</span><span class="sxs-lookup"><span data-stu-id="1679c-112">PARAMETERS</span></span>

### <span data-ttu-id="1679c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1679c-113">-DefaultProfile</span></span>
<span data-ttu-id="1679c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1679c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1679c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1679c-115">-Name</span></span>
<span data-ttu-id="1679c-116">Especifica o nome da extensão obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1679c-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1679c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1679c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1679c-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1679c-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1679c-119">-Status</span><span class="sxs-lookup"><span data-stu-id="1679c-119">-Status</span></span>
<span data-ttu-id="1679c-120">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão.</span><span class="sxs-lookup"><span data-stu-id="1679c-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="1679c-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="1679c-121">-VMName</span></span>
<span data-ttu-id="1679c-122">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1679c-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1679c-123">Este cmdlet obtém informações sobre VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1679c-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1679c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1679c-124">CommonParameters</span></span>
<span data-ttu-id="1679c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1679c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1679c-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1679c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1679c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1679c-127">INPUTS</span></span>

### <span data-ttu-id="1679c-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1679c-128">None</span></span>
<span data-ttu-id="1679c-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1679c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1679c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1679c-130">OUTPUTS</span></span>

### <span data-ttu-id="1679c-131">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="1679c-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="1679c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1679c-132">NOTES</span></span>

## <span data-ttu-id="1679c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1679c-133">RELATED LINKS</span></span>

[<span data-ttu-id="1679c-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1679c-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="1679c-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1679c-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="1679c-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1679c-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


