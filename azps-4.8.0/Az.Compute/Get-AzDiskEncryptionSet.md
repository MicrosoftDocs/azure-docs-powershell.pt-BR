---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948147"
---
# <span data-ttu-id="3aff6-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3aff6-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="3aff6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3aff6-102">SYNOPSIS</span></span>
<span data-ttu-id="3aff6-103">Obter ou listar conjuntos de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="3aff6-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="3aff6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3aff6-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aff6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3aff6-105">DESCRIPTION</span></span>
<span data-ttu-id="3aff6-106">Obter ou listar conjuntos de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="3aff6-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="3aff6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3aff6-107">EXAMPLES</span></span>

### <span data-ttu-id="3aff6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3aff6-108">Example 1</span></span>
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

<span data-ttu-id="3aff6-109">Obter conjunto de criptografia de disco ' enc1 '</span><span class="sxs-lookup"><span data-stu-id="3aff6-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="3aff6-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3aff6-110">Example 2</span></span>
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

<span data-ttu-id="3aff6-111">Obter todos os conjuntos de criptografia de disco no grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="3aff6-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="3aff6-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3aff6-112">Example 3</span></span>
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

<span data-ttu-id="3aff6-113">Obter todos os conjuntos de criptografia de disco na assinatura.</span><span class="sxs-lookup"><span data-stu-id="3aff6-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="3aff6-114">OS</span><span class="sxs-lookup"><span data-stu-id="3aff6-114">PARAMETERS</span></span>

### <span data-ttu-id="3aff6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aff6-115">-DefaultProfile</span></span>
<span data-ttu-id="3aff6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3aff6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aff6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3aff6-117">-Name</span></span>
<span data-ttu-id="3aff6-118">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="3aff6-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="3aff6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aff6-119">-ResourceGroupName</span></span>
<span data-ttu-id="3aff6-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3aff6-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3aff6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aff6-121">CommonParameters</span></span>
<span data-ttu-id="3aff6-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aff6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aff6-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3aff6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aff6-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3aff6-124">INPUTS</span></span>

### <span data-ttu-id="3aff6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3aff6-125">System.String</span></span>

## <span data-ttu-id="3aff6-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3aff6-126">OUTPUTS</span></span>

### <span data-ttu-id="3aff6-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3aff6-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="3aff6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3aff6-128">NOTES</span></span>

## <span data-ttu-id="3aff6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3aff6-129">RELATED LINKS</span></span>
