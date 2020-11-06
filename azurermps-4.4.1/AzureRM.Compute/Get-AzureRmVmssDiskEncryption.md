---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 045265a347b4a8bbcc387079f3c5a27a629a8ec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432639"
---
# <span data-ttu-id="be5a0-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="be5a0-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="be5a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be5a0-102">SYNOPSIS</span></span>
<span data-ttu-id="be5a0-103">Mostra o status de criptografia do disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="be5a0-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be5a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be5a0-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be5a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be5a0-105">DESCRIPTION</span></span>
<span data-ttu-id="be5a0-106">Mostra o status de criptografia do disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="be5a0-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="be5a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be5a0-107">EXAMPLES</span></span>

### <span data-ttu-id="be5a0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be5a0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="be5a0-109">Mostra o status de criptografia de disco do conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="be5a0-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="be5a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="be5a0-110">PARAMETERS</span></span>

### <span data-ttu-id="be5a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5a0-111">-DefaultProfile</span></span>
<span data-ttu-id="be5a0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be5a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be5a0-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="be5a0-113">-ExtensionName</span></span>
<span data-ttu-id="be5a0-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="be5a0-114">The extension name.</span></span>
<span data-ttu-id="be5a0-115">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="be5a0-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="be5a0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5a0-116">-ResourceGroupName</span></span>
<span data-ttu-id="be5a0-117">Nome do grupo de recursos do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="be5a0-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5a0-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="be5a0-118">-VMScaleSetName</span></span>
<span data-ttu-id="be5a0-119">O nome do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be5a0-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5a0-120">CommonParameters</span></span>
<span data-ttu-id="be5a0-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5a0-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5a0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5a0-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be5a0-123">INPUTS</span></span>

### <span data-ttu-id="be5a0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="be5a0-124">System.String</span></span>

## <span data-ttu-id="be5a0-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be5a0-125">OUTPUTS</span></span>

### <span data-ttu-id="be5a0-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="be5a0-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="be5a0-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be5a0-127">NOTES</span></span>

## <span data-ttu-id="be5a0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be5a0-128">RELATED LINKS</span></span>

