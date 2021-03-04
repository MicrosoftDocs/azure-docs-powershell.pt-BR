---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887548"
---
# <span data-ttu-id="d3f1f-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="d3f1f-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="d3f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f1f-103">Obtém a lista de recursos associados ao conjunto de criptografia de disco especificado.</span><span class="sxs-lookup"><span data-stu-id="d3f1f-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="d3f1f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3f1f-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f1f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f1f-106">O cmdlet **Get-AzDiskEncryptionSetAssociatedResource** obtém a lista de recursos associados ao conjunto de criptografia de disco especificado.</span><span class="sxs-lookup"><span data-stu-id="d3f1f-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="d3f1f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3f1f-107">EXAMPLES</span></span>

### <span data-ttu-id="d3f1f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3f1f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="d3f1f-109">O cmdlet recupera os dois recursos, 'exampleDisk01' e 'exampleDisk02', associados ao Conjunto de Criptografia de Disco fornecido</span><span class="sxs-lookup"><span data-stu-id="d3f1f-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="d3f1f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3f1f-110">PARAMETERS</span></span>

### <span data-ttu-id="d3f1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f1f-111">-DefaultProfile</span></span>
<span data-ttu-id="d3f1f-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f1f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f1f-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="d3f1f-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="d3f1f-114">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="d3f1f-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f1f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f1f-115">-ResourceGroupName</span></span>
<span data-ttu-id="d3f1f-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3f1f-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f1f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f1f-117">CommonParameters</span></span>
<span data-ttu-id="d3f1f-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f1f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f1f-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3f1f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f1f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3f1f-120">INPUTS</span></span>

### <span data-ttu-id="d3f1f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d3f1f-121">System.String</span></span>

## <span data-ttu-id="d3f1f-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3f1f-122">OUTPUTS</span></span>

### <span data-ttu-id="d3f1f-123">System.Uri[]</span><span class="sxs-lookup"><span data-stu-id="d3f1f-123">System.Uri[]</span></span>

## <span data-ttu-id="d3f1f-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3f1f-124">NOTES</span></span>

## <span data-ttu-id="d3f1f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3f1f-125">RELATED LINKS</span></span>
