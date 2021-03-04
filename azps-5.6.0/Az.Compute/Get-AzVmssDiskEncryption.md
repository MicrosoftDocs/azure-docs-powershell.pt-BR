---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 56fcbadbcdbd874df3fea74918381eb24b2fa1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888999"
---
# <span data-ttu-id="acc93-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="acc93-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="acc93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc93-102">SYNOPSIS</span></span>
<span data-ttu-id="acc93-103">Mostra o status de criptografia de disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="acc93-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="acc93-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="acc93-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc93-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="acc93-105">DESCRIPTION</span></span>
<span data-ttu-id="acc93-106">Mostra o status de criptografia de disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="acc93-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="acc93-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acc93-107">EXAMPLES</span></span>

### <span data-ttu-id="acc93-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="acc93-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="acc93-109">Mostra o status de criptografia de disco do conjunto de escala VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="acc93-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="acc93-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="acc93-110">PARAMETERS</span></span>

### <span data-ttu-id="acc93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc93-111">-DefaultProfile</span></span>
<span data-ttu-id="acc93-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="acc93-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc93-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="acc93-113">-ExtensionName</span></span>
<span data-ttu-id="acc93-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="acc93-114">The extension name.</span></span>
<span data-ttu-id="acc93-115">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="acc93-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="acc93-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc93-116">-ResourceGroupName</span></span>
<span data-ttu-id="acc93-117">Nome do grupo de recursos do conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="acc93-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="acc93-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="acc93-118">-VMScaleSetName</span></span>
<span data-ttu-id="acc93-119">O nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="acc93-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="acc93-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc93-120">CommonParameters</span></span>
<span data-ttu-id="acc93-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc93-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc93-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acc93-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc93-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acc93-123">INPUTS</span></span>

### <span data-ttu-id="acc93-124">System.String</span><span class="sxs-lookup"><span data-stu-id="acc93-124">System.String</span></span>

## <span data-ttu-id="acc93-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="acc93-125">OUTPUTS</span></span>

### <span data-ttu-id="acc93-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="acc93-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="acc93-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="acc93-127">NOTES</span></span>

## <span data-ttu-id="acc93-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acc93-128">RELATED LINKS</span></span>
