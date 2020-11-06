---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 32f5973668ca03dedb22b05186eda83002167648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426932"
---
# <span data-ttu-id="295e3-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="295e3-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="295e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="295e3-102">SYNOPSIS</span></span>
<span data-ttu-id="295e3-103">Modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="295e3-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="295e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="295e3-104">SYNTAX</span></span>

### <span data-ttu-id="295e3-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="295e3-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="295e3-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="295e3-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="295e3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="295e3-107">DESCRIPTION</span></span>
<span data-ttu-id="295e3-108">O cmdlet **set-AzureRmVMBootDiagnostics** modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="295e3-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="295e3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="295e3-109">EXAMPLES</span></span>

### <span data-ttu-id="295e3-110">Exemplo 1: habilitar o diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="295e3-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="295e3-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="295e3-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="295e3-112">O comando o armazena na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="295e3-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="295e3-113">O segundo comando habilita o diagnóstico de inicialização para a máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="295e3-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="295e3-114">Os dados de diagnóstico são armazenados na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="295e3-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="295e3-115">OS</span><span class="sxs-lookup"><span data-stu-id="295e3-115">PARAMETERS</span></span>

### <span data-ttu-id="295e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295e3-116">-DefaultProfile</span></span>
<span data-ttu-id="295e3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="295e3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="295e3-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="295e3-118">-Disable</span></span>
<span data-ttu-id="295e3-119">Indica que esse cmdlet desabilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="295e3-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e3-120">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="295e3-120">-Enable</span></span>
<span data-ttu-id="295e3-121">Indica que esse cmdlet habilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="295e3-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="295e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="295e3-123">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="295e3-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295e3-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="295e3-124">-StorageAccountName</span></span>
<span data-ttu-id="295e3-125">Especifica o nome da conta de armazenamento na qual os dados de diagnóstico de inicialização são salvos.</span><span class="sxs-lookup"><span data-stu-id="295e3-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295e3-126">-VM</span><span class="sxs-lookup"><span data-stu-id="295e3-126">-VM</span></span>
<span data-ttu-id="295e3-127">Especifica a máquina virtual para a qual esse cmdlet altera o diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="295e3-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="295e3-128">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="295e3-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="295e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295e3-129">CommonParameters</span></span>
<span data-ttu-id="295e3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="295e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295e3-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="295e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295e3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="295e3-132">INPUTS</span></span>

## <span data-ttu-id="295e3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="295e3-133">OUTPUTS</span></span>

## <span data-ttu-id="295e3-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="295e3-134">NOTES</span></span>

## <span data-ttu-id="295e3-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="295e3-135">RELATED LINKS</span></span>

[<span data-ttu-id="295e3-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="295e3-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="295e3-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="295e3-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


