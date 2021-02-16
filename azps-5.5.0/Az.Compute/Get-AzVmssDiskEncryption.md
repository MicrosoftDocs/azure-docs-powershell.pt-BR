---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117858"
---
# <span data-ttu-id="3181d-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3181d-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="3181d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3181d-102">SYNOPSIS</span></span>
<span data-ttu-id="3181d-103">Mostra o status de criptografia de disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="3181d-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="3181d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3181d-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3181d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3181d-105">DESCRIPTION</span></span>
<span data-ttu-id="3181d-106">Mostra o status de criptografia de disco de um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="3181d-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="3181d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3181d-107">EXAMPLES</span></span>

### <span data-ttu-id="3181d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3181d-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3181d-109">Mostra o status de criptografia de disco do conjunto de escala VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="3181d-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="3181d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3181d-110">PARAMETERS</span></span>

### <span data-ttu-id="3181d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3181d-111">-DefaultProfile</span></span>
<span data-ttu-id="3181d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3181d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3181d-113">-Nomeda Extensão</span><span class="sxs-lookup"><span data-stu-id="3181d-113">-ExtensionName</span></span>
<span data-ttu-id="3181d-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="3181d-114">The extension name.</span></span>
<span data-ttu-id="3181d-115">Se esse parâmetro não for especificado, os valores padrão usados serão VMs do AzureDiskEncryption para windows e VMs do AzureDiskEncryptionForLinux para Linux.</span><span class="sxs-lookup"><span data-stu-id="3181d-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="3181d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3181d-116">-ResourceGroupName</span></span>
<span data-ttu-id="3181d-117">Nome do grupo de recursos do conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3181d-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="3181d-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3181d-118">-VMScaleSetName</span></span>
<span data-ttu-id="3181d-119">O nome do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3181d-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="3181d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3181d-120">CommonParameters</span></span>
<span data-ttu-id="3181d-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3181d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3181d-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3181d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3181d-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="3181d-123">INPUTS</span></span>

### <span data-ttu-id="3181d-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3181d-124">System.String</span></span>

## <span data-ttu-id="3181d-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="3181d-125">OUTPUTS</span></span>

### <span data-ttu-id="3181d-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="3181d-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="3181d-127">Notas</span><span class="sxs-lookup"><span data-stu-id="3181d-127">NOTES</span></span>

## <span data-ttu-id="3181d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3181d-128">RELATED LINKS</span></span>
