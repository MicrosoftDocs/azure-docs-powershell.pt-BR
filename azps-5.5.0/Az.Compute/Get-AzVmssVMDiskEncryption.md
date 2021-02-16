---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127098"
---
# <span data-ttu-id="82ddd-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="82ddd-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="82ddd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="82ddd-103">Mostra o status de criptografia de disco de VMs em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="82ddd-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="82ddd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82ddd-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ddd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="82ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="82ddd-106">Mostra o status de criptografia de disco do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="82ddd-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="82ddd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="82ddd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="82ddd-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="82ddd-109">Mostra o status de criptografia de disco da instância VM 1 no conjunto de escala VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="82ddd-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="82ddd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82ddd-110">PARAMETERS</span></span>

### <span data-ttu-id="82ddd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ddd-111">-DefaultProfile</span></span>
<span data-ttu-id="82ddd-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="82ddd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ddd-113">-Nomeda Extensão</span><span class="sxs-lookup"><span data-stu-id="82ddd-113">-ExtensionName</span></span>
<span data-ttu-id="82ddd-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="82ddd-114">The extension name.</span></span>
<span data-ttu-id="82ddd-115">Se esse parâmetro não for especificado, os valores padrão usados serão VMs do AzureDiskEncryption para windows e VMs do AzureDiskEncryptionForLinux para Linux.</span><span class="sxs-lookup"><span data-stu-id="82ddd-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ddd-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="82ddd-116">-InstanceId</span></span>
<span data-ttu-id="82ddd-117">Especifica a ID de instância.</span><span class="sxs-lookup"><span data-stu-id="82ddd-117">Specifies the instance ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ddd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ddd-118">-ResourceGroupName</span></span>
<span data-ttu-id="82ddd-119">Nome do grupo de recursos do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82ddd-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="82ddd-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="82ddd-120">-VMScaleSetName</span></span>
<span data-ttu-id="82ddd-121">O nome do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82ddd-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ddd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ddd-122">CommonParameters</span></span>
<span data-ttu-id="82ddd-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ddd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ddd-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82ddd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ddd-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="82ddd-125">INPUTS</span></span>

### <span data-ttu-id="82ddd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="82ddd-126">System.String</span></span>

## <span data-ttu-id="82ddd-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="82ddd-127">OUTPUTS</span></span>

### <span data-ttu-id="82ddd-128">Microsoft.Azure.Commands.Compute.Models.PSVmsSVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="82ddd-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="82ddd-129">Notas</span><span class="sxs-lookup"><span data-stu-id="82ddd-129">NOTES</span></span>

## <span data-ttu-id="82ddd-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82ddd-130">RELATED LINKS</span></span>
