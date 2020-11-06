---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5219b43a1d80515f0bce02c5f6fdd2117b736a00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601332"
---
# <span data-ttu-id="aab1c-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="aab1c-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="aab1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aab1c-102">SYNOPSIS</span></span>
<span data-ttu-id="aab1c-103">Mostra o status de criptografia do disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="aab1c-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="aab1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aab1c-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aab1c-105">DESCRIPTION</span></span>
<span data-ttu-id="aab1c-106">Mostra o status de criptografia do disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="aab1c-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="aab1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aab1c-107">EXAMPLES</span></span>

### <span data-ttu-id="aab1c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aab1c-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="aab1c-109">Mostra o status de criptografia de disco do conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="aab1c-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="aab1c-110">OS</span><span class="sxs-lookup"><span data-stu-id="aab1c-110">PARAMETERS</span></span>

### <span data-ttu-id="aab1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab1c-111">-DefaultProfile</span></span>
<span data-ttu-id="aab1c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aab1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab1c-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="aab1c-113">-ExtensionName</span></span>
<span data-ttu-id="aab1c-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="aab1c-114">The extension name.</span></span>
<span data-ttu-id="aab1c-115">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="aab1c-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="aab1c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab1c-116">-ResourceGroupName</span></span>
<span data-ttu-id="aab1c-117">Nome do grupo de recursos do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="aab1c-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="aab1c-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aab1c-118">-VMScaleSetName</span></span>
<span data-ttu-id="aab1c-119">O nome do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aab1c-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="aab1c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab1c-120">CommonParameters</span></span>
<span data-ttu-id="aab1c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab1c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab1c-122">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aab1c-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab1c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aab1c-123">INPUTS</span></span>

### <span data-ttu-id="aab1c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="aab1c-124">System.String</span></span>

## <span data-ttu-id="aab1c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aab1c-125">OUTPUTS</span></span>

### <span data-ttu-id="aab1c-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="aab1c-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="aab1c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aab1c-127">NOTES</span></span>

## <span data-ttu-id="aab1c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aab1c-128">RELATED LINKS</span></span>
