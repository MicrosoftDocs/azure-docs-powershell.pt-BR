---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941467"
---
# <span data-ttu-id="f5060-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="f5060-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="f5060-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5060-102">SYNOPSIS</span></span>
<span data-ttu-id="f5060-103">Cria um objeto configurável de conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="f5060-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="f5060-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5060-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5060-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5060-105">DESCRIPTION</span></span>
<span data-ttu-id="f5060-106">Cria um objeto configurável de conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="f5060-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="f5060-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5060-107">EXAMPLES</span></span>

### <span data-ttu-id="f5060-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5060-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="f5060-109">Cria um conjunto de criptografia de disco usando a chave ativa fornecida no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f5060-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="f5060-110">OS</span><span class="sxs-lookup"><span data-stu-id="f5060-110">PARAMETERS</span></span>

### <span data-ttu-id="f5060-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5060-111">-DefaultProfile</span></span>
<span data-ttu-id="f5060-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5060-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5060-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f5060-113">-IdentityType</span></span>
<span data-ttu-id="f5060-114">O tipo de identidade gerenciada usado pelo DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="f5060-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="f5060-115">Só há suporte para SystemAssigned.</span><span class="sxs-lookup"><span data-stu-id="f5060-115">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="f5060-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="f5060-116">-KeyUrl</span></span>
<span data-ttu-id="f5060-117">URL apontando para a chave ativa no cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="f5060-117">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5060-118">-Local</span><span class="sxs-lookup"><span data-stu-id="f5060-118">-Location</span></span>
<span data-ttu-id="f5060-119">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="f5060-119">Specifies a location.</span></span>

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

### <span data-ttu-id="f5060-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f5060-120">-SourceVaultId</span></span>
<span data-ttu-id="f5060-121">ID do recurso do cofre que contém a tecla ativa.</span><span class="sxs-lookup"><span data-stu-id="f5060-121">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5060-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="f5060-122">-Tag</span></span>
<span data-ttu-id="f5060-123">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f5060-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f5060-124">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f5060-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5060-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5060-125">-Confirm</span></span>
<span data-ttu-id="f5060-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5060-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5060-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5060-127">-WhatIf</span></span>
<span data-ttu-id="f5060-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5060-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5060-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5060-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5060-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5060-130">CommonParameters</span></span>
<span data-ttu-id="f5060-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5060-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5060-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5060-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5060-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5060-133">INPUTS</span></span>

### <span data-ttu-id="f5060-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f5060-134">System.String</span></span>

### <span data-ttu-id="f5060-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f5060-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f5060-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5060-136">OUTPUTS</span></span>

### <span data-ttu-id="f5060-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f5060-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="f5060-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5060-138">NOTES</span></span>

## <span data-ttu-id="f5060-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5060-139">RELATED LINKS</span></span>
