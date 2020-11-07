---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
ms.openlocfilehash: 2faa28fc0f0e4c27e384c178b96b8d38cae16a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786126"
---
# <span data-ttu-id="cae1d-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cae1d-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="cae1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cae1d-102">SYNOPSIS</span></span>
<span data-ttu-id="cae1d-103">Modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cae1d-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cae1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cae1d-104">SYNTAX</span></span>

### <span data-ttu-id="cae1d-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cae1d-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cae1d-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cae1d-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cae1d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cae1d-107">DESCRIPTION</span></span>
<span data-ttu-id="cae1d-108">O cmdlet **set-AzureRmVMBootDiagnostics** modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cae1d-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="cae1d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cae1d-109">EXAMPLES</span></span>

### <span data-ttu-id="cae1d-110">Exemplo 1: habilitar o diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="cae1d-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="cae1d-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="cae1d-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="cae1d-112">O comando o armazena na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="cae1d-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="cae1d-113">O segundo comando habilita o diagnóstico de inicialização para a máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="cae1d-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="cae1d-114">Os dados de diagnóstico são armazenados na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="cae1d-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="cae1d-115">OS</span><span class="sxs-lookup"><span data-stu-id="cae1d-115">PARAMETERS</span></span>

### <span data-ttu-id="cae1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae1d-116">-DefaultProfile</span></span>
<span data-ttu-id="cae1d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cae1d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae1d-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="cae1d-118">-Disable</span></span>
<span data-ttu-id="cae1d-119">Indica que esse cmdlet desabilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cae1d-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae1d-120">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="cae1d-120">-Enable</span></span>
<span data-ttu-id="cae1d-121">Indica que esse cmdlet habilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cae1d-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="cae1d-123">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cae1d-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae1d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cae1d-124">-StorageAccountName</span></span>
<span data-ttu-id="cae1d-125">Especifica o nome da conta de armazenamento na qual os dados de diagnóstico de inicialização são salvos.</span><span class="sxs-lookup"><span data-stu-id="cae1d-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae1d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="cae1d-126">-VM</span></span>
<span data-ttu-id="cae1d-127">Especifica a máquina virtual para a qual esse cmdlet altera o diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="cae1d-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="cae1d-128">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="cae1d-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae1d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae1d-129">CommonParameters</span></span>
<span data-ttu-id="cae1d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae1d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae1d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae1d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae1d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cae1d-132">INPUTS</span></span>

### <span data-ttu-id="cae1d-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cae1d-133">PSVirtualMachine</span></span>
<span data-ttu-id="cae1d-134">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cae1d-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="cae1d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cae1d-135">OUTPUTS</span></span>

### <span data-ttu-id="cae1d-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cae1d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cae1d-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cae1d-137">NOTES</span></span>

## <span data-ttu-id="cae1d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cae1d-138">RELATED LINKS</span></span>

[<span data-ttu-id="cae1d-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cae1d-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cae1d-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cae1d-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


