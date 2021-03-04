---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 344bba00d610b5e23b2af5bce8476185e8bee377
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887550"
---
# <span data-ttu-id="cd7ee-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cd7ee-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="cd7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7ee-103">Obter ou listar conjuntos de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="cd7ee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cd7ee-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd7ee-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cd7ee-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7ee-106">Obter ou listar conjuntos de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="cd7ee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd7ee-107">EXAMPLES</span></span>

### <span data-ttu-id="cd7ee-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd7ee-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="cd7ee-109">Obter conjunto de criptografia de disco 'enc1'</span><span class="sxs-lookup"><span data-stu-id="cd7ee-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="cd7ee-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cd7ee-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="cd7ee-111">Obter todos os conjuntos de criptografia de disco no grupo de recursos 'rg1'.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="cd7ee-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cd7ee-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="cd7ee-113">Obter todos os conjuntos de criptografia de disco na assinatura.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="cd7ee-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cd7ee-114">PARAMETERS</span></span>

### <span data-ttu-id="cd7ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7ee-115">-DefaultProfile</span></span>
<span data-ttu-id="cd7ee-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7ee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cd7ee-117">-Name</span></span>
<span data-ttu-id="cd7ee-118">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd7ee-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd7ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7ee-121">CommonParameters</span></span>
<span data-ttu-id="cd7ee-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7ee-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd7ee-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7ee-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd7ee-124">INPUTS</span></span>

### <span data-ttu-id="cd7ee-125">System.String</span><span class="sxs-lookup"><span data-stu-id="cd7ee-125">System.String</span></span>

## <span data-ttu-id="cd7ee-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cd7ee-126">OUTPUTS</span></span>

### <span data-ttu-id="cd7ee-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cd7ee-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="cd7ee-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="cd7ee-128">NOTES</span></span>

## <span data-ttu-id="cd7ee-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd7ee-129">RELATED LINKS</span></span>
