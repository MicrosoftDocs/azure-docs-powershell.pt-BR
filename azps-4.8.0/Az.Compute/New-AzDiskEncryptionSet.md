---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111176"
---
# <span data-ttu-id="21a9e-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="21a9e-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="21a9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="21a9e-103">Cria um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="21a9e-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="21a9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21a9e-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="21a9e-106">Cria um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="21a9e-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="21a9e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21a9e-107">EXAMPLES</span></span>

### <span data-ttu-id="21a9e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21a9e-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="21a9e-109">Cria um conjunto de criptografia de disco usando a chave ativa fornecida no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="21a9e-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="21a9e-110">OS</span><span class="sxs-lookup"><span data-stu-id="21a9e-110">PARAMETERS</span></span>

### <span data-ttu-id="21a9e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21a9e-111">-AsJob</span></span>
<span data-ttu-id="21a9e-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21a9e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21a9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a9e-113">-DefaultProfile</span></span>
<span data-ttu-id="21a9e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21a9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a9e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a9e-115">-InputObject</span></span>
<span data-ttu-id="21a9e-116">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="21a9e-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="21a9e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="21a9e-117">-Name</span></span>
<span data-ttu-id="21a9e-118">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="21a9e-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="21a9e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a9e-119">-ResourceGroupName</span></span>
<span data-ttu-id="21a9e-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21a9e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="21a9e-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21a9e-121">-Confirm</span></span>
<span data-ttu-id="21a9e-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21a9e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a9e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a9e-123">-WhatIf</span></span>
<span data-ttu-id="21a9e-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21a9e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a9e-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21a9e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a9e-126">CommonParameters</span></span>
<span data-ttu-id="21a9e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a9e-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21a9e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a9e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21a9e-129">INPUTS</span></span>

### <span data-ttu-id="21a9e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="21a9e-130">System.String</span></span>

### <span data-ttu-id="21a9e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="21a9e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="21a9e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21a9e-132">OUTPUTS</span></span>

### <span data-ttu-id="21a9e-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="21a9e-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="21a9e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21a9e-134">NOTES</span></span>

## <span data-ttu-id="21a9e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21a9e-135">RELATED LINKS</span></span>
