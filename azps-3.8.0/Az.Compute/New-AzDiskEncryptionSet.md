---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941469"
---
# <span data-ttu-id="b4040-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4040-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="b4040-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4040-102">SYNOPSIS</span></span>
<span data-ttu-id="b4040-103">Cria um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4040-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="b4040-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4040-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4040-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4040-105">DESCRIPTION</span></span>
<span data-ttu-id="b4040-106">Cria um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4040-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="b4040-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4040-107">EXAMPLES</span></span>

### <span data-ttu-id="b4040-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4040-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="b4040-109">Cria um conjunto de criptografia de disco usando a chave ativa fornecida no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b4040-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="b4040-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4040-110">PARAMETERS</span></span>

### <span data-ttu-id="b4040-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4040-111">-AsJob</span></span>
<span data-ttu-id="b4040-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4040-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4040-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4040-113">-DefaultProfile</span></span>
<span data-ttu-id="b4040-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4040-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4040-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4040-115">-InputObject</span></span>
<span data-ttu-id="b4040-116">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4040-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4040-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4040-117">-Name</span></span>
<span data-ttu-id="b4040-118">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4040-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4040-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4040-119">-ResourceGroupName</span></span>
<span data-ttu-id="b4040-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4040-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4040-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4040-121">-Confirm</span></span>
<span data-ttu-id="b4040-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4040-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4040-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4040-123">-WhatIf</span></span>
<span data-ttu-id="b4040-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4040-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4040-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4040-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4040-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4040-126">CommonParameters</span></span>
<span data-ttu-id="b4040-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4040-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4040-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4040-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4040-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4040-129">INPUTS</span></span>

### <span data-ttu-id="b4040-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b4040-130">System.String</span></span>

### <span data-ttu-id="b4040-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4040-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="b4040-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4040-132">OUTPUTS</span></span>

### <span data-ttu-id="b4040-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4040-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="b4040-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4040-134">NOTES</span></span>

## <span data-ttu-id="b4040-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4040-135">RELATED LINKS</span></span>
