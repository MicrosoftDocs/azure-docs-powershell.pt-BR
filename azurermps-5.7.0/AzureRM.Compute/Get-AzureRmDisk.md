---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431068"
---
# <span data-ttu-id="45c2e-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="45c2e-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="45c2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="45c2e-103">Obtém as propriedades de um disco.</span><span class="sxs-lookup"><span data-stu-id="45c2e-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45c2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45c2e-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="45c2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="45c2e-106">O cmdlet **Get-AzureRmDisk** Obtém as propriedades de um disco.</span><span class="sxs-lookup"><span data-stu-id="45c2e-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="45c2e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45c2e-107">EXAMPLES</span></span>

### <span data-ttu-id="45c2e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45c2e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="45c2e-109">Este comando obtém as propriedades do disco chamado "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="45c2e-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="45c2e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="45c2e-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="45c2e-111">Esse comando obtém as propriedades de todos os discos no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="45c2e-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="45c2e-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="45c2e-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="45c2e-113">Esse comando obtém as propriedades de todos os discos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="45c2e-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="45c2e-114">OS</span><span class="sxs-lookup"><span data-stu-id="45c2e-114">PARAMETERS</span></span>

### <span data-ttu-id="45c2e-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="45c2e-115">-DiskName</span></span>
<span data-ttu-id="45c2e-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="45c2e-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c2e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c2e-117">-ResourceGroupName</span></span>
<span data-ttu-id="45c2e-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45c2e-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c2e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c2e-119">CommonParameters</span></span>
<span data-ttu-id="45c2e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c2e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c2e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c2e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c2e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45c2e-122">INPUTS</span></span>

### <span data-ttu-id="45c2e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="45c2e-123">System.String</span></span>

## <span data-ttu-id="45c2e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45c2e-124">OUTPUTS</span></span>

### <span data-ttu-id="45c2e-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="45c2e-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="45c2e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45c2e-126">NOTES</span></span>

## <span data-ttu-id="45c2e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45c2e-127">RELATED LINKS</span></span>

