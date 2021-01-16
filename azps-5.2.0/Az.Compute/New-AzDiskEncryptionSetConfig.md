---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257731"
---
# <span data-ttu-id="a6396-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="a6396-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="a6396-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6396-102">SYNOPSIS</span></span>
<span data-ttu-id="a6396-103">Cria um objeto configurável de conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="a6396-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="a6396-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6396-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6396-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6396-105">DESCRIPTION</span></span>
<span data-ttu-id="a6396-106">Cria um objeto configurável de conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="a6396-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="a6396-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6396-107">EXAMPLES</span></span>

### <span data-ttu-id="a6396-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6396-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="a6396-109">Cria um conjunto de criptografia de disco usando a chave ativa fornecida no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a6396-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="a6396-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6396-110">PARAMETERS</span></span>

### <span data-ttu-id="a6396-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6396-111">-DefaultProfile</span></span>
<span data-ttu-id="a6396-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6396-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6396-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="a6396-113">-EncryptionType</span></span>
<span data-ttu-id="a6396-114">Use esta configuração para definir o tipo de criptografia do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="a6396-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="a6396-115">Os valores disponíveis são: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey".</span><span class="sxs-lookup"><span data-stu-id="a6396-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="a6396-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a6396-116">-IdentityType</span></span>
<span data-ttu-id="a6396-117">O tipo de identidade gerenciada usado pelo DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="a6396-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="a6396-118">Só há suporte para SystemAssigned.</span><span class="sxs-lookup"><span data-stu-id="a6396-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="a6396-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="a6396-119">-KeyUrl</span></span>
<span data-ttu-id="a6396-120">URL apontando para a chave ativa no cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a6396-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="a6396-121">-Local</span><span class="sxs-lookup"><span data-stu-id="a6396-121">-Location</span></span>
<span data-ttu-id="a6396-122">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="a6396-122">Specifies a location.</span></span>

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

### <span data-ttu-id="a6396-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a6396-123">-SourceVaultId</span></span>
<span data-ttu-id="a6396-124">ID do recurso do cofre que contém a tecla ativa.</span><span class="sxs-lookup"><span data-stu-id="a6396-124">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="a6396-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="a6396-125">-Tag</span></span>
<span data-ttu-id="a6396-126">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a6396-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6396-127">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a6396-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a6396-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6396-128">-Confirm</span></span>
<span data-ttu-id="a6396-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6396-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6396-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6396-130">-WhatIf</span></span>
<span data-ttu-id="a6396-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6396-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6396-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6396-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6396-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6396-133">CommonParameters</span></span>
<span data-ttu-id="a6396-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6396-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6396-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6396-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6396-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6396-136">INPUTS</span></span>

### <span data-ttu-id="a6396-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a6396-137">System.String</span></span>

### <span data-ttu-id="a6396-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a6396-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a6396-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6396-139">OUTPUTS</span></span>

### <span data-ttu-id="a6396-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a6396-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="a6396-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6396-141">NOTES</span></span>

## <span data-ttu-id="a6396-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6396-142">RELATED LINKS</span></span>
