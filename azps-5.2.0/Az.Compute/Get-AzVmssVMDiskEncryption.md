---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263896"
---
# <span data-ttu-id="0256a-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0256a-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="0256a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0256a-102">SYNOPSIS</span></span>
<span data-ttu-id="0256a-103">Mostra o status de criptografia de disco das VMs em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="0256a-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="0256a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0256a-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0256a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0256a-105">DESCRIPTION</span></span>
<span data-ttu-id="0256a-106">Mostra o status de criptografia do disco do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="0256a-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="0256a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0256a-107">EXAMPLES</span></span>

### <span data-ttu-id="0256a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0256a-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="0256a-109">Mostra o status de criptografia de disco da instância de VM 1 no conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="0256a-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0256a-110">OS</span><span class="sxs-lookup"><span data-stu-id="0256a-110">PARAMETERS</span></span>

### <span data-ttu-id="0256a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0256a-111">-DefaultProfile</span></span>
<span data-ttu-id="0256a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0256a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0256a-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="0256a-113">-ExtensionName</span></span>
<span data-ttu-id="0256a-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="0256a-114">The extension name.</span></span>
<span data-ttu-id="0256a-115">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="0256a-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="0256a-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0256a-116">-InstanceId</span></span>
<span data-ttu-id="0256a-117">Especifica a ID de instância.</span><span class="sxs-lookup"><span data-stu-id="0256a-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="0256a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0256a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0256a-119">Nome do grupo de recursos do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0256a-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0256a-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0256a-120">-VMScaleSetName</span></span>
<span data-ttu-id="0256a-121">O nome do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0256a-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="0256a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0256a-122">CommonParameters</span></span>
<span data-ttu-id="0256a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0256a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0256a-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0256a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0256a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0256a-125">INPUTS</span></span>

### <span data-ttu-id="0256a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0256a-126">System.String</span></span>

## <span data-ttu-id="0256a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0256a-127">OUTPUTS</span></span>

### <span data-ttu-id="0256a-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="0256a-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="0256a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0256a-129">NOTES</span></span>

## <span data-ttu-id="0256a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0256a-130">RELATED LINKS</span></span>
