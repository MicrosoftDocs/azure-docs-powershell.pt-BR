---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
ms.openlocfilehash: 551e5928ca4628b9964132ee117cbf65fdbaedba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426422"
---
# <span data-ttu-id="5603b-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5603b-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="5603b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5603b-102">SYNOPSIS</span></span>
<span data-ttu-id="5603b-103">Mostra o status de criptografia de disco das VMs em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="5603b-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5603b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5603b-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5603b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5603b-105">DESCRIPTION</span></span>
<span data-ttu-id="5603b-106">Mostra o status de criptografia do disco do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="5603b-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="5603b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5603b-107">EXAMPLES</span></span>

### <span data-ttu-id="5603b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5603b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="5603b-109">Mostra o status de criptografia de disco da instância de VM 1 no conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="5603b-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5603b-110">OS</span><span class="sxs-lookup"><span data-stu-id="5603b-110">PARAMETERS</span></span>

### <span data-ttu-id="5603b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5603b-111">-DefaultProfile</span></span>
<span data-ttu-id="5603b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5603b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5603b-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5603b-113">-ExtensionName</span></span>
<span data-ttu-id="5603b-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="5603b-114">The extension name.</span></span>
<span data-ttu-id="5603b-115">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="5603b-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="5603b-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5603b-116">-InstanceId</span></span>
<span data-ttu-id="5603b-117">Especifica a ID de instância.</span><span class="sxs-lookup"><span data-stu-id="5603b-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="5603b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5603b-118">-ResourceGroupName</span></span>
<span data-ttu-id="5603b-119">Nome do grupo de recursos do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5603b-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5603b-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5603b-120">-VMScaleSetName</span></span>
<span data-ttu-id="5603b-121">O nome do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5603b-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="5603b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5603b-122">CommonParameters</span></span>
<span data-ttu-id="5603b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5603b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5603b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5603b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5603b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5603b-125">INPUTS</span></span>

### <span data-ttu-id="5603b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5603b-126">System.String</span></span>

## <span data-ttu-id="5603b-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5603b-127">OUTPUTS</span></span>

### <span data-ttu-id="5603b-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="5603b-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="5603b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5603b-129">NOTES</span></span>

## <span data-ttu-id="5603b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5603b-130">RELATED LINKS</span></span>
